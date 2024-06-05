# Python Dictionaries

Python dictionaries are a powerful and versatile data structure for storing and manipulating data.

They are similar to lists in that they store a collection of items, but unlike lists, they use keys and values to access the items instead of indexes.

This guide will cover the basics of working with dictionaries in Python, including creating dictionaries, adding and removing items, and looping through them.

## Creating Dictionaries

The simplest way to create a dictionary is to use curly braces { } and separate the keys and values with colons.

For example:

```python
>>> my_dict = {'apple': 0.5, 'banana': 0.25}
>>> print(my_dict)
{'apple': 0.5, 'banana': 0.25}
```

Alternatively, you can use the built-in dict() function to create a dictionary.

This can be useful when creating a dictionary from a list of key-value pairs:

```python
>>> fruits = [('apple', 0.5), ('banana', 0.25)]
>>> my_dict = dict(fruits)
>>> print(my_dict)
{'apple': 0.5, 'banana': 0.25}
```

## Accessing Dictionary Items

Once you have a dictionary, you can access the items using the keys in square brackets.

For example:

```python
>>> my_dict = {'apple': 0.5, 'banana': 0.25}
>>> print(my_dict['apple'])
0.5
```

If you try to access a key that doesn't exist in the dictionary, you will get a KeyError:

```python
>>> my_dict['orange']
KeyError: 'orange'
```

To avoid this, you can use the get() method, which will return None if the key is not found:

```python
>>> my_dict.get('orange')
None
```

You can also specify a default value to be returned if the key is not found:

```python
>>> my_dict.get('orange', 0)
0
```

## Adding and Removing Items

You can add items to a dictionary by using the keys in square brackets and assigning a value:

```python
>>> my_dict = {'apple': 0.5, 'banana': 0.25}
>>> my_dict['orange'] = 0.75
>>> print(my_dict)
{'apple': 0.5, 'banana': 0.25, 'orange': 0.75}
```

You can also use the update() method to add multiple items at once:

```python
>>> my_dict.update({'pear': 0.3, 'grape': 0.2})
>>> print(my_dict)
{'apple': 0.5, 'banana': 0.25, 'orange': 0.75, 'pear': 0.3, 'grape': 0.2}
```

To remove an item from a dictionary, you can use the pop() method, which will remove the item with the specified key and return its value:

```python
>>> price = my_dict.pop('apple')
>>> print(price)
0.5
>>> print(my_dict)
{'banana': 0.25, 'orange': 0.75, 'pear': 0.3, 'grape': 0.2}
```

You can also use the del keyword to remove an item without returning its value:

```python
>>> del my_dict['orange']
>>> print(my_dict)
{'banana': 0.25, 'pear': 0.3, 'grape': 0.2}
```

Another way to remove items is the clear() method which will remove all items from the dictionary:

```python
>>> my_dict.clear()
>>> print(my_dict)
{}
```

## Looping through Dictionaries

There are several ways to loop through a dictionary, depending on what you need to do with the data.

The keys() method returns a list of all the keys in the dictionary, which you can then use to access the values:

```python
>>> my_dict = {'apple': 0.5, 'banana': 0.25, 'orange': 0.75}
>>> for key in my_dict.keys():
... print(key, my_dict[key])
...
apple 0.5
banana 0.25
orange 0.75
```

The values() method returns a list of all the values in the dictionary:

```python
>>> for value in my_dict.values():
... print(value)
...
0.5
0.25
0.75
```

The items() method returns a list of all the key-value pairs in the dictionary, which you can unpack using the for loop:

```python
>>> for key, value in my_dict.items():
... print(key, value)
...
apple 0.5
banana 0.25
orange 0.75
```

## Dictionary Comprehensions

Dictionary comprehension is a concise way to create a dictionary by applying a function to each item in an iterable.

It has the same syntax as a list comprehension, but with curly braces { } instead of square brackets \[ \].

For example, this list comprehension:

```python
>>> prices = {'apple': 0.5, 'banana': 0.25, 'orange': 0.75}
>>> discounted_prices = {fruit: price * 0.8 for fruit, price in prices.items()}
>>> print(discounted_prices)
{'apple': 0.4, 'banana': 0.2, 'orange': 0.6}
```

You can also include an if statement to filter items in the comprehension:

```python
>>> expensive_fruits = {fruit: price for fruit, price in prices.items() if price > 0.5}
>>> print(expensive_fruits)
{'orange': 0.75}
```

In conclusion, Python dictionaries are a powerful and versatile data structure for storing and manipulating data.

They use keys and values to access items instead of indexes.

It's important to know how to create, access, add and remove items, loop through them and use dictionary comprehension.

With these basic concepts, you'll be well on your way to mastering dictionaries in Python.
