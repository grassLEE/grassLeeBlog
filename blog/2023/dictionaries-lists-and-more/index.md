# Dictionaries, Lists, and More... in Python

Python offers multiple ways of storing data, including dictionaries, lists, and tuples. To understand the syntax, let's look at a some exmaples to get us started.

### Dictionary

A dictionary is denoted with **{curly braces}**, which are designed to hold key value pairs. Such as:

```
Discworld_People = {"City Watch": "Sir Sam Vimes", "Witch": "Granny Weatherwax", "Witch": "Queen Magrat", "City Watch": "Captain Carrot", "Wizard": "Rincewind the Wizzard"}
```
Each of our key value pairs are separated by colons and wrapped in quotes... making these entries strings. 

However, keep in mind that a dictionary can hold multiple value types, including integers, lists, and even other dictionaries. 

Let's look at some important functions we can perform with a Python dictionary and then we can explore some examples with out above Discworld_People dictionary.

## Dictionary Functions:

1. `len(dict)`: This will return the number of key-value pairs within a dictionary.
2. `dict.keys()`: Returns a list of all keys within a dictionary.
3. `dict.values()`: Similar to the above, this function returns a list of all the values within a dictionary.
4. `dict.get(key, default)`: Returns the value associated with the key. If the key is not found, it returns the default value.
5. `dict.update(other_dict)`: Updates the dictionary with the key-value pairs from another dictionary.
6. `dict.clear()`: Removes all the key-value pairs from the dictionary.

```
len(Discworld_People)
```

### List

A list is constructed with **[square brackets]**, which holds data in a set order, allowing for indexing, and a bevy of other functions.

```
Discworld_novels = [('The Color of Magic, 1), ('The Light Fantastic, 2)]
```

## List Functions:

1. `len(list)`: Returns the number of elements in the list.
2. `list.append(element)`: Adds an element to the end of the list.
3. `list.insert(index, element)`: Inserts an element at the specified index.
4. `list.remove(element)`: Removes the first occurrence of the specified element from the list.
5. `list.index(element)`: Returns the index of the first occurrence of the specified element in the list.
6. `list.reverse()`: Reverses the order of the elements in the list.

