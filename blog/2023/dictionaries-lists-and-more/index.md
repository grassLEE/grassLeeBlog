# Dictionaries, Lists, and More... in Python

Python offers multiple ways of storing data, including dictionaries, lists, and tuples. To understand the syntax, let's look at some examples to get us started.

### Dictionary

A dictionary is denoted with **{curly braces}**, which are designed to hold key value pairs. Such as:

```
disc_dict = {'Rincewind the Wizzard': 'Wizard', 'Sir Sam Vimes': 'City Watch', 'Nobby Nobs': 'City Watch', 'Queen Magrat': 'Witch'}
```
Each of our key value pairs are separated by colons and wrapped in quotes... making these entries strings. 

However, keep in mind that a dictionary can hold multiple value types, including integers, lists, and even other dictionaries. 

Now that we have some key/value pairs established, we can now explore some of the basic Python functions to retrieve that data.

## Dictionary Functions:

Currently, our dictionary is relatively short, so we can easily spot a character’s name, but that will not always be the case. Fortunately we have some handy functions to retrieve the data. Let’s say we need to identify the value of a specific key?

```
disc_dict.get(‘Sir Sam Vimes’) # first call the dictionary name, then we enter the string we want to query

print(disc_dict.get(‘Sir Sam Vimes’) # to view the data, wrap the function in a print statement

$City Watch # printed output
```
Another handy function comes with our first entry in the list below, title len(). This function performs a count on all the key-value pairs that appear in our dictionary. Again, this is easy to count when the present information is relatively small, but becomes increasingly challenging as the data grows.

Let’s take a look at the len() function in action before we move on to lists and other container types in Python:

```
len(disc_dict) #calls the function, passing in our disc_dict dictionary

print(len(disc_dict) # as with our above example, to view the data we need to call our print function.

$ 4 # printed output representing the number of key/value pairs in our dictionary
```


1. `len(dict)`: This will return the number of key-value pairs within a dictionary.
2. `dict.keys()`: Returns a list of all keys within a dictionary.
3. `dict.values()`: Similar to the above, this function returns a list of all the values within a dictionary.
4. `dict.get(key, default)`: Returns the value associated with the key. If the key is not found, it returns the default value.
5. `dict.update(other_dict)`: Updates the dictionary with the key-value pairs from another dictionary.
6. `dict.clear()`: Removes all the key-value pairs from the dictionary.

### List

A list is constructed with **[square brackets]**, which holds data in a set order, allowing for indexing, and a bevy of other functions. Most importantly, a list in Python is mutable, meaning that new data elements can be inserted without the need to recreate the entire object. 

To start, let’s build a short list similar to our disc_dict. To do so we can simply declare a new variable name and set the value to empty **[square brackets]**. Information can then be typed directly into the list, appearing in multiple ways:


```
disc_list = [('The Color of Magic', 1), ('The Light Fantastic', 2)]

discworld_novels = []
novels = [0]
for novel in novels:
    discworld_novels.append(novels + list(range(1, 42)))

    print(discworld_novels)
```
For the purposes of our short article here, we will be using the simple disc_list option. As you may know, Terry Pratchett wrote over 41 novels for his Discworld fantasy series, and by the looks of it we have quite a few entries to add to our disc_list. 

Let’s take a look at a simple way of appending new values.

```
disc_list = [('The Color of Magic', 1), ('The Light Fantastic', 2)]

disc_list.append(('Equal Rites', 3))
print(disc_list)

$[(‘The Color of Magic’, 1), (‘The Light Fantastic’: 2), (‘Equal Rites’, 3)]
```
Similar to our above example featuring the len() function, we can programmatically count the entries in our disc_list:

```
disc_list = [('The Color of Magic', 1), ('The Light Fantastic', 2)]

disc_list.append(('Equal Rites', 3))

len(disc_list)
print(len(disc_list))

$ 3 
```
There are several more popular functions available in the list below, and countless others across Python and its many libraries, but we have seen today the basic syntax and structure, allowing us to continue to experiment across the language. 

## List Functions:

1. `len(list)`: Returns the number of elements in the list.
2. `list.append(element)`: Adds an element to the end of the list.
3. `list.insert(index, element)`: Inserts an element at the specified index.
4. `list.remove(element)`: Removes the first occurrence of the specified element from the list.
5. `list.index(element)`: Returns the index of the first occurrence of the specified element in the list.
6. `list.reverse()`: Reverses the order of the elements in the list.

In future articles, we will explore some of the fundamentals of **for** and **while** loops, which allows us to iterate over a set of data and perform commands at each instance. 
