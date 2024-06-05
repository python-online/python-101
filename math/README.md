# Python Math

Python is a powerful programming language with a wide range of applications, including scientific computing and data analysis.

In this guide, we will explore the various mathematical operations and functions available in Python, as well as how to use them effectively.

## Arithmetic Operations

One of the most basic mathematical operations in Python is arithmetic.

Python supports the basic arithmetic operations of + addition, \- subtraction, \* multiplication, and / division, as well as the modulus operator %.

Here's an example of some basic arithmetic in Python:

```python
# Addition
print(2 + 3) # prints 5

# Subtraction
print(5 - 2) # prints 3

# Multiplication
print(2 * 3) # prints 6

# Division
print(6 / 2) # prints 3.0

# Modulus
print(7 % 3) # prints 1
```

In addition to these basic operations, Python also supports the use of parentheses () to control the order of operations, as well as the use of the \*\* operator for exponentiation.

```python
# Parentheses
print((2 + 3) * 4) # prints 20

# Exponentiation
print(2 ** 3) # prints 8
```

## Built-in Functions

Python also includes a number of built-in mathematical functions, such as the math module, which provides access to common mathematical functions such as trigonometric functions, logarithms, and more.

Here's an example of how to use some of the functions in the math module:

```python
import math

# Absolute value
print(math.fabs(-3.14)) # prints 3.14

# Trigonometric functions
print(math.sin(math.pi / 2)) # prints 1.0

# Logarithms
print(math.log10(100)) # prints 2.0
```

In addition to the math module, Python also includes a number of other built-in functions for working with numbers, such as the round() function for rounding a number to a specified number of decimal places, and the int() and float() functions for converting between integers and floating-point numbers.

```python
# Rounding
print(round(3.14159, 2)) # prints 3.14

# Type conversion
print(int(3.14)) # prints 3
print(float(3)) # prints 3.0
```

## NumPy

NumPy is a powerful library for scientific computing in Python.

It provides a wide range of mathematical operations and functions, including support for arrays, matrices, and linear algebra.

Here's an example of how to use NumPy to perform a matrix multiplication:

```python
import numpy as np

# Matrix Multiplication
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])
print(np.dot(A, B))
# prints [[19 22]
# [43 50]]
```

NumPy also provides a wide range of mathematical functions such as trigonometric functions, logarithms, and more, similar to the built-in math module.

```python
# Trigonometric functions
print(np.sin(np.pi / 2)) # prints 1.0

# Logarithms
print(np.log10(100)) # prints 2.
```

## Symbolic Computation

Python also has support for symbolic computation through libraries such as SymPy.

SymPy is a library for symbolic mathematics that allows you to perform algebraic operations, calculus, and other advanced mathematical operations using symbolic expressions.

Here's an example of how to use SymPy to solve an equation:

```python
import sympy

# Solving an equation
x = sympy.Symbol('x')
eq = x**2 - 2*x - 3
sol = sympy.solve(eq, x)
print(sol) # prints [-1, 3]
```

SymPy also provides a wide range of other features such as simplification of expressions, substitution, and differentiation and integration.

```python
# Simplifying an expression
expr = sympy.sin(x)**2 + sympy.cos(x)**2
print(sympy.simplify(expr)) # prints 1

# Substituting a value
expr = x**2 + 2*x + 1
sub = {x: 2}
print(expr.subs(sub)) # prints 9

# Differentiation
f = x**2 + 2*x + 1
df = sympy.diff(f, x)
print(df) # prints 2*x + 2

# Integration
f = x**2
integ = sympy.integrate(f, x)
print(integ) # prints x**3/3
```

## Conclusion

Python is a powerful programming language that provides a wide range of mathematical operations and functions, from basic arithmetic to advanced symbolic computation.

Whether you're working on a scientific project or just need to perform some calculations, Python has everything you need to get the job done.

With the help of built-in functions, modules, and libraries like NumPy and SymPy, you can easily perform complex mathematical operations and analyze your data.
