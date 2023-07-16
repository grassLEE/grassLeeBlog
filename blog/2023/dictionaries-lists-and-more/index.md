# Dictionaries, Lists, and More... in Python

Python offers multiple ways of storing data, including dictionaries, lists, and tuples. To understand the syntax, let's look at a some exmaples to get us started.

A dictionary is denoted with **{curly braces}**, which are designed to hold key value pairs. Such as:

```
dictionary = {"Granny Weatherwax":"witch", "Rincewind":"wizzard", "Magrat":"witch/queen"}
```
Each of our key value pairs are separated by colons and wrapped in quotes... making these entries strings. 

However, keep in mind that a dictionary can hold multiple value types, including integers, lists, and even other dictionaries. 

Let's look at some important functions we can perform with dictionaries:

Python Dictionary Functions:

1. `len(dict)`: Returns the number of key-value pairs in the dictionary.
2. `dict.keys()`: Returns a list of all the keys in the dictionary.
3. `dict.values()`: Returns a list of all the values in the dictionary.
4. `dict.items()`: Returns a list of tuples containing key-value pairs.
5. `dict.get(key, default)`: Returns the value associated with the key. If the key is not found, it returns the default value.
6. `dict.pop(key, default)`: Removes and returns the value associated with the key. If the key is not found, it returns the default value.
7. `dict.popitem()`: Removes and returns an arbitrary key-value pair from the dictionary.
8. `dict.update(other_dict)`: Updates the dictionary with the key-value pairs from another dictionary.
9. `dict.clear()`: Removes all the key-value pairs from the dictionary.

Python List Functions:

1. `len(list)`: Returns the number of elements in the list.
2. `list.append(element)`: Adds an element to the end of the list.
3. `list.extend(iterable)`: Appends elements from an iterable to the end of the list.
4. `list.insert(index, element)`: Inserts an element at the specified index.
5. `list.remove(element)`: Removes the first occurrence of the specified element from the list.
6. `list.pop(index)`: Removes and returns the element at the specified index.
7. `list.index(element)`: Returns the index of the first occurrence of the specified element in the list.
8. `list.count(element)`: Returns the number of occurrences of the specified element in the list.
9. `list.sort()`: Sorts the elements in the list in ascending order.
10. `list.reverse()`: Reverses the order of the elements in the list.
11. `list.copy()`: Returns a shallow copy of the list.

