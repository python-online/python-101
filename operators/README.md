# Python Operators

Python operators are special symbols in Python that carry out arithmetic or logical computation. The value that the operator operates on is called the operand.

For example: in the expression 2 + 3 = 5, + is the operator that performs addition. The operands are 2 and 3 and the result is 5.

Python supports the following types of operators:

*   Arithmetic Operators
*   Comparison (Relational) Operators
*   Logical (Boolean) Operators
*   Bitwise Operators
*   Assignment Operators
*   Special Operators

## Arithmetic Operators

Arithmetic operators are used to perform mathematical operations like + addition, \- subtraction, \* multiplication, etc.

| Operator | Description | Example |
| --- | --- | --- |
| +   | Addition | 2 + 3 = 5 |
| \-  | Subtraction | 3 - 2 = 1 |
| \*  | Multiplication | 2 \* 3 = 6 |
| /   | Division (float) | 7 / 2 = 3.5 |
| //  | Division (floor) | 7 // 2 = 3 |
| %   | Modulus (remainder) | 7 % 2 = 1 |
| \*\* | Exponentiation | 2 \*\* 3 = 8 |

Example of using Arithmetic Operators:

```python
# Addition
print(2 + 3) # Output: 5

# Subtraction
print(3 - 2) # Output: 1

# Multiplication
print(2 * 3) # Output: 6

# Division (float)
print(7 / 2) # Output: 3.5

# Division (floor)
print(7 // 2) # Output: 3

# Modulus
print(7 % 2) # Output: 1

# Exponentiation
print(2 ** 3) # Output: 8
```

## Comparison Operators

Comparison operators are used to compare values and return a Boolean value.

| Operator | Description | Example |
| --- | --- | --- |
| \== | Equal to | 2 == 3 returns False |
| !=  | Not equal to | 2 != 3 returns True |
| \>  | Greater than | 2 > 3 returns False |
| <   | Less than | 2 < 3 returns True |
| \>= | Greater than or equal to | 2 >= 3 returns False |
| <=  | Less than or equal to | 2 <= 3 returns True |

Example of using Comparison Operators:

```python
# Equal to
print(2 == 3) # Output: False

# Not equal to
print(2 != 3) # Output: True

# Greater than
print(2 > 3) # Output: False

# Less than
print(2 < 3) # Output: True

# Greater than or equal to
print(2 >= 3) # Output: False

# Less than or equal to
print(2 <= 3) # Output: True
```

## Logical Operators

Logical operators are used to combine conditions using and, or, and not.

| Operator | Description | Example |
| --- | --- | --- |
| and | Logical and | (2 == 2) and (3 > 2) returns True |
| or  | Logical or | (2 == 2) or (3 > 2) returns True |
| not | Logical not | not(2 == 2) returns False |

Example of using Logical Operators:

```python
# Logical and
print((2 == 2) and (3 > 2)) # Output: True

# Logical or
print((2 == 2) or (3 > 2)) # Output: True

# Logical not
print(not(2 == 2)) # Output: False
```

## Bitwise Operators

Bitwise operators are used to perform bit-level operations on integers.

| Operator | Description | Example |
| --- | --- | --- |
| &   | Bitwise and | 5 & 3 = 1 |
| \|  | Bitwise or | 5 \| 3 = 7 |
| ^   | Bitwise xor | 5 ^ 3 = 6 |
| ~   | Bitwise not | ~5 = -6 |
| <<  | Left shift | 5 ​\`oaicite:{"index":0,"invalid\_reason":"Malformed citation << 2 = 20 |

Example of using Bitwise Operators:

```python
# Bitwise and
print(5 & 3) # Output: 1

# Bitwise or
print(5 | 3) # Output: 7

# Bitwise xor
print(5 ^ 3) # Output: 6

# Bitwise not
print(~5) # Output: -6

# Left shift
print(5 &#8203;`oaicite:{"index":1,"invalid_reason":"Malformed citation << 2) # Output: 20\n\n# Right shift\nprint(5 >>"}`&#8203; 2) # Output: 1
```

## Assignment Operators

Assignment operators are used to assign values to variables.

| Operator | Description | Example |
| --- | --- | --- |
| \=  | Simple assignment | x = 5 |
| +=  | Add and assignment | x += 5 (same as x = x + 5) |
| \-= | Subtract and assignment | x -= 5 (same as x = x - 5) |
| \*= | Multiply and assignment | x \*= 5 (same as x = x \* 5) |
| /=  | Divide and assignment | x /= 5 (same as x = x / 5) |
| %=  | Modulus and assignment | x %= 5 (same as x = x % 5) |
| //= | Floor division and assignment | x //= 5 (same as x = x // 5) |
| \*\*= | Exponentiation and assignment | x \*\*= 5 (same as x = x \*\* 5) |

Example of using Assignment Operators:

```python
x = 5

# Simple assignment
x = 5
print(x) # Output: 5

# Add and assignment
x += 5
print(x) # Output: 10

# Subtract and assignment
x -= 5
print(x) # Output: 5

# Multiply and assignment
x *= 5
print(x) # Output: 25

# Divide and assignment
x /= 5
print(x) # Output: 5.0

# Modulus and assignment
x %= 3
print(x) # Output: 2.0

# Floor division and assignment
x //= 2
print(x) # Output: 1.0

# Exponentiation and assignment
x **= 2
print(x) # Output: 1.0
```

## Special Operators

Python has a few special operators:

### Identity Operators

Identity operators are used to compare the memory locations of two objects.

| Operator | Description | Example |
| --- | --- | --- |
| is  | True if the operands point to the same object | x is y (True if x and y point to the same object) |
| is not | True if the operands do not point to the same object | x is not y (True if x and y do not point to the same object) |

Example of using Identity Operators:

```python
x = [1, 2, 3]
y = [1, 2, 3]
z = x

# True if x and y point to the same object
print(x is y) # Output: False

# True if x and z point to the same object
print(x is z) # Output: True

# True if x and y do not point to the same object
print(x is not y) # Output: True
```

### Membership Operators

Membership operators are used to test whether an item is present in a sequence (i.e. list, tuple, string).

| Operator | Description | Example |
| --- | --- | --- |
| in  | True if the item is present in the sequence | 3 in x (True if 3 is present in the list x) |
| not in | True if the item is not present in the sequence | 3 not in x (True if 3 is not present in the list x) |

Example of using Membership Operators:

```python
x = [1, 2, 3]

# True if 3 is present in the list x
print(3 in x) # Output: True

# True if 4 is not present in the list x
print(4 not in x) # Output: True
```

### Operator Precedence

Operator precedence determines the order in which operations are performed. Python follows the standard mathematical rules for operator precedence, where operators with higher precedence are executed before operators with lower precedence.

For example, in the expression 2 + 3 \* 4, the multiplication 3 \* 4 is done first because the multiplication operator has higher precedence than the addition operator.

You can use parentheses to change the order of operations. For example, in the expression (2 + 3) \* 4, the addition 2 + 3 is done first because it is inside the parentheses.

You can refer to the table of operator precedence in python to know the order of precedence of operators.

In conclusion, Python has a wide variety of operators that can be used to perform various types of operations. These operators include arithmetic, comparison, logical, bitwise, assignment, identity, and membership operators.

It is important to understand the different types of operators and their precedence in order to write efficient and accurate code.
