## **A simple Flask based application** designed to index novels, including page count, author name, genre, and of course, the title. 

<img src="https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/bookapp1.png" width="50%" float="right" margin-right="10px">  

*This screen shows the interface for adding a new novel to the DB.* 

<img src="https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/bookapp3.png" width="50%" float="right" margin-right="10px">

Now let's take a look under the hood and see what the 'POST' method is doing. As you can see, each of the four input fields is saved as its own variable, including the final variable 'book' which captures all four data points and prepares them for the db.add statement.

Click the link below to see the full repo.  
[novel_app](https://github.com/grassLEE/novel_app.git)