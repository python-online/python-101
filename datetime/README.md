# Python Date / Time

Python's datetime module provides several classes for working with dates and times. These classes include date, time, datetime, timedelta, and tzinfo.

In this guide, we will cover the basics of using these classes to work with date and time data in Python.

## date

The date class represents a single date (year, month, and day).

It can be used to create a date object, which can then be used to extract the individual components of the date (year, month, and day).

### Creating a date object

To create a date object, you can use the date() constructor, which takes three arguments: year, month, and day.

For example:

```python
from datetime import date

d = date(2022, 12, 31)
print(d)
# Output: 2022-12-31
```

You can also use the today() function to create a date object representing the current date:

```python
from datetime import date

d = date.today()
print(d)
# Output: 2022-12-31
```

### Extracting date components

You can use the year, month, and day attributes of a date object to extract the individual components of the date.

For example:

```python
from datetime import date

d = date(2022, 12, 31)
print(d.year) # Output: 2022
print(d.month) # Output: 12
print(d.day) # Output: 31
```

### Comparing dates

You can use the standard comparison operators ( <, \>, \==, etc. ) to compare two date objects.

For example:

```python
from datetime import date

d1 = date(2022, 12, 31)
d2 = date(2022, 12, 30)
print(d1 > d2) # Output: True
```

## time

The time class represents a single time (hours, minutes, seconds, and microseconds).

It can be used to create a time object, which can then be used to extract the individual components of the time (hours, minutes, seconds, and microseconds).

### Creating a time object

To create a time object, you can use the time() constructor, which takes four arguments: hours, minutes, seconds, and microseconds.

For example:

```python
from datetime import time

t = time(12, 30, 45)
print(t)
# Output: 12:30:45
```

### Extracting time components

You can use the hour, minute, second, and microsecond attributes of a time object to extract the individual components of the time.

For example:

```python
from datetime import time

t = time(12, 30, 45)
print(t.hour) # Output: 12
print(t.minute) # Output: 30
print(t.second) # Output: 45
print(t.microsecond) # Output: 0
```

### Comparing times

You can use the standard comparison operators ( <, \>, \==, etc. ) to compare two time objects.

For example:

```python
from datetime import time

t1 = time(12, 30, 45)
t2 = time(12, 30, 44)
print(t1 > t2) # Output: True
```

## datetime

The datetime class combines the functionality of the date and time classes.

It can be used to create a single object representing both a date and a time.

### Creating a datetime object

To create a datetime object, you can use the datetime() constructor, which takes six arguments: year, month, day, hour, minute, and second.

For example:

```python
from datetime import datetime

dt = datetime(2022, 12, 31, 12, 30, 45)
print(dt)
# Output: 2022-12-31 12:30:45
```

You can also use the now() function to create a datetime object representing the current date and time:

```python
from datetime import datetime

dt = datetime.now()
print(dt)
# Output: 2022-12-31 12:30:45.123456
```

### Extracting datetime components

You can use the year, month, day, hour, minute, second, and microsecond attributes of a datetime object to extract the individual components of the date and time.

For example:

```python
from datetime import datetime

dt = datetime(2022, 12, 31, 12, 30, 45)
print(dt.year) # Output: 2022
print(dt.month) # Output: 12
print(dt.day) # Output: 31
print(dt.hour) # Output: 12
print(dt.minute) # Output: 30
print(dt.second) # Output: 45
print(dt.microsecond) # Output: 0
```

### Comparing datetimes

You can use the standard comparison operators ( <, \>, \==, etc. ) to compare two datetime objects.

For example:

```python
from datetime import datetime

dt1 = datetime(2022, 12, 31, 12, 30, 45)
dt2 = datetime(2022, 12, 31, 12, 30, 44)
print(dt1 > dt2) # Output: True
```

### Formatting datetime

You can use the strftime() method to format a datetime object as a string. It takes a format string as an argument, which specifies how the datetime should be formatted.

For example:

```python
from datetime import datetime

dt = datetime(2022, 12, 31, 12, 30, 45)
print(dt.strftime('%Y-%m-%d %H:%M:%S'))
# Output: 2022-12-31 12:30:45
```

You can use the various codes like %Y, %m, %d, %H, %M, %S, etc. to format the datetime object accordingly.

## timedelta

A timedelta object represents a duration, the difference between two dates or times.

It can be used to perform arithmetic with date and time objects.

### Creating a timedelta object

To create a timedelta object, you can use the timedelta() constructor, which takes several arguments to represent days, seconds, microseconds, milliseconds, minutes, hours, weeks.

For example:

```python
from datetime import timedelta

td = timedelta(days=1, seconds=3600)
print(td)
# Output: 1:01:00
```

### Arithmetic with timedeltas

You can perform arithmetic operations with timedeltas and datetime objects.

For example:

```python
from datetime import timedelta, datetime

dt = datetime(2022, 12, 31)
td = timedelta(days=1)
print(dt + td)
# Output: 2023-01-01 00:00:00

td2 = timedelta(days=3)
print(td + td2)
# Output: 4:00:00
```

### Comparing timedeltas

You can use the standard comparison operators ( <, \>, \==, etc. ) to compare two timedelta objects.

For example:

```python
from datetime import timedelta

td1 = timedelta(days=1)
td2 = timedelta(hours=24)
print(td1 == td2) # Output: True
```

### timedelta attributes

You can use the days, seconds, microseconds attributes of a timedelta object to extract the individual components of the duration.

For example:

```python
from datetime import timedelta

td = timedelta(days=1, seconds=3600)
print(td.days) # Output: 1
print(td.seconds) # Output: 3600
print(td.microseconds) # Output: 0
```

In this guide, I have provided an overview of the date, time, datetime, and timedelta classes in the Python datetime module.

I have shown how to create date and time objects, extract their components, perform arithmetic with them, and format them as strings.

With the knowledge of these classes and their methods, you should be able to work with dates and times in your Python programs.
