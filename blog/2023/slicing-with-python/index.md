# Slicing Objects: How to Target Data in Python

When our program only demands a specific element from a list, we can use basic indexing, such as   

```Python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
my_list[2]
# returns 3
```
However, when we need to grab entire sections of a list, or filter through specific entries, Python offers *slicing*. The syntax for slicing is quite simple: first, we indicate our starting position, next, we indicate our stop point (keep in mind Python’s non-inclusive nature), and finally, we establish a *step*. The step defines the increment that our program will skip between values.  

## Example: Basic Structure:

```Python
my_list[0:11:2] # First position ‘0’ begins at the start of the list. Second position ‘11’ ends our list at the last value. The last position, our step, ‘2’ skips every other value in our list.
# returns: [0, 2, 4, 6, 8, 10] 

slice[a:b:c] # a=start, b=end, c=step– the increment between values.
```
## Reverse Syntax
In addition to the basic syntax, slicing also supports reversing. This is performed simply with the use of a negative integer. Just as indexing functions with a negative integer, such as -1, returns the last item from our list. Python allows for our entire list to be returned to us, without changing the actual list itself, in reverse order.  

```Python
my_list[::-1] # [10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
``` 
But that is only the beginning of what slicing has to offer. Let’s see how Python can introduce new data into and remove data from a mutable sequence with slicing.

## Assigning to Slices

Python can modify, retrieve, and delete information in place from a list using slice notation. Setting slice notation at the left-hand of our expression allows us to change values and remove specific values via a delete statement. The below examples explore these concepts in more detail.

### Examples:

```Python
# Example 1
k = list(range(10)) # operator to set ‘k’ to a list from 0 - 9
print(k) # print: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(len(k)) # 10

# Example 2
k[2:5] = [20, 30]  # k[2:5] specifies the values ‘2 - 4’ and then sets the values to ‘20 - 30’.
print(k) # prints: [0, 1, 20, 30, 5, 6, 7, 8, 9] 
print(len(k)) # 9

# Example 3
del k[5:7] 
print(k) # prints: [0, 1, 20, 30, 5, 8, 9]

# Example 4
k[3::2] = [11, 22]
print(k) # prints: [0, 1, 20, 11, 5, 22, 9]
```

Did you notice that our second example actually does more than just replace the values from 2 through 4? It also removes a value, reducing our total list from 10 items, down to 9 items.
We can see this in the output totals from our **print(len(k))** expressions at the end of the first two examples.  

The **del** function with slicing, as we see in the third example, provides us the ability to pull a range of values from our list. Targeting the 5th item from our list, 6 and extending to the 7th item, 8. Keep in mind, Python maintains its non-inclusive syntax, meaning the end value will not be included in our delete statement. 

Our last example appears to break the normal syntax, but is actually just a little more complex. The slice, **k[3::2]**, begins at the third place, in our case ‘30’ and spans the entire list. Keep in mind, an empty **:** communicates to the Python Interpreter that we are moving to our ‘step’ section and including the whole list. Afterwards, we establish our step between the items, in this case we are going to skip every other entry.

## Common Error with Assignments

Whenever we are attempting to replace an iterable’s data, it is important to remember that a new assignment can only be replaced with another iterable object–-otherwise we will encounter an error. The example below demonstrates the error code, including a try/except statement.

### Examples:

 ```
# Example 1
k[2:5] = 100
"""Traceback (most recent call last)
TypeError: can only assign an iterable. When the target of the assignment is a slice, the right-hand side must be an iterable object, even if just one item."""

# Example 2
try:
    k[2:5] = 100
except TypeError:
    print(“Value on the right-hand side must be an iterable”)  

# Example 3
k[2:5] = [100] 
print(k) # [0, 1, 100, 22, 9]
```

The first example shows our expected error code, returning a ‘TypeError,’ which crashes our program. This is because slicing is unable to handle non-iterables, such as the integer, 100. 

We can see in the second example, the same slicing notation is expressed, but now wrapped within a try/except statement. This will prevent our program from crashing when attempting an unsupported operation. However, we still have not made any changes to our list. 

However, the fix is quite easy, simply wrap the integer inside square brackets, turning the raw number into an iterable. Our final print statement confirms the addition of the new value, 100. 

[Top](#slicing-objects-how-to-target-data-in-python)