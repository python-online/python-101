# Python Data Types

Python is a powerful and versatile programming language that provides a wide range of data types to work with.

Understanding the different data types available in Python is essential for writing efficient and effective code.

In this guide, we will take a closer look at the most commonly used data types in Python and how to work with them.

## Numbers

Python supports three different types of numbers: integers, floating-point numbers, and complex numbers.

Integers are whole numbers, such as 1, 2, or \-3. They can be created by simply typing the number without a decimal point.

For example:

```python
x = 5
print(type(x))
# Output: <class 'int'>
```

Floating-point numbers are numbers with a decimal point, such as 3.14 or \-2.5.

They can be created by typing the number with a decimal point.

For example:

```python
y = 3.14
print(type(y))
# Output: <class 'float'>
```

Complex numbers are numbers with both a real and imaginary component, such as 3 + 4j.

They can be created using the complex() function.

For example:

```python
z = complex(3, 4)
print(type(z))
# Output: <class 'complex'>
```

## Strings

A string is a sequence of characters, such as "hello" or "Python is fun!".

They can be created by enclosing characters in single or double quotes.

For example:

```python
a = "Hello"
b = 'Python is fun!'
print(type(a))
print(type(b))
# Output: <class 'str'>
# Output: <class 'str'>
```

You can also use the str() function to convert other data types to strings.

For example:

```python
c = str(123)
print(type(c))
# Output: <class 'str'>
```

## Lists

A list is a collection of items, which can be of any data type.

Lists are enclosed in square brackets \[ \] and the items are separated by commas.

For example:

```python
fruits = ['apple', 'banana', 'mango']
print(type(fruits))
# Output: <class 'list'>
```

You can access individual elements of a list by specifying the index of the element in square brackets.

For example:

```python
print(fruits[0])
# Output: 'apple'
```

You can also use negative indexing to access elements from the end of the list.

For example:

```python
print(fruits[-1])
# Output: 'mango'
```

## Tuples

A tuple is similar to a list, but it is enclosed in parentheses and the items are separated by commas.

Once created, the items in a tuple cannot be modified, unlike lists.

For example:

```python
colors = ('red', 'green', 'blue')
print(type(colors))
# Output: <class 'tuple'>
```

You can access individual elements of a tuple by specifying the index of the element in square brackets, just like with lists.

For example:

```python
print(colors[1])
# Output: 'green'
```

## Dictionaries

A dictionary is a collection of key-value pairs, where each key is unique.

Dictionaries are enclosed in curly braces { } and the items are separated by commas.

The keys and values are separated by a colon.

For example:

```python
person = {'name': 'John', 'age': 30, 'gender': 'male'}
print(type(person))
# Output: <class 'dict'>
```

You can access individual values of a dictionary by specifying the key in square brackets.

For example:

```python
print(person['name'])
# Output: 'John'
```

You can also use the get() method to access values, which will return None if the key does not exist, instead of raising an error.

For example:

```python
print(person.get('address'))
# Output: None
```

## Sets

A set is a collection of unique items, similar to a list or tuple, but with no order and no duplicate values.

Sets are enclosed in curly braces and the items are separated by commas.

For example:

```python
numbers = {1, 2, 3, 3, 4}
print(type(numbers))
# Output: <class 'set'>
```

You can also create a set using the set() function.

For example:

```python
numbers = set([1, 2, 3, 3, 4])
print(type(numbers))
# Output: <class 'set'>
```

## Booleans

A Boolean is a data type that can have one of two values: True or False.

Booleans are often used in conditional statements to check if a certain condition is met.

For example:

```python
is_student = True
print(type(is_student))
# Output: <class 'bool'>
```

In conclusion, understanding the different data types in Python is essential for writing efficient and effective code.

This guide covered the most commonly used data types in Python, including numbers, strings, lists, tuples, dictionaries, sets, and Booleans.

With this knowledge, you will be able to choose the appropriate data type for your specific needs and work with them effectively.
