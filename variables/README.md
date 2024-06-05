# Python Variables

In programming, a variable is a container that holds a value. In Python, a variable is a name that is assigned to a value.

Variables are used to store data and perform operations on them. In this guide, we will cover the basics of creating and using variables in Python.

## Creating Variables

In Python, variables are created when a value is assigned to a name. The assignment operator \= is used to assign a value to a variable.

The variable name can be any combination of letters, numbers, and underscores, but it cannot start with a number.

Here is an example of creating a variable in Python:

```python
x = 5
```

In this example, the variable x is assigned the value of 5.

## Assigning Values to Variables

After a variable is created, you can assign a new value to it at any time. The new value will overwrite the previous value.

Here is an example of reassigning a value to a variable:

```python
x = 5
x = 10
```

In this example, the value of x is first set to 5, and then it is overwritten with the value of 10.

## Variable Naming Conventions

When naming variables in Python, it is important to follow some conventions to make your code more readable.

Here are some guidelines to follow when naming variables:

*   Variable names should be descriptive and should reflect the value they hold.
*   Variable names should be in lowercase, with words separated by underscores.
*   Variable names should not contain spaces.
*   Variable names should not start with a number.
*   Variable names should not contain any special characters except for the underscore \_.

Here are some examples of good variable names:

```python
student_name
employee_age
product_price
```

## Variable Types

In Python, variables can hold different types of values.

The most common types of values that variables can hold are:

*   Numbers (int and float)
*   Strings
*   Booleans

Here are some examples of variables of different types:

```python
x = 5
y = 3.14
name = "John Doe"
is_student = True
```

In the above example, x is an integer, y is a float, name is a string, and is\_student is a boolean.

## Variable Scope

The scope of a variable refers to the parts of the program where the variable can be accessed.

In Python, a variable declared inside a function is only accessible within that function, and a variable declared outside a function is accessible throughout the program.

Here is an example of variable scope:

```python
x = 5 # Global variable

def my_function():
  y = 10 # Local variable
  print(x)
  print(y)

my_function()
  print(x)
  print(y) # This will give an error because y is a local variable and is not accessible outside the function
```

In this example, x is a global variable and can be accessed both inside and outside the function. y is a local variable and can only be accessed within the function.

## Many Values to Multiple Variables

In Python, you can assign multiple values to multiple variables in one line of code. This is known as unpacking and it is done using the assignment operator \= and a tuple or a list of values.

Here is an example of unpacking a tuple:

```python
x, y, z = (1, 2, 3)
print(x) # Output: 1
print(y) # Output: 2
print(z) # Output: 3
```

In this example, the values 1, 2, and 3 are assigned to the variables x, y, and z respectively.

Here is an example of unpacking a list:

```python
a, b, c = [4, 5, 6]
print(a) # Output: 4
print(b) # Output: 5
print(c) # Output: 6
```

You can also use unpacking to swap the values of two variables without using a temporary variable:

```python
x = 10
y = 20
x, y = y, x
print(x) # Output: 20
print(y) # Output: 10
```

You can also unpack a string, but you have to split the string first.

```python
string = "Hello World"
a, b, c, d, e, f, g, h, i, j, k = string.split()
print(a) # Output: Hello
print(b) # Output: World
```

It's important to note that the number of variables must match the number of values being unpacked.

If the number of variables does not match the number of values, you will get a ValueError:

```python
x, y = (1, 2, 3) # This will raise a ValueError because there are 3 values and only 2 variables.
```

Unpacking can be very useful in situations where you need to assign multiple values to multiple variables quickly and efficiently. It can make your code more readable and concise.

## Outputting Variables

Outputting variables in Python is a simple task that can be done using the print() function. The print() function takes one or more arguments and prints them to the console or the output screen.

Here is an example of using the print() function to output a variable:

```python
x = 10
print(x) # Output: 10
```

In this example, the variable x is assigned the value 10 and then passed as an argument to the print() function. The output will be 10.

You can also use the print() function to output multiple variables at once by separating them with a comma:

```python
x = 10
y = 20
print(x, y) # Output: 10 20
```

You can also include text and other characters in the output by including them as string literals or variables within the print() function:

```python
x = 10
y = 20
print("The value of x is", x, "and the value of y is", y) 
# Output: The value of x is 10 and the value of y is 20
```

You can also use the format() method of strings to create a more readable output.

```python
x = 10
y = 20
print("The value of x is {} and the value of y is {}".format(x, y))
# Output: The value of x is 10 and the value of y is 20
```

You can also use f-strings(formatted string literals) if you are using python 3.6 or later.

```python
x = 10
y = 20
print(f"The value of x is {x} and the value of y is {y}")
# Output: The value of x is 10 and the value of y is 20
```

In addition to the print() function, you can also output variables using the input() function, which is used to get input from the user. The input() function returns the input as a string, so you may need to convert it to a different data type if needed.

Overall, outputting variables in Python is a simple task that can be done using the print() function. You can use it to output a single variable or multiple variables at once, and you can also include text and other characters in the output for better readability.

## Global Variables

In Python, a variable declared outside of a function or class is considered a global variable. Global variables can be accessed from anywhere in the code, including inside functions and classes.

Here is an example of a global variable:

```python
x = 10 # Global variable

def my_function():
  print(x) # Output: 10

my_function()
```

In this example, the variable x is declared outside of the my\_function() function and can be accessed inside the function without any issues.

However, if you try to modify a global variable inside a function without using the global keyword, Python will create a new local variable with the same name instead of modifying the global variable.

```python
x = 10 # Global variable

def my_function():
  x = 20 # Local variable
  print(x) # Output: 20

my_function()
  print(x) # Output: 10
```

Here, inside the function, x is assigned a new value of 20, but it does not change the global variable.

To modify a global variable inside a function, you need to use the global keyword:

```python
x = 10 # Global variable

def my_function():
  global x
  x = 20
  print(x) # Output: 20

my_function()
  print(x) # Output: 20
```

In this example, the global x statement tells Python that the x variable inside the function is the same as the global x variable, and any changes made to it will also be made to the global variable.

It's generally not recommended to use global variables in your code because it can make the code harder to understand and harder to debug. Instead, try to use local variables and pass them as arguments to functions. However, there are some cases when global variables are useful, such as when you need to share data between functions or when you need to keep track of a value that is used throughout the entire program.

In summary, global variables in Python are variables declared outside of a function or class that can be accessed from anywhere in the code. To modify a global variable inside a function, you need to use the global keyword, but it's generally not recommended to use global variables in your code because it can make the code harder to understand and harder to debug.

## Conclusion

In this guide, we have covered the basics of creating and using variables in Python. Variables are an essential part of programming and understanding how to use them correctly is essential for writing efficient and readable code. Remember to follow the naming conventions and understand the scope of the variables to avoid any confusion or errors in your code.

It's also important to note that Python is a dynamically typed language, which means that the type of a variable can change based on the value it holds. This is different from a statically typed language, where the type of a variable must be explicitly defined and cannot change.

In addition to the basic types we covered earlier, Python also has several built-in data structures such as lists, dictionaries, and tuples that can hold multiple values. These data structures provide powerful ways to organize and manipulate data in your programs.

Lastly, it's important to keep in mind that variables are just one part of the bigger picture of programming. In order to write more complex and powerful programs, you will need to learn about other concepts such as control flow, functions, and modules.

Overall, variables are a fundamental concept in Python and understanding how to use them is essential to becoming a proficient programmer. Practice and experimenting with different types of variables and data structures will help solidify your understanding and improve your skills.
