# Python JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate.

JSON is a text format that is completely language-independent but uses conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. These properties make JSON an ideal data-interchange language.

In Python, JSON can be used in two ways:

*   Converting Python objects into JSON strings - also known as serialization.
*   Parsing JSON strings into Python objects - also known as deserialization.

## Converting Python objects into JSON strings

Python has a built-in package called json, which can be used to work with JSON data.

The json.dumps() method converts a Python object into a JSON string, while json.dump() method is used to write JSON data to a file-like object.

Here is an example of converting a Python dictionary into a JSON string:

```python
import json

data = {
  "name": "John Smith",
  "age": 30,
  "city": "New York"
}

json_data = json.dumps(data)

print(json_data)
```

Output:

```plain
{"name": "John Smith", "age": 30, "city": "New York"}
```

Here is an example of writing JSON data to a file:

```python
import json

data = {
  "name": "John Smith",
  "age": 30,
  "city": "New York"
}

with open("data.json", "w") as outfile:
  json.dump(data, outfile)
```

## Parsing JSON strings into Python objects

The json.loads() method is used to parse a JSON string and convert it into a Python object, while the json.load() method is used to read a JSON file and convert it into a Python object.

Here is an example of parsing a JSON string and converting it into a Python dictionary:

```python
import json

json_data = '{"name": "John Smith", "age": 30, "city": "New York"}'

data = json.loads(json_data)

print(data)
```

Output:

```plain
{'name': 'John Smith', 'age': 30, 'city': 'New York'}
```

Here is an example of reading a JSON file and converting it into a Python object:

```python
import json

with open("data.json", "r") as infile:
  data = json.load(infile)

print(data)
```

Output:

```plain
{'name': 'John Smith', 'age': 30, 'city': 'New York'}
```

Additionally you can use json.load() and json.loads() method with object\_hook and object\_pairs\_hook parameters to deserialize JSON to custom Python object, like this:

```python
import json

class Person:
  def __init__(self, name, age, city):
  self.name = name
  self.age = age
  self.city = city

def json_obj_hook(dct):
  return Person(dct['name'], dct['age'], dct['city'])
  json_data = '{"name": "John Smith", "age": 30, "city": "New York"}'
  data = json.loads(json_data, object_hook=json_obj_hook)

print(data.name)
print(data.age)
print(data.city)
```

Output:

```plain
John Smith
30
New York
```

In this example, we defined a Person class and used the json\_obj\_hook function to convert the JSON data into an instance of the Person class.

You can also use json.JSONEncoder class for custom JSON encoding.

```python
class PersonEncoder(json.JSONEncoder):
  def default(self, obj):
    if isinstance(obj, Person):
      return {'name': obj.name, 'age': obj.age, 'city': obj.city}
    return super().default(obj)

data = Person("John Smith", 30, "New York")
json_data = json.dumps(data, cls=PersonEncoder)
print(json_data)
```

Output:

```plain
{"name": "John Smith", "age": 30, "city": "New York"}
```

In this example, we defined a PersonEncoder class that inherits from json.JSONEncoder and overrides the default method to handle instances of the Person class.

In this guide, we have covered the basic usage of the json module in Python for working with JSON data.

It should give you a good foundation for working with JSON data in Python, and provide you with the tools to start integrating JSON data into your Python applications.
