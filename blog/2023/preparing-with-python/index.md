# Preparing with Python: Formatting Lists between Common Apps

Python is a versatile tool capable of automating a great deal of our daily tasks, from programmatically changing filenames, to sorting datasets by entry value, and a great deal in between. These tools are available to even the most green of beginners, so there is no need to feel intimidated.  

Let’s explore a common data entry task and see how Python can simplify the process. Consider an Excel Spreadsheet just like this one below:  

## Example Excel Spreadsheet  

![image of example excel chart](https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/excel_project_example.png)

You’ll notice the column 'A' features a long list of names. Now, if we wanted to extract that information, we could just copy/paste the data into a Word doc and call it a day. However, that option is quite limiting in terms of formatting and modularity. This can become further complicated if our example list features several duplicate values.  

Let's take a look at an example with these values pasted directly, we will end up with a crude copy of the list such as this sample.  
## Sample Copy/Paste - With Formatting
![unformatted table](https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/copy_paste_example.png)


Here, you have a copy of our table from Excel. This appears quite nicely formatted, but appearances can be deceiving as you will notice how challenging it can be to move entries around, add visible text, and even use additional formatting considerations such as bulleted/numbered lists.

Now, we'll look at another scenario.

## Sample Copy/Paste - Without Formatting

![unformatted copy/paste](https://raw.githubusercontent.com/grassLEE/grassleeblog/main/images/copy_paste_2.png)

This mess is easy to identify as just that, but you will notice the entries can be repositioned without much issue, except for the excessive time sink the task would demand. Each line would have to be restructured!

It is pretty obvious that both copy/paste examples fail to provide a clean output, ready for additional information. Fortunately for us, Python offers a simple way to format this data, ensuring the final output features a properly formatted list.

## Triple Quotes - More than just Docstrings
First, we need to capture both lists and store them into unique variables. This is accomplished through “””triple quotes”””, which allows Python to interpret multiple lines without causing an error. 

```Python
project_titles = """
CodeCraft Pro
ByteWave Studio
DataFusion Plus
CodeGenius Suite
TechSynth Pro
LogicNest Studio
BitLink Connect
DataForge Pro
PixelMerge Pro
CodeFlow Nexus
QuantumScript Pro
CyberLink Nexus
CodePulse Studio
ByteBeam Fusion
LogicBurst Pro
DataCraft Nexus
CodeVista Suite
ByteForge Nexus
CloudWave Pro
DataLink Nexus
BytePulse Fusion
LogicLink Studio
CodeWave Nexus
PixelCraft Pro
ByteSynth Fusion
""".splitlines()
```

Notice the last line of this first example, which stores the list of project names copied and pasted directly between the quotes, ends with the ‘.splitlines()’ method. This method will return a list of the lines separated into a string, each broken at the line break.

However, keep in mind, we can preserve the line breaks by passing in the argument ‘keepends’ and setting the value to True– this will ensure the returned object includes the previous line breaks. Although, this is not the only way to separate the information into new lines (more on that below).

Moving forward, we’ll save the Project Descriptions in the same way and print the output of our variables to verify the information appears correct.


```Python
for project_title in project_titles:
print(f"\n{project_title}")


for project_description in project_descriptions:
print(f"\n{project_description}")
```

These simple For loops iterate through our variable lists, applying a new line before each entry prints. Allowing us to pick and choose when to add or remove a new line from our formatted list.

Now, we have cleanly formatted printouts of our two lists, but we can still do more to marry the content together. 

## Pairing the Lists Together

Time for a bit of Python magic. We will use the **zip() method** to package the two lists together and produce tuples until we have exhausted the entries. 

There are a few properties to consider when utilizing the **zip() method**, most importantly the (strict =) argument can be passed directly along with the two iterables (our lists: project_titles and project_descriptions). By default, 'strict' is set to True, meaning that the connected tuples must match 1-for-1, else the program will cause an error. So, if we have 25 titles, we will need to have 25 descriptions available. Otherwise, we will encounter an error.

```Python
project_data = zip(project_titles, project_descriptions)

project_list = list(project_data) # Convert to a list of tuples
```
The first line sets the variable ‘project_data’ to the zip() method and passes in the two lists we created as two arguments separated by a comma. This will produce a set of tuples for each of our entries in the two lists. Afterwards, another variable is set to accept the previous variable passed into the list() function. 

We can then iterate over our list by calling two temporary variables to properly structure our output. The terminal print statement will then produce a ready to copy/paste output, easily incorporated into a regular preparatory workflow process.

```
LogicLink Studio:
Simplify complex logic with LogicLink Studio, a software suite that offers intuitive tools for logical reasoning and analysis.

CodeWave Nexus:
Surf the coding wave with CodeWave Nexus, an integrated coding environment designed to enhance coding productivity and efficiency.

PixelCraft Pro:
Master the art of pixel manipulation with PixelCraft Pro, a comprehensive pixel editing and art creation tool.

ByteSynth Fusion:
Dive into the world of digital synthesis with ByteSynth Fusion, a powerful software synthesizer that unlocks boundless creative possibilities in music production.

```
With this tool in place, we can spend more time preparing for challenging writing tasks, technical interviews with engineers, or any other task the modern technical writer faces everyday. Anything beats the drudge work of formatting a seemingly endless list of data entries.  

[Top](#preparing-with-python-formatting-lists-between-common-apps)