# Python For Loops

For loops in Python are used to iterate over a sequence (such as a list, tuple, or string) and execute a block of code for each item in the sequence.

The basic syntax for a for loop is as follows:

```python
for variable in sequence:
  # code to execute
```

The variable is a placeholder for the current item in the sequence, and the sequence is the list, tuple, or string that you want to iterate over.

Here is an example of a for loop that iterates over a list of numbers and prints each one:

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
  print(num)
```

This code would output the following:

```plain
1
2
3
4
5
```

You can also use the range() function to create a sequence of numbers to iterate over.

The range() function takes three arguments: start, stop, and step.

The start argument is the first number in the sequence, the stop argument is the number to stop at (this number is not included in the sequence), and the step argument is the difference between each number in the sequence.

Here is an example of using the range() function to print out the numbers from 0 to 9:

```python
for num in range(10):
  print(num)
```

This code would output the following:

```plain
0
1
2
3
4
5
6
7
8
9
```

You can also use the enumerate() function to iterate over a sequence and keep track of the index of the current item.

The enumerate() function takes a sequence as an argument and returns an iterator that generates tuples containing the index and the current item.

Here is an example of using the enumerate() function to print out the index and value of each item in a list:

```python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
  print(index, fruit)
```

This code would output the following:

```plain
0 apple
1 banana
2 cherry
```

You can also use for loops with else statement to run some code once the for loop is completed successfully.

Here is an example of using the else statement with a for loop:

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
  print(num)
else:
  print("For loop completed successfully")
```

This code would output the following:

```plain
1
2
3
4
5
For loop completed successfully
```

Another use case of using for loops is using break and continue statements.

break statement is used to exit the loop before it completes the iteration and continue statement is used to skip the current iteration and continue with the next iteration.

Here is an example of using break statement:

```python
for num in range(10):
  if num == 3:
    break
  print(num)
```

This code would output the following:

```plain
0
1
2
```

Here is an example of using the continue statement:

```python
for num in range(10):
  if num % 2 != 0:
    continue
  print(num)
```

This code would output the following:

```plain
0
2
4
6
8
```

In the above example, the continue statement is used to skip all the odd numbers and only print the even numbers.

For loops in Python are a powerful tool for iterating over a sequence of items and executing a block of code for each item.

The range() function, enumerate() function, else statement, break and continue statements provide additional functionality to for loops to make them more versatile and efficient.

## The range() Function

The range() function in Python is used to generate a sequence of numbers.

The basic syntax for the range() function is as follows:

```python
range(stop)
range(start, stop)
range(start, stop, step)
```

The stop argument is required, and it specifies the number to stop at (this number is not included in the sequence).

The start and step arguments are optional and default to 0 and 1, respectively.

The start argument is the first number in the sequence, and the step argument is the difference between each number in the sequence.

Here are some examples of using the range() function:

```python
# Generate a sequence of numbers from 0 to 9
for num in range(10):
  print(num)
```

```python
# Generate a sequence of numbers from 5 to 9
for num in range(5, 10):
  print(num)
```

```python
# Generate a sequence of even numbers from 0 to 10
for num in range(0, 11, 2):
  print(num)
```

It's important to note that the range() function returns an iterable object and not a list, so if you want to create a list of numbers, you can use the list() function as follows:

```python
numbers = list(range(10))
```

The range() function can be used in a variety of ways, such as in for loops to iterate over a sequence of numbers, in list comprehension to create lists of numbers, or with the next() function to generate numbers one at a time.

## Nested Loops

A nested loop is a loop that is inside another loop. In other words, it is a loop that is used within another loop.

The inner loop runs to completion for each iteration of the outer loop.

Here is an example of a nested loop:

```python
for i in range(3):
  for j in range(2):
    print(i, j)
```

The output of this code will be:

```plain
0 0
0 1
1 0
1 1
2 0
2 1
```

In the above example, the outer loop runs 3 times, and for each iteration of the outer loop, the inner loop runs 2 times.

The inner loop completes before the outer loop continues to the next iteration.

The nested loop can also be used with different types of loops.

For example, you can use a for loop inside a while loop:

```python
i = 0
while i < 3:
  for j in range(2):
    print(i, j)
  i += 1
```

Nested loops are useful when you need to perform a certain operation on all elements of a nested list or a nested data structure like a dictionary.

You can use the outer loop to iterate over the outer elements, and the inner loop to iterate over the inner elements.

It's important to keep in mind that the number of iterations of the nested loop is equal to the number of iterations of the outer loop multiplied by the number of iterations of the inner loop.

So, nested loops can be very powerful but also make your code to run slow, especially when the number of iterations is large.

In summary, nested loops are useful when you need to perform an operation on all elements of a nested data structure or when you need to iterate over multiple sequences at the same time.

It's important to be mindful of the number of iterations and the performance of your code when using nested loops.

## The pass Statement

The pass statement in Python is used as a placeholder for code that has not yet been implemented.

It is a null statement and does not perform any action when executed.

The pass statement is often used as a placeholder in control structures (such as loops and conditional statements) when the programmer doesn't want to leave the structure empty, but also doesn't have any specific code to execute yet.

Here is an example of using the pass statement in a loop:

```python
for num in range(10):
  if num % 2 == 0:
    pass
  else:
    print(num)
```

In the above example, the if statement checks if the current number is even.

If the number is even, the pass statement is executed, and nothing happens.

If the number is odd, the else statement is executed and the number is printed.

Another use case for the pass statement is in classes and functions that are being defined but not implemented yet.

For example:

```python
class MyClass:
  pass
```

```python
def my_function():
  pass
```

In this case, the pass statement is used as a placeholder so that the class or function can be defined, but no code will be executed when the class or function is called.

This allows the programmer to implement the class or function later without having to remove or comment out any code.

In summary, the pass statement is a null statement that is used as a placeholder in control structures and class/function definitions when the developer doesn't have any specific code to execute yet.

It is useful to keep the structure of the code intact while allowing the programmer to implement the code later.
