# Flask Restful API

After going through the straightforward startup documentation found on the official [flask page](""), we are ready to explore the Flask_RESTful library and some of the syntax to programmatically store and retrieve data elements. 

Flask_RESTful utilizes the elements of Create, Read, Update, and Delete (CRUD– these four elements makeup the mainstays of persistent data management using a Structured Query Language (SQL) database. 

## CRUD Breakdown:
Create - This type refers to the addition of new data entries into the database. In the Flask_RESTful library, the method leverages the POST statement. 
Read - A statement of this variety refers to returned data based on a specific GET query.
Update - Similar to the Create (POST) method, Update allows for edits to existing data elements within the database. This method utilizes the PUT statement to communicate with the endpoint.
Delete - The delete statement, referred to as DEL, removes the data from the database, excluding it from future queries. 

## Package Installations:
Before attempting this in your own development environment, make sure you have the correct package installations. For this article, we will need to install the flask_restful library packages, this must be performed in the same VirtualEnvironment as the initial Flask startup guide. 

If unsure, the command [pip freeze] provides a list of all current packages.

## Connecting to a Database
```
Codebase```

The initial import statements establish our methods and application connections. However, before we go any farther, we need to set up our working database. In the above example, we see the If statement is used to programmatically spin up a new database with the name = dsworld.db.




