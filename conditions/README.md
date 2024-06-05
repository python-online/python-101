# Python Conditions and If statements

In programming, a condition is a statement that determines whether a certain block of code should be executed or not.

Python, like many other programming languages, has a set of built-in conditions and control structures that allow developers to write code that can make decisions based on certain conditions.

One of the most basic and commonly used control structures in Python is the if statement.

In this article, we will explore the basics of Python conditions and if statements, including how to write and use them in your code.

We will also look at some examples of how they can be used in real-world situations to add logic and control to your programs.

## Elif

In Python, elif is a shorthand for "else if" and is used in conjunction with the if statement.

The elif statement allows you to specify additional conditions to check if the initial if statement is false.

The syntax for an elif statement is as follows:

```python
if condition1:
  # code to execute if condition1 is true
elif condition2:
  # code to execute if condition1 is false and condition2 is true
```

When the if statement is executed, the interpreter first checks the condition specified in the if statement.

If the condition is true, the code block following the if statement is executed.

If the condition is false, the interpreter then checks the condition specified in the first elif statement.

If that condition is true, the code block following the elif statement is executed.

You can have as many elif statements as you need and you can chain them together after the if statement.

It will check the conditions from top to bottom and as soon as it finds the true condition it executes the block and exit the if-elif block.

```python
if condition1:
  # code to execute if condition1 is true
elif condition2:
  # code to execute if condition1 is false and condition2 is true
elif condition3:
  # code to execute if condition1 and condition2 are false and condition3 is true
```

It's important to note that once a true condition is found and its corresponding code block is executed, the interpreter will not check any of the remaining conditions in the elif statements.

This is because the elif statement is used to add an additional level of conditional branching to the if statement, rather than providing multiple options for code execution.

## Else

In Python, the else statement is used in conjunction with the if statement to specify a block of code to be executed if none of the conditions specified in the if and elif statements are true.

The syntax for an else statement is as follows:

```python
if condition1:
  # code to execute if condition1 is true
else:
  # code to execute if condition1 is false
```

When the if statement is executed, the interpreter first checks the condition specified in the if statement.

If the condition is true, the code block following the if statement is executed.

If the condition is false, the interpreter then goes to the else block and execute the code in that block.

You can also use the else statement in conjunction with elif statement:

```python
if condition1:
  # code to execute if condition1 is true
elif condition2:
  # code to execute if condition1 is false and condition2 is true
else:
  # code to execute if condition1 and condition2 are false
```

It's important to note that the else statement does not have a condition, unlike if and elif.

It is a catch-all statement that is executed if all of the previous conditions are false.

It is a good practice to use else statement as a last resort, when none of the conditions are met.

It is also important to note that if you have multiple if-elif blocks in a program, the interpreter will check the condition of each block independently, it will not check the conditions of the if-elif block if it has already found a true condition in a previous block.

## Short Hand If

In Python, a shorthand version of the if-else statement is available, also known as a ternary operator.

This shorthand version allows you to write a simple if-else statement in a single line of code.

The syntax for the shorthand if-else statement is as follows:

```python
result = value_if_true if condition else value_if_false
```

This shorthand version is equivalent to the following if-else statement:

```python
if condition:
  result = value_if_true
else:
  result = value_if_false
```

In the shorthand version, the condition is specified first, followed by the value to be assigned if the condition is true, separated by the keyword if, followed by the value to be assigned if the condition is false, separated by the keyword else.

Here's an example of how you can use the shorthand if in a program:

```python
x = 5
result = "x is greater than 3" if x > 3 else "x is not greater than 3"
print(result)
```

This shorthand version is useful when you want to assign a value to a variable based on a simple condition, but it may not be as readable as the traditional if-else statement when dealing with more complex conditions or multiple conditions.

It's important to note that the shorthand if-else statement is not the same as the ternary operator in C-like languages, which are used to evaluate an expression and return a value.

In Python, shorthand if-else statement is used to assign value to a variable based on a condition.

## And

In Python, the and operator is a logical operator that is used to combine two or more conditions in a single statement.

The and operator returns "True" if all of the conditions are true, and "False" if any of the conditions are false.

The syntax for the and operator is as follows:

```python
condition1 and condition2
```

For example, consider the following code:

```python
x = 5
if x > 0 and x < 10:
  print("x is between 0 and 10")
else:
  print("x is not between 0 and 10")
```

In this example, the and operator is used to check if the value of "x" is greater than 0 and less than 10.

Since the value of "x" is 5, which is greater than 0 and less than 10, the if statement is true and the code in the if block will be executed which will print "x is between 0 and 10".

You can also use the and operator with more than two conditions:

```python
x = 5
y = 10
if x > 0 and x < 10 and y > 0 and y < 20:
  print("x and y are between 0 and 10, and 0 and 20 respectively")
else:
  print("x or y are not between 0 and 10, and 0 and 20 respectively")
```

