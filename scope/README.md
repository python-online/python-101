# Python Scope

Python uses a system of scope to determine where a variable can be accessed in a program.

There are two types of scope in Python: global and local.

## Global Scope

A variable that is defined at the top level of a script or module is said to be in global scope.

This means that it can be accessed from anywhere in the script or module, including inside functions.

For example:

```python
x = 5

def my_function():
  print(x)

my_function() # prints 5
```

In this example, the variable x is defined in global scope and can be accessed inside the function my\_function.

## Local Scope

A variable that is defined inside a function is said to be in local scope.

This means that it can only be accessed inside the function in which it is defined.

For example:

```python
def my_function():
  x = 5
  print(x)

my_function() # prints 5
print(x) # raises NameError because x is not defined in global scope
```

In this example, the variable x is defined in local scope and can only be accessed inside the function my\_function.

Attempting to access it outside the function will raise a NameError.

## Scope Hierarchy

If a variable is accessed inside a function and there is a variable with the same name defined in both local and global scope, Python will use the local variable.

For example:

```python
x = 5

def my_function():
  x = 10
  print(x)

my_function() # prints 10
print(x) # prints 5
```

In this example, the function my\_function defines a local variable x with a value of 10.

When the function is called and x is printed, the local variable is used. The global variable with a value of 5 is not affected.

## The keyword global

If a variable is defined in global scope and you need to modify its value inside a function, you can use the global keyword.

For example:

```python
x = 5

def my_function():
  global x
  x = 10

my_function()
print(x) # prints 10
```

In this example, the function my\_function uses the global keyword to specify that it wants to modify the global variable x.

After the function is called, the global variable x has a new value of 10.

## Nested Functions

When a function is defined inside another function, it is said to be a nested function.

Nested functions can access both local and global variables defined in the outer function.

For example:

```python
def outer_function():
  x = 5
  def inner_function():
    print(x)
  inner_function()

outer_function() # prints 5
```

In this example, the inner function inner\_function has access to the local variable x defined in the outer function outer\_function.

## Conclusion

Scope in Python determines where a variable can be accessed in a program.

Variables defined at the top level of a script or module are in global scope and can be accessed from anywhere in the script or module.

Variables defined inside a function are in local scope and can only be accessed inside the function in which they are defined.

The global keyword can be used to specify that a variable in local scope should be treated as a global variable.

The scope hierarchy in Python follows the principle of LEGB (Local, Enclosing, Global, Built-in) , which means that Python will first look for a variable in the local scope, then in the enclosing scope (if the variable is used inside a nested function), then in the global scope, and finally in the built-in scope.

This is important to keep in mind when working with nested functions and variables with the same name.

In summary, understanding scope in Python is important to avoid confusion and errors in your code.

It allows you to control the visibility and accessibility of variables, and to modify global variables when necessary.

By following the rules and principles of scope, you can write cleaner, more organized and well-structured code.
