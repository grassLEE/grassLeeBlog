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

days_to_units()  #Required execution call of new function.
```
The above example demonstrates a basic function in action. Remember, when describing a new function, it will only run when specially called/executed. 

### **Function Parameters:**
Specific information can be passed directly into functions, Python refers to these as *parameters* or *argurments*.

#### Example: 
```Python
calculation_to_units = 24 * 60 * 60
name_of_units = "seconds"


def days_to_units(num_of_days):  #Variable defined within a function.
    print(f"{num_of_days} days are {num_of_days * calculation_to_units}{name_of_units}"{num_of_days * calculation_to_units}{name_of_units}")


days_to_units()
```
Functions are not limited to a single parameter, a secondary... or tertiary parameter can easily be passed into the same function.

#### Example: 
```Python
def days_to_units(num_of_days, custom_msg):
    print(f"{num_of_days} days are {num_of_days * calculation_to_units}{name_of_units}")
    print(custom_msg)


days_to_units(20, "Awesome")  #Requires two inputs.
days_to_units(35, "Neat")  #Requires two inputs.
```
