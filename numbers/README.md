# Python Numbers

Python supports several types of numeric data types: int, float, and complex. These numeric types are used to store numerical values.

In this guide, we will take a closer look at each of these types and learn how to work with them in Python.

## Integers (int)

Integers are whole numbers, positive or negative, without a decimal point. They are represented in Python by the int data type.

For example, the number 1 is an integer, and it is written as such in Python:

```python
x = 1

print(type(x)) # Output: <class 'int'>
```

In Python, integers can be of any size and do not have a maximum or minimum value.

You can perform mathematical operations on integers, such as + addition, \- subtraction, \* multiplication, and / division, using the standard mathematical operators.

```python
x = 5
y = 2

print(x + y) # Output: 7
print(x - y) # Output: 3
print(x * y) # Output: 10
print(x / y) # Output: 2.5
```

Note that when two integers are divided in Python 3, the result is always a float.

If you want to perform integer division, you can use the // operator.

```python
print(x // y) # Output: 2
```

## Floats

Floats are numbers with a decimal point. They are represented in Python by the float data type.

For example, the number 1.0 is a float, and it is written as such in Python:

```python
x = 1.0

print(type(x)) # Output: <class 'float'>
```

You can perform mathematical operations on floats just like integers, using the standard mathematical operators.

```python
x = 5.0
y = 2.0

print(x + y) # Output: 7.0
print(x - y) # Output: 3.0
print(x * y) # Output: 10.0
print(x / y) # Output: 2.5
```

## Complex Numbers

Complex numbers are numbers with both a real and an imaginary part. They are represented in Python by the complex data type. The imaginary part is represented by the letter j in Python.

For example, the number 1+2j is a complex number, and it is written as such in Python:

```python
x = 1 + 2j

print(type(x)) # Output: <class 'complex'>
```

You can perform mathematical operations on complex numbers just like integers and floats, using the standard mathematical operators.

```python
x = 5 + 3j
y = 2 + 4j

print(x + y) # Output: (7+7j)
print(x - y) # Output: (3-j)
print(x * y) # Output: (-2+22j)
print(x / y) # Output: (0.6-0.2j)
```

## Conversion between data types

It is possible to convert a number from one data type to another using the built-in functions int(), float(), and complex().

```python
x = 1
y = 2.5
z = 1 + 2j

print(int(y)) # Output: 2
print(float(x)) # Output: 1.0
print(complex(x)) # Output: (1+0j)
```

It is important to note that when converting a float to an integer, the decimal part of the number will be truncated, not rounded.

Also, when converting a complex number to a float or an int, the imaginary part will be dropped.

```python
x = 5.6
print(int(x)) # Output: 5

y = 2 + 3j
print(float(y)) # TypeError: can't convert complex to float
```

## Conclusion

In this guide, we have discussed the three numeric data types in Python: int, float, and complex. We have also learned how to perform mathematical operations on these data types and how to convert between them using built-in functions.

Understanding these data types and how to work with them is crucial for any Python developer, as they are used in various applications, from basic calculations to advanced numerical computing.
