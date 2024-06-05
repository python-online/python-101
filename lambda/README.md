# Python Lambda

Python lambda is a small anonymous function without a name.

It can have any number of arguments but only one expression.

The expression is evaluated and returned when the function is called.

Python lambda functions are useful when we need a small function for a short period of time.

These functions are also called throw-away functions.

## Syntax

The syntax of a Python lambda function is as follows:

```python
lambda arguments: expression
```

For example, the following lambda function takes in two arguments and returns their sum:

```python
lambda x, y: x + y
```

## Using Lambda Functions

Python lambda functions can be used in various ways.

They can be used as an argument to a higher-order function (a function that takes in another function as an argument).

For example, the map() function in Python takes in a function and an iterable as arguments, and applies the function to each element of the iterable.

We can use a lambda function as the function argument to the map() function:

```python
numbers = [1, 2, 3, 4, 5]
squared_numbers = map(lambda x: x**2, numbers)
print(list(squared_numbers))
```

This will print \[1, 4, 9, 16, 25\].

lambda functions can also be used as the key function argument to sorting functions like sorted() and sort().

For example:

```python
words = ["apple", "banana", "cherry", "date"]
sorted_words = sorted(words, key=lambda x: len(x))
print(sorted_words)
```

This will print \['date', 'cherry', 'apple', 'banana'\].

## Advantages

There are several advantages of using lambda functions in Python:

*   They are small and easy to read.
*   They do not clutter the namespace with unnecessary function names.
*   They are useful when we need a function for a short period of time.
*   They can be used as an argument to higher-order functions.

## Limitations

While lambda functions are useful in many cases, there are a few limitations:

*   They can only have one expression. This means that they cannot contain multiple statements.
*   They cannot contain any statements and only have one expression.
*   They are not as powerful as regular Python functions, since they are limited in what they can do.

## Conclusion

Python lambda functions are small, anonymous functions that can be useful when we need a function for a short period of time.

They are easy to read and do not clutter the namespace with unnecessary function names.

They can be used as an argument to higher-order functions, and are useful in situations where a function is needed for a short period of time.

However, they have limitations, such as being limited to one expression and not being as powerful as regular Python functions.
