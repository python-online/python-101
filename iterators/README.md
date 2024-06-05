# Python Iterators

An iterator is an object that can be iterated (looped) upon. An object which will return data, one element at a time. They are used to represent a stream of data.

In Python, an iterator is an object which implements the iterator protocol, which consist of the methods iter() and next().

## Creating an Iterator

To create an iterator in Python, there are two methods:

*   Using iter() function
*   Implementing iter() and next() methods

### Method 1: Using iter() function

The iter() function is used to create an iterator. It takes an iterable object as an argument, and returns an iterator object.

The following example shows how to use the iter() function to create an iterator for a list.

```python
# Creating an iterator using iter() function
numbers = [1, 2, 3, 4]
it = iter(numbers)
print(next(it))
print(next(it))
print(next(it))
print(next(it))
```

### Method 2: Implementing iter() and next() methods

The iter() method returns the iterator object itself. The next() method returns the next value from the iterator.

If there are no more items to return, it should raise StopIteration.

Here is an example of how to create an iterator by implementing these methods:

```python
class Numbers:
  def __init__(self):
    self.num = 1

  def __iter__(self):
    return self

  def __next__(self):
    if self.num <= 10:
      val = self.num
      self.num += 1
      return val
    else:
      raise StopIteration

numbers = Numbers()
it = iter(numbers)
print(next(it))
print(next(it))
print(next(it))
```

## Iterating through an Iterator

Once we have an iterator, we can use the next() function to get the next value from the iterator.

The following example shows how to iterate through the elements of a list using an iterator:

```python
numbers = [1, 2, 3, 4]
it = iter(numbers)

for i in it:
  print(i)
```

## Iterator vs Iterable

An iterable is an object which has an iter() method. It can be used to get an iterator. An iterator is an object which has a next() method.

In Python, lists, tuples, sets, and dictionaries are all iterable objects.

They have an iter() method which returns an iterator. Strings are also iterable objects.

```python
# A string is an iterable
string = "Python"
it = iter(string)
print(next(it))
print(next(it))

# A list is also iterable
numbers = [1, 2, 3, 4]
it = iter(numbers)
print(next(it))
```

In summary, an iterator is an object that can be iterated (looped) upon. An object which will return data, one element at a time.

To create an iterator in Python, we can use the iter() function or by implementing the iter() and next() methods.

Iterators have a next() method which returns the next value.

## StopIteration

The StopIteration is raised when there are no more items to return in an iterator.

It is used to signal the end of the iteration. When the next() function is called and there are no more items to return, it raises the StopIteration exception.

This is how the for loop or any other looping construct knows when to stop loop.

In the example I gave earlier, the \_\_next\_\_() method of the Numbers class raises the StopIteration exception when the value of self.num becomes greater than 10, indicating that there are no more values to return in the iterator.

## Using the iterator in a for loop

We can also use an iterator in a for loop.

The for loop automatically catches the StopIteration exception and stops the loop when there are no more items to return.

Here is an example of using an iterator in a for loop:

```python
numbers = [1, 2, 3, 4]
it = iter(numbers)

for i in it:
  print(i)
```

In this example, the for loop automatically calls the next() function of the iterator and assigns the returned value to the variable i.

When the iterator raises the StopIteration exception, the for loop stops.

Another way to do this is to use the built-in function range() to generate a sequence of numbers.

```python
for i in range(5):
  print(i)
```

This is equivalent to the following code:

```python
it = iter(range(5))
for i in it:
  print(i)
```

In this way, we can use an iterator to handle a large amount of data that cannot fit in memory all at once, or to read a file line by line, or to traverse a tree or a graph.

In summary, Python Iterators are objects that can be iterated (looped) upon.

They are used to represent a stream of data. In Python, an iterator is an object which implements the iterator protocol, which consist of the methods iter() and next().

The iter() method returns the iterator object itself, the next() method returns the next value from the iterator and when there are no more items to return, it should raise StopIteration.

Iterators are commonly used in for loops and can be used to handle large amount of data, read a file line by line, or traverse a tree or a graph.
