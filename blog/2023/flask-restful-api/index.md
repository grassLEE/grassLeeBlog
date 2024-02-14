# Flask Restful API

After going through the straightforward startup documentation found on the official [flask page]("https://flask.palletsprojects.com/en/2.3.x/"), we are ready to explore the Flask_RESTful library and some of the syntax to programmatically store and retrieve data elements. 

Flask_RESTful utilizes the elements Create, Read, Update, and Delete (CRUD)– these four elements makeup the mainstays of persistent data management using a Structured Query Language (SQL) database. 

## CRUD Breakdown:
**Create** - This type refers to the addition of new data entries into the database. In the Flask_RESTful library, the method leverages the POST statement.  
**Read** - A statement of this variety refers to returned data based on a specific GET query.  
**Update** - Similar to the Create (POST) method, Update allows for edits to existing data elements within the database. This method utilizes the PUT statement to communicate with the endpoint.  
**Delete** - The delete statement, referred to as DEL, removes the data from the database, excluding it from future queries.  

## Package Installations:
Before attempting this in your own development environment, make sure you have the correct package installations. For this article, we will need to install the flask_restful library packages, this must be performed in the same VirtualEnvironment as the initial Flask startup guide. 

If unsure, the command [pip freeze] provides a list of all current packages.

## Database Connection
```
from flask import Flask, request
from flask_restful import Api, Resource, reqparse
import sqlite3
import os
import json

app = Flask(__name__)
api = Api(app)

if not os.path.exists('dsworld.db'):
    open('dsworld.db', 'w').close()

# Create a connection to the SQLite database
conn = sqlite3.connect('dsworld.db')
cursor = conn.cursor()

# Create a table if it doesn't exist
cursor.execute('''CREATE TABLE IF NOT EXISTS novel
                (id INTEGER PRIMARY KEY AUTOINCREMENT,
                name TEXT NOT NULL,
                email TEXT NOT NULL)''')
conn.commit()

```
The initial import statements establish our methods and application connections. However, before we go any farther, we need to set up our working database. In the above example, we see the If statement is used to programmatically spin up a new database with the name = dsworld.db.

This programming logic allows us to run the API without having to previously spin up the **dsworld.db** file. However, we will need to make our db connection in each of our following endpoints.

## GET Method:
```
class AllNovels(Resource):
    def get(self, novel_id=None):
        conn = sqlite3.connect('dsworld.db')
        cursor = conn.cursor()

        if novel_id:
            cursor.execute("SELECT * FROM novels WHERE id=?", 
                           (novel_id,))
        else:
            cursor.execute("SELECT * FROM novels")

        novels = cursor.fetchall()
        novel_list = []
        for novel in novels:
            novel_list.append({
                'title': novel[1],
                'pages': novel[2],
                'focus': novel[3]
            })
        
        conn.close()
        return {'novels': novel_list}
```

A unique aspect of the initial def GET(self, novel_id=None) is the **=None** as this allows us to use the parameter for both single query entries and all entries in the db. The following **if statement** establishes the operating logic to handle the **novel_id** if it exists. 

This single query entry makes use of the specific novel_id by setting it as a parameter of the SQL query: 
```cursor.execute("SELECT * FROM novels WHERE id=?", (novel_id,))```

Whereas the following **else** statement provides an alternative SQL query targeting ALL entries. cursor.execute("SELECT * FROM novels")

Now to iterate over the similar types in our db, we call the cursor again along with the fetchall() method. This will allow us to populate the **novel_list** with a simple **for** loop. We are then able to comb through the entire list and print the list back with the final return statement **return {'novels': novel_list}**
## POST Method:

```
def post(self):
        data = request.get_json(force=True)
        if not data:
            return {'message': "Invalid request format. Expected 'application/json'."}, 400

        title = data.get('title')
        focus = data.get('focus')

        if not title or not focus:
            return {'message': 'Missing required data'}, 401
        
        conn = sqlite3.connect('dsworld.db')
        cursor = conn.cursor()
        parser = reqparse.RequestParser()
        parser.add_argument('title', type=str, required=True)
        parser.add_argument('pages', type=int, required=True)
        parser.add_argument('focus', type=str, required=True)
        args = parser.parse_args()

        cursor.execute("INSERT INTO novels (title, pages, focus) VALUES (?, ?, ?)", 
                       (args['title'], args['pages'], args['focus']))
        
        conn.commit()
        conn.close()
        return {'message': 'Novel added'}
```
The next section demonstrates some additional complications, namely with the data = request.get_json(force=True) statement. This is used to make a simpler POST command in our terminal, without the need to set the specific 'application/json' parameter with every request. Moreover, the programming logic accounts for non-json requests, which returns a dictionary error message, helping ensure we are handling the correct data format. 

Next, we use the request library to pass in the arguments for **title** and **focus**, which again features another potential error message that would catch any missing data points before attempting to save them to our db. 

Afterwards, our POST method needs to set up the correct handling logic for the components of the endpoint. Notice, the parser.add_arguments() method features an additional argument. This is completely fine as we don't have to use every component of an endpoint when setting up qualifying checks. 

Finally, we have our next SQL command, which targets the correct table in our db and passes the arguments of our POST in the parsing tool. 

```cursor.execute("INSERT INTO novels (title, pages, focus) VALUES (?, ?, ?)", (args['title'], args['pages'], args['focus']))```

Remember, we have to use the same amount of (?, ?, ?) to match the number of arguments we are passing into the db.

## Add_Resource():
Now that we have our GET and POST method established. We are nearly ready to give this a test run, but first we have to establish our URL endpoint.

This is performed with this simple command logic
```api.add_resource(AllNovels, '/dsworld', '/dsworld/<int:novel_id>'```

Here, we have two separate endpoints, the first '/dsworld' will return our list of novels from the db. While the '/dsworld/<int:novel_id>' will return the individual novel based on ID.

Finally, make sure to include this:

```if __name__ == '__main__':```
    ```app.run(debug=True)```

This will allow for the app to run reliably and include debug messages should we encounter an error. 

[Top](#flask-restful-api)