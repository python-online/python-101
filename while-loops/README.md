# Python While Loops

A while loop in Python is used to repeatedly execute a block of code as long as a given condition is true.

The syntax for a while loop is as follows:

```python
while condition:
  # code to be executed
```

The condition is evaluated before each iteration of the loop. If the condition is true, the code within the loop is executed.

Once the code within the loop has finished executing, the condition is evaluated again.

If the condition is still true, the code within the loop is executed again, and so on.

This process continues until the condition becomes false, at which point the loop stops executing.

It's important to keep in mind that if the condition is never false, the loop will continue to execute indefinitely, resulting in an infinite loop.

To prevent this, it's important to ensure that the condition will eventually become false, or to include a way to break out of the loop within the loop's code.

Example 1:

```python
count = 0
while count < 5:
  print(count)
  count += 1
```

Output:

```plain
0
1
2
3
4
```

In this example, the while loop will execute as long as the value of the variable count is less than 5.

The code within the loop simply prints the current value of count, and then increments the value of count by 1.

Once count reaches a value of 5, the loop will stop executing.

Example 2:

```python
while True:
  response = input("Enter a number: ")
  if int(response) % 2 == 0:
    print("The number you entered is even.")
    break
  else:
    print("The number you entered is odd.")
```

In this example, the while loop will execute indefinitely, because the condition is always true.

However, the code within the loop includes a way to break out of the loop: if the user enters an even number, the break statement is executed, which causes the loop to stop executing.

In summary, Python's while loops allow you to repeatedly execute a block of code as long as a given condition is true.

It's important to ensure that the condition will eventually become false or include a way to break out of the loop within the loop's code to avoid infinite loop.

Another way to control the flow of a while loop is through the use of the continue statement.

The continue statement causes the current iteration of the loop to be skipped, and the next iteration to begin immediately.

Example:

```python
count = 0
while count < 5:
  count += 1
  if count % 2 != 0:
    continue
  print(count)
```

Output:

```plain
2
4
```

In this example, the while loop will execute as long as the value of the variable count is less than 5.

The code within the loop increments the value of count by 1 and then checks if it is an odd number.

If it is an odd number, the continue statement is executed and the current iteration is skipped and the loop will continue to the next iteration.

If the value of count is even, the print statement is executed and the value of count is printed out.

In summary, the continue statement allows you to skip the current iteration of a loop and move on to the next iteration.

This can be useful for filtering out certain values or skipping over certain sections of code.

It can be used in conjunction with the if-else statement, to control the flow of the loop depending on certain conditions.

## The break Statement

The break statement is used to exit a loop early, before the loop's condition is met.

When the break statement is encountered within a loop, the loop is immediately terminated, and the program control resumes after the loop.

Example:

```python
count = 0
while count < 5:
  count += 1
  if count == 3:
    break
  print(count)
```

Output:

```plain
1
2
```

In this example, the while loop will execute as long as the value of the variable count is less than 5.

The code within the loop increments the value of count by 1, and then checks if it is equal to 3, if it is true the break statement is executed, and the loop is immediately terminated and the program control resumes after the loop.

If the condition is not met the print statement is executed and the value of count is printed out.

It's important to keep in mind that the break statement will only exit the innermost loop in which it is used.

If a break statement is used within a nested loop, it will only exit the innermost loop, and the program control will return to the next higher level loop.

The break statement can be useful for exiting a loop early when a specific condition is met, or for exiting a loop that would otherwise run indefinitely.

It's often used in conjunction with an if-else statement, to control the flow of the loop depending on certain conditions.

In summary, the break statement is used to exit a loop early, before the loop's condition is met, it can be useful for exiting a loop early when a specific condition is met, or for exiting a loop that would otherwise run indefinitely.

It can be used in conjunction with an if-else statement, to control the flow of the loop depending on certain conditions.

## The Continue Statement

The continue statement is used to skip the current iteration of a loop and move on to the next iteration.

When the continue statement is encountered within a loop, the current iteration is skipped, and the program control jumps to the next iteration of the loop.

Example:

```python
count = 0
while count < 5:
  count += 1
  if count % 2 != 0:
    continue
  print(count)
```

Output:

```plain
2
4
```

In this example, the while loop will execute as long as the value of the variable count is less than 5.

The code within the loop increments the value of count by 1 and then checks if it is an odd number using the modulo operator.

If the remainder when dividing by 2 is not equal to zero, the continue statement is executed, and the current iteration is skipped, and the loop continues to the next iteration.

If the value of count is even, the print statement is executed, and the value of count is printed out.

The continue statement can be useful for filtering out certain values or skipping over certain sections of code.

It can be used in conjunction with an if-else statement, to control the flow of the loop depending on certain conditions.

In summary, The continue statement allows you to skip the current iteration of a loop and move on to the next iteration.

This can be useful for filtering out certain values or skipping over certain sections of code.

It can be used in conjunction with the if-else statement, to control the flow of the loop depending on certain conditions.

## The else Statement

The else statement can be used in conjunction with a while loop, and it is executed when the loop has completed all of its iterations.

The else statement is only executed if the loop's condition is false, which means the loop has completed all of its iterations without being terminated by a break statement.

Example:

```python
count = 0
while count < 5:
  count += 1
  if count == 3:
    break
  print(count)
else:
  print("The loop has completed all its iterations")
```

Output:

```plain
1
2
The loop has completed all its iterations
```

In this example, the while loop will execute as long as the value of the variable count is less than 5.

The code within the loop increments the value of count by 1, and then checks if it is equal to 3.

If it is true, the break statement is executed, and the loop is immediately terminated, and the program control resumes after the loop.

If the condition is not met the print statement is executed, and the value of count is printed out.

Since the loop has completed all its iterations without the break statement, the else statement is executed and the message "The loop has completed all its iterations" is printed out.

The else statement can be useful for providing a way to run some code after the loop has completed, without using a flag variable.

It can be used in conjunction with the if-else statement, to control the flow of the loop depending on certain conditions.

In summary, the else statement can be used in conjunction with a while loop, and it is executed when the loop has completed all of its iterations, the else statement is only executed if the loop's condition is false, which means the loop has completed all of its iterations without being terminated by a break statement.

It can be useful for providing a way to run some code after the loop has completed, without using a flag variable.

It can be used in conjunction with the if-else statement, to control the flow of the loop depending on certain conditions.
