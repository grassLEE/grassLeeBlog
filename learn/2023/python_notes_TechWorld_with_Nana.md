## Python Tutorial: TechWorld with Nana
[Full Video](https://www.youtube.com/watch?v=t8pPdKYpowI&t=1169s)
### Strings & Numbers:  

**Data Types:**  
Text = **"String" or 'String'**  
*Python accepts both 'single' and "double" quotes.*  

Numbers = **Two types**    
Integers = **whole numbers:** 20, 1, -20, etc.  
Floating point = **decimals:** $19.99

### **Working with Numbers:** 

``` Python
print(20 * 24 * 60)
```
**Functional Output:** Mathematical Calculations = 28800

### **String Concatenation:**  
Definition: *"The action of linking things together in a series."*    
Python utilizes the **(+) symbol** to combine multiple strings together.  

```Python
print("20 days are" + xxx + "minutes")
```
Plugging a number (xxx) directly will result in an error.
**System expects: 'str', but got 'int'.**  

**Conversion tool** = **str( ):** Allows Python to interpret this (xxx) 'int' as the expected 'str'. 

```Python
print("20 days are" + str(50) + "minutes")
```

**Functional Output:** 20 days are50minutes  

Correct the spacing error by adding additional spacing in the print command:

```Python
print("20 days are " + str(50) " minutes")
```

**Functional Output:** 20 days are 50 minutes  
This syntax is still clunky and can be hard to remember. Luckily, Python 3 (and above) offers a robust shortcut:
```Python
print(f"20 days are {50} minutes")
```
Definition: *f* stands for *formatting,* allowing Python to automatically recognize non-text values. While the curly braces { } avoid the need for the otherwise cumbersome (+) symbol notation. 

### **Variables:**
Python treats variables as *containers* that store values. Moreover, Python is dynamically typed. [Differences between dynamic vs static](https://www.educative.io/answers/what-is-dynamic-typing) can be found here.  

**Naming Convention:** A generally agreed upon scheme for naming things. Our example below utilizes a lowercase style separated by underscores, but also support camelCase style. Python encourages the use of descriptive variable names. 

#### Example: 
```Python
calculation_to_seconds = 24 * 60 * 60
print(f"20 days are {calculation_to_seconds} seconds.")
```

### **Functions:**
Unique blocks of code used to reduce repeating logic. Python defines a function using the keyword *def*.

#### Example: 
```Python
calculation_to_units = 24 * 60 * 60
name_of_units = "seconds"

def days_to_units():
    print(f"20 days are {20 * calculation_to_units}{name_of_units}")

days_to_units()  # Required execution call of new function.
```
The above example demonstrates a basic function in action. Remember, when describing a new function, it will only run when specially called/executed. 

### **Function Parameters:**
Specific information can be passed directly into functions, Python refers to these as *parameters* or *argurments*.

#### Example: 
```Python
calculation_to_units = 24 * 60 * 60
name_of_units = "seconds"


def days_to_units(num_of_days):  # Variable defined within a function.
    print(f"{num_of_days} days are {num_of_days * calculation_to_units}{name_of_units}")


days_to_units()
```
Functions are not limited to a single parameter, a secondary... or tertiary parameter can easily be passed into the same function.

#### Example: 
```Python
def days_to_units(num_of_days, custom_msg):
    print(f"{num_of_days} days are {num_of_days * calculation_to_units}{name_of_units}")
    print(custom_msg)


days_to_units(20, "Awesome")  # Requires two inputs.
days_to_units(35, "Neat")  # Requires two inputs.
```

### **Scope:**
Variable scope refers to where the variable is located.  
**Global Scope** = Variables available from within any scope.  
**Local Scope** = Variables created inside a specific function. Local variables can only be used inside a specific function.
```Python
def scope_check(num_of_days):
    my_var = "variable inside a function."
    print(name_of_unit)
    print(num_of_days)
    print(my_var)

scope_check()  # Must pass parameter.
```

### **Accepting User Input:**
**Python Built-in Function** = *input()*. This syntax prompts a user for an input. Python will stop executing when it comes to that user-input.
**Expression** = An instruction that combines values and operators, evaluating down to a single value.
```Python
user_input = input("Hey user, enter number of days and I will convert it to hours.\n")
```
### **Function with Return Value:**
Must return value in the function: 
#### Example: 
```Python 
def days_to_units(num_of_days):
    return f"{num_of_days} days are {num_of_days * calc_to_units}{name_of_unit}"
```
The above example has two key factors that must be considered:
1. Changing the print( ) keyword to return. This will stop our logic from immediately printing input data. 
2. Currently, the num_of_days variable is treated as a string, but it must be converted (or cast) with int( ).
    - Same as the previously reviewed str( ) built-in Python function. 

### **Using User Input Data:**
#### Example: 
```Python
user_input = input("hey User,...")  # Always treats value as a string, not a number.
```
### **Casting:**
#### Example:
```Python
user_input = input("hey User,...")
int(user_input)  # Built-in Python function.
```
**Int( )** = A built-in Python function. Converts value in 'int' (whole numbers). Int number is returned by the function. 

### **Conditionals (if/else) and Boolean Data Type:**
Validate user inputs, help avoid and handle improper errors. Such as entries that don't make sense, or crash the program, or present potential security risks.

### **Conditionals:**
Expressions that calculate to either true or false:
```Python
equals: a == b
not equals: a != b
less than: a < b
less than or equal: a <= b
greater than: a > b
greater than or equal: a >= b
```
### **If/Else Statements:**
#### Example:
```Python
def days_to_units(num_of_days):
    if num_of_days > 0:  # Condition that is either true or false.
        return f"{num_of_days} days are {...}"
    else:
        return "You have entered an invalid number."
```

### **Logic to Define Negative Values and Zero:**
True and false values are represented as a boolean. These are allowed to be nested inside of other function calls.  

Note: 
- ( = ) is used to assign value to a variable
- ( == ) is used as for equality of value checks. 

#### Example:
```Python
def days_to_units(num_of_days):
    if num_of_days > 0:
        return f"{num_of_days} days are {num_of_days * calculation_to_units}{name_of_units}"
    elif num_of_days == 0:  # Condition 
        return "Entered an invalid number: 0."
    else:  # Called without conditions
        return "Entered an invalid number: negative value."
```
### **Protect Against Strings and Other Non-Int Value Inputs:**
### Example:
```Python
user_input = input("Hey User, enter a value and I will convert it!")
        
        if user_input.isdigit():  # .isdigit - built-in Python function used to check for positive integers.
            user_input_num = int(user_input)
            calculated_value = days_to_units(user_input_num)
            print(calculated_value)
        else:
            print("Input is not valid.")
```
### **Cleaning Up Code:**
Define the previous if/else statement in its own definition. 

#### Example:
```Python
def validate_and_execute():
    if user_input.isdigit():
        user_input.num = int(user_input)
        calculate_value = days_to_units(user_input_num)
        print(calculated.value)
    else:
        print("Input is not valid")


user.input = input("Hey user...")
validate_and_execute()  # When declaring a new definition, must execute it in the file.
```

### **Nested if/else Statements:**
#### Example: Perform all validation in one definition

```Python
def validate_and_execute():
    if user_input.isdigit():
        user_input_num = int(user_input)
        if user_input_num > 0:
            calculated_value = days_to_units(user_input_num)
            print(calculated_value)
        elif user_input_number == 0:
            print("Input is not positive.")
    else:
        print("Input is not valid.")
```

### **Error Handling with try/except:**
#### try/except:
- The try block: tests a block of code for errors.  
- The except block: catches errors and handles them through programming logic.

### **While Loops:**
#### Looping:
- execute logic multiple times.
- Python has two (2) types of loops: *for* and *while*
- Conditions are used to evaluate true/false and most commonly found in "if statements and loops"  

**While** loop: execute a set of statements as long as the condition is true.
#### Example:
```Python
while True  # Requires capital letter. Will continuously run.
    user_input = input("Hey user...\n")  # \n used to create a new line for the user.
    validate_and_execute()
```

**For** loop: used for iterating over a sequence, like a list. Also used to so the program can execute something for each item represented in a list.
#### Example:
```Python
user_input = ""
while user_input != "exit":
    user_input = input("Hey user...")
    for num_of_days_element in user_input.split(", "):
        validate_and_execute()
```
**.split:** built-in Python function to convert string into list. Transforms "10 22 30 100" to [10, 22, 30, 100] .split uses spaces as default separator. The (", ") in the above example is used to allow input separations by comma from the user. 

### **Basic List Operations:**
**Lists:** used to store multiple items in a single variable. Represented with [ ], such as: [10, 22, 30, 100].
**Operations:**
- create list
- add item to a list
- remove an item from the list
- change items in the list
- access items in the list

#### Example:
```Python
my_list = ["Jan", "Feb", "Mar"]
my_list[0]  # Python lists start at 0. 
print(my_list[0])  # Prints first entry from my_list.
```

### **Adding & Removing Entries from a List:**
Python offers additional built-in functionality to easily add and remove entries from a list. 
#### Example:
```Python
my_list = ["Jan", "Feb", "Mar"]
my_list.append("Apr")
print(my_list)  # Output: ["Jan", "Feb", "Mar", "Apr"]

my_list = ["Jan", "Feb", "Mar", "Apr"]
my_list.remove("Jan")
print(my_list)  # Output: ["Feb", "Mar", "Apr"]
```
### **Sets:**
Another built-in function of Python are Sets. Similar to Lists, Sets are used to store multiple items of data. However, with several key differences, such as, Sets do **NOT** allow for duplicate values.

#### Example:
```Python
for num_of_days_element in set(user_input.split(", ")):  # The .split built-in function converts a List into a Set. 
    validate_and_execute()
```
### **Nested Function Execution:**
#### Example: 
```Python
list_of_days = user_input.split(", ")
print(list_of_days)
print(set(list_of_days))

print(type(list_of_types))
print(type(set(list_of_types)))
```
#### Example: *user input/output*
**Input:** 10, 10, 20, 15, 55
Python's output will follow the sequence from inner value to outer value. 
**Output:**   
['10', '10', '20', '15', '55']  
{'10', '20', '55', '15'}  
<class 'list'>  
<class 'set'>  

### **Nested Function Execution:** *Continued*
```Python
print(type(set(list_of_days)))
```
1. set(list_of_days)
    - **Input:** User input array
    - **Output:** Returns the converted set
2. type (return_value_of_previous_function)
    - **Input:** The converted set
    - **Output:** Returns the datatype of the set
3. print(return_value_of_previous_function)
    - **Input:** The data type
    - **Output:** Prints the value to console

### **Basic Set Operations & Syntax:**
Set Operations: 
- Create a set
- Access items (only via loop)
- Add item to a set
- Remove an item from a set

Items in a set do **NOT** have a defined order (as they do in a list), items cannot be referred to by index (as performed with a list), and items cannot be changed - only added/removed. 
#### Example:
```Python
my_set = {"Jan", "Feb", "Mar"}
for element in my_set:
    print(element)
```
#### Example: Add Elements to a Set
```Python
my_set.add("Apr")
print(my_set)
```
#### Example: Remove Elements from a Set
```Python
my_set.remove("Jan")
print(my_set)
```
### **Built-In Functions:**
**print( )** -> prints a standard output  
**input( )** -> Asks user for an input
**Set( )** -> returns a new set  
**int( )** -> converts value to integer string  

#### Direct Value Functions
Such as the previously mentioned **.split( )**  
Own list of functions dependent on that data type: string, list, and other function types. 

### **Dictionary Data Type:**
**Dictionary:** Used to store values in key:value pairs. A collection which doesn't allow for duplicate values. Items can be accessed via key name.

#### Example:
```Python
my_dictionary = {
    "days": 20,
    "unit": "hours",
}
```
#### Example:
```Python
days_and_unit_dictionary = {"days":days_to_unit[0]}  # Accessing items in a list via index - first item is 0.
```

**Accessing Dictionary Element/Entry:**
```Python
user_input_number = int(days_and_unit_dictionary["days"])
```

### List vs Dictionary:
#### Example: List
```Python
my_list = ["20", "30", "100"]
print(my_list[0])  # prints value of 20
```

#### Example: Dictionary
```Python
my_dictionary = {"days":20, "unit":"hours"}
print(my_dictionary["days"])  # print value of 20
```

### **Import Statements:**
```Python
import Django  # takes all functions
OR
from filename import validate_and_execute  # Specific function from a module
```
The entire module import requires specific references in the function. Python supports more than one function utilizing 'from filename function'. 
#### Example:
```Python
from helperNana import validate_and_execute, user_input_message
```
Elements/logic from another file are called definitions. Longer file names can be shortened with:
#### Example:
```Python
import filename as h  # then needs h. ref at all points in the logic
```
### **Built-In Python Modules:**
DateTime module - useful functions for working with dates.  
OS module - operating system functions  
logging module - error messages and warnings.  

### **Object Oriented Programming:**  

#### Classes and Methods:  

**Classes:** function as an object container. It must have an ```__init__( )``` function. This is executed automatically whenever creating the object from the class. The ```__init__( )``` constructor will autofill 'self'. 

**Methods:** These are functions that belong to an object. See example below.

#### Example: Creating a Class
```Python
class User: 
    def __init__(self, email, name, password, job_title)
        self.email = email
        self.name = name
        self.password = password
        self.job_title = job_title

    def change_password(self, new_password):
        self.password = new_password
    
    def change_title(self, new_job_title):
        self.job_title = new_job_title

    def get_user_infor(self):
        print(f"User {self.name} currently works as a {self.job_title} and can be reached at {self.email}")


app_user_1 = User("J@j.com", "J G", "pwd", "DM")
app_user_1.get_user_infor()

app_user_1.change_job_title("Dev")
app_user_1.get_user_infor()

app_user_2 = User("a@a.com", "A A", "pwd1", "PM")
```

[Top](##python-tutorial:-techworld-with-nana)
