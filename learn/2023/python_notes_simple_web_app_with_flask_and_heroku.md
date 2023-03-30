## Python Tutorial: Python Simplified  

[Full video:](https://www.youtube.com/watch?v=6plVs_ytIH8&t=425s)

**Flask:** Made up of several languages, including HTML, CSS, JavaScript, and Python.

**File Structure:**   
Within our project folder, we will need to create two empty directories (or folders). 
1. templates  
    - In this folder create a file index.html
2. static 
    - In this folder create another empty directory titled css

#### Example: index.html
```Python
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>Say Hello</title>
        <link rel="stylesheet" href="{{ url_for('static', filename='css/main.css')}}">
    </head>
    <body>
        <img src="http://raw.githubusercontent.com/MariyaSha/SimpleGreetingApp/main/logo.png">
        <br>
        <form action="greet" method="post">
            {% for message in get_flashed_message()%}
                <p> {{message}} </p>
            {% endfor %}
            <br>
            <input type="text" name="name_input">
            <br>
            <input type="submit" value="GREET" id="greet">
        </form>
    </body>
</html>
```

```Python
from flask import Flask, render_template, request, flash

app = Flask(__name__)
app.secret_key = "the_markdown_GUIDE"


@app.route("/hello")
def index():
    flash("What's your name?")
    return render_template("index.html")


@app.route("/greet", methods=["POST", "GET"])
def greet():
    flash("Hi " + str(request.form['name_input']) + ", great to see you!")
    return render_template("index.html")
```

### **HTML Interaction with Python:**
Syntax:

{{ % for loop in function()%}}
    <p>{{   }}</p>
{{% forend %}}

#### Example: 

{% for message in get_flashed_message()%}
 <p> {{message}} </p>
{% endfor %}


#### Example: Python
```Python 
@app.route("/hello")
def index():
    flash("What's your name?")   # Flash is the connecting word with html
    return render_template("index.html")
```

#### Example: CSS
```CSS
body {
    background-color: #2e8b57;
    text-align: center;
}

p {
    color: white;
    font-family: Shanti;
    font-size: 1.2em;
    margin: 20px;
}

img {
    margin: 60px 0 30px 0;
    width: 250px;
}

input {
    width: 300px;
    height: 50px;
    margin: 20px;
    border: none;
    border-radius: 10px;
    font-family: Shanti;
    text-align: center;
    font-size: 1.3em;
}

input: focus {
    border: solid 5px #00FFCE;
    outline: none;
}

#greet {
    background-color: #8fbc8f;
    color: white;
    width: 200px;
}

#greet:hover {
    background-color: #556b2f;
    cursor: pointer;
}
```
#### **Additional Requirements:**
1. From the terminal, within the root project directory. Run:
```
pip install gunicorn
```
2. Next, create a new file in the root directory (project folder):
```
echo > Procfile 
```
3. Navigate to the file folder within the finder and open Procfile in Notepad. In the file update the content as follows:
    - Keep in mind, the spacing must match the above example.
```
web: gunicorn app:app
```
4. Back at the Terminal within the root directory:
``` 
pip freeze > requirements.txt
```
5. Open file in the directory. Locate the MarkupSafe entry - if missing, at Terminal:
``` 
pip install MarkupSafe
```

 6. At the .txt file, change the MarkupSafe value to == the version number:
 ```
 MarkupSafe == 2.0.1
 ```

### **Deployment:** ~~Heroku~~  
 No longer a free option available.  
 Alternatively, use [Python Anywhere!](https://www.pythonanywhere.com)
 
### **App Demonstration:**
#### Example: Landing
<img src="https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/sayHello_landing.jpg" width="50%" height="50%">

#### Example: Response
<img src="https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/sayHello_response.jpg" width="50%" height="50%">

[Top](#python-tutorial-python-simplified)