It's important to note that the and operator has a higher precedence than comparison operators, so it is evaluated before them.

Also, the evaluation of the conditions in an and statement stops as soon as one of the conditions is false.

This is called short-circuit evaluation, which means that if the first condition is false, the interpreter will not evaluate the second condition.

## Or

In Python, the or operator is a logical operator that is used to combine two or more conditions in a single statement.

The or operator returns "True" if any of the conditions are true, and "False" if all of the conditions are false.

The syntax for the or operator is as follows:

condition1 or condition2

For example, consider the following code:

```python
x = 5
if x > 0 or x < -10:
  print("x is greater than 0 or x is less than -10")
else:
  print("x is not greater than 0 or x is not less than -10")
```

In this example, the or operator is used to check if the value of "x" is greater than 0 or x is less than -10.

Since the value of "x" is 5, which is greater than 0, the if statement is true and the code in the if block will be executed which will print "x is greater than 0 or x is less than -10".

You can also use the or operator with more than two conditions:

```python
x = 5
y = 10
if x > 0 or x < -10 or y > 20 or y < -5:
  print("x or y is greater than 0, or x or y is less than -10 or greater than 20 or less than -5 respectively")
else:
  print("x and y are not greater than 0, or x and y are not less than -10 or greater than 20 or less than -5 respectively")
```

It's important to note that the or operator has a higher precedence than comparison operators, so it is evaluated before them.

Also, the evaluation of the conditions in an or statement stops as soon as one of the conditions is true.

This is called short-circuit evaluation, which means that if the first condition is true, the interpreter will not evaluate the second condition.

## Not

In Python, the not operator is a logical operator that is used to negate or invert a Boolean value.

The not operator returns "True" if the operand is "False" and "False" if the operand is "True".

The syntax for the not operator is as follows:

```python
not operand
```

For example, consider the following code:

```python
x = 5
if not (x > 10):
  print("x is not greater than 10")
else:
  print("x is greater than 10")
```

In this example, the not operator is used to check if the value of "x" is not greater than 10.

Since the value of "x" is 5, which is not greater than 10, the if statement is true and the code in the if block will be executed which will print "x is not greater than 10".

You can also use the not operator with other logical operators:

```python
x = 5
y = 10
if not (x > y or x < y):
  print("x is not greater or less than y")
else:
  print("x is greater or less than y")
```

It's important to note that not operator has the highest precedence among the logical operators and it is evaluated first.

Also, when using the not operator with a comparison operator, it is a good practice to use parentheses for clarity.

## Nested If

In Python, a nested if statement is an if statement that is inside another if statement.

This means that an if block can contain one or more if statements.

A nested if statement can be used when you want to check multiple conditions in a single block of code.

The inner if statement is executed only if the outer if statement is true.

The syntax for a nested if statement is as follows:

```python
if condition1:
  # code block 1
  if condition2:
    # code block 2
  else:
    # code block 3
else:
  # code block 4
```

For example, consider the following code:

```python
x = 5
y = 10
if x > 0:
  if y > 0:
    print("x and y are both greater than 0")
  else:
    print("x is greater than 0 and y is not greater than 0")
else:
  print("x is not greater than 0")
```

In this example, the outer if statement checks if the value of "x" is greater than 0.

If the condition is true, the inner if statement is executed, which checks if the value of "y" is greater than 0.

If both conditions are true, the code in the inner if block will be executed which will print "x and y are both greater than 0".

If only the outer condition is true, the code in the inner else block will be executed which will print "x is greater than 0 and y is not greater than 0".

If the outer condition is false, the code in the outer else block will be executed which will print "x is not greater than 0".

Nested if statements can also be used with other control statements like elif and else to create more complex conditions.

## The pass Statement

In Python, the pass statement is used as a placeholder when you want to create a block of code that does nothing.

The pass statement is a null operation; nothing happens when it is executed.

It is useful when you have an empty block of code in a control structure such as an if statement or a for loop, and you don't want to raise a syntax error.

The syntax for the pass statement is simply the keyword pass by itself, with no other code following it.

```python
if condition:
  pass
```

```python
for i in range(10):
  pass
```

For example, consider the following code:

```python
x = 5
if x > 0:
  pass
else:
  print("x is not greater than 0")
```

In this example, if the condition x > 0 is true, the code block under the if statement will not do anything.

The pass statement can also be useful as a placeholder when you are working on a piece of code and you don't have the full implementation ready yet.

Instead of leaving the block of code empty, you can use the pass statement to indicate that the block is not complete and that you plan to come back to it later.

It's important to note that the pass statement is not the same as a comment. A comment is ignored by the interpreter, whereas the pass statement is executed and has no effect.
