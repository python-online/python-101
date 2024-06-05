# Python Inheritance

Inheritance is a fundamental concept in object-oriented programming (OOP) that allows one class to inherit properties and methods from another class.

In Python, inheritance is achieved by defining a class that is derived from one or more base classes.

## Understanding Inheritance

Inheritance allows a derived class to inherit the properties and methods of a base class, which can save time and effort when creating new classes.

The derived class is also known as a child class or subclass, while the base class is known as the parent class or superclass.

A classic example of inheritance is a shape class, which can have subclasses such as a rectangle or a circle class.

The shape class would have properties and methods that are common to all shapes, such as a location and a color.

The rectangle and circle classes would then inherit these properties and methods, and also have additional properties and methods specific to their shape.

## Defining a Base Class

A base class is defined like any other Python class, with the class keyword, followed by the name of the class and a colon.

Properties and methods are then defined within the class using the standard Python syntax.

For example, let's create a base class called Shape with a location and color property, and a move method that changes the location of the shape:

```python
class Shape:
  def __init__(self, x, y, color):
    self.location = (x, y)
    self.color = color

def move(self, x, y):
  self.location = (x, y)
```

## Defining a Derived Class

A derived class is defined by including the base class in parentheses after the class name, like so:

```python
class Rectangle(Shape):
```

This tells Python that the Rectangle class is derived from the Shape class, and that it should inherit all of the properties and methods of the Shape class.

We can add properties and methods to the Rectangle class that are specific to rectangles, such as a width and height property, and a calculate\_area() method:

```python
class Rectangle(Shape):
  def __init__(self, x, y, color, width, height):
    super().__init__(x, y, color)
    self.width = width
    self.height = height
  def calculate_area(self):
    return self.width * self.height
```

Here, we are using super() function which calls the \_\_init\_\_ method of the base class Shape and pass the required parameters.

## Overriding Properties and Methods

A derived class can also override properties and methods of the base class.

This allows the derived class to change the behavior of the inherited properties and methods, or to add additional functionality.

For example, if we want to change the behavior of the move() method for the Rectangle class, we can do this:

```python
class Rectangle(Shape):
  def move(self, x, y):
    self.location = (x + self.width, y + self.height)
```

This new move() method will move the rectangle by the width and height, rather than just to the new x and y coordinates.

## Using Inheritance

Once a class has been defined, it can be used just like any other class in Python.

For example, to create an instance of the Rectangle class, we can do this:

```python
r = Rectangle(0, 0, "blue", 10, 20)
```

And we can access its properties and methods:

```python
print(r.location) # (0, 0)
print(r.color) # blue
print(r.width) # 10
print(r.height) # 20
print(r.calculate_area()) # 200

r.move(5, 5)
print(r.location) # (5, 5)
```

It's also possible to check if an instance of a class is an instance of a particular class or one of its subclasses using the isinstance() function.

```python
print(isinstance(r, Rectangle)) # True
print(isinstance(r, Shape)) # True
```

## Conclusion

Inheritance is a powerful feature of object-oriented programming that allows for code reuse and efficient organization of code.

It allows a derived class to inherit the properties and methods of a base class, and also allows for overriding and adding new functionality.

Understanding and utilizing inheritance can greatly improve the structure and maintainability of your code.
