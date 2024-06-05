# Python RegEx

Regular expressions, also known as RegEx or regex, are a powerful tool for manipulating text.

They provide a concise way to search and manipulate strings, making them a valuable addition to any programmer's toolbox.

In this guide, we will cover the basics of regular expressions in Python, including how to use them to search for patterns in strings, extract information from text, and replace or manipulate text.

## What are regular expressions?

A regular expression is a sequence of characters that defines a search pattern.

These patterns can be used to match and manipulate strings, making them a powerful tool for text processing.

In Python, regular expressions are supported by the re module, which provides a variety of functions for working with regular expressions.

## Basic Patterns

The most basic regular expression is a simple string of characters.

For example, the pattern "hello" will match any string that contains the substring hello.

```python
import re

# Using the `search` function to find a match
if re.search("hello", "hello world"):
print("Found a match.")
else:
print("No match found.")

# Output: Found a match
```

You can also use special characters called metacharacters to create more complex patterns.

Some of the most commonly used metacharacters include:

*   `.` : Matches any character except a newline.
*   `*` : Matches zero or more of the preceding character or group.
*   `+` : Matches one or more of the preceding character or group.
*   `?` : Matches zero or one of the preceding character or group.
*   `^` : Matches the beginning of a string.
*   `$` : Matches the end of a string.
*   `[]` : Matches any character inside the brackets.
*   `{}` : Specifies the number of times the preceding character or group should be matched.
*   `|` : Matches either the preceding character or group or the character or group following the |.
*   `()` : Groups characters or patterns together.

## Searching for Patterns

There are several functions in the re module that can be used to search for patterns in strings.

Some of the most commonly used functions include:

*   search() : Returns a match object if there is a match anywhere in the string.
*   match() : Returns a match object if the pattern matches the entire string.
*   findall() : Returns a list of all non-overlapping matches in the string.
*   finditer() : Returns an iterator over all non-overlapping matches in the string.

```python
import re

# Searching for a pattern in a string
text = "The cat is beautiful."
match = re.search("cat", text)
if match:
  print("Found a match.")
else:
  print("No match found.")
# Output: Found a match

# Using `findall` function to find all matches
text = "The cat is beautiful. The dog is cute."
matches = re.findall("[cd]at", text)
  print(matches)
# Output: ['cat', 'cat']

# Using `finditer` function to find all matches
text = "The cat is beautiful. The dog is cute."
matches = re.finditer("[cd]at", text)
for match in matches:
  print(match.group())
# Output: 'cat'
```

## Extracting Information from Text

Regular expressions can also be used to extract information from text.

The group() method of a match object can be used to extract the matched string.

Additionally, the groups() method can be used to extract all groups defined in the pattern.

```python
import re

# Extracting information from text
text = "The cat's name is Whiskers."
match = re.search("The (\w+)'s name is (\w+)", text)
if match:
  animal = match.group(1)
  name = match.group(2)
  print(f"Animal: {animal}, Name: {name}")

# Output: Animals: cat, Name: Whiskers
```

## Replacing or Manipulating Text

Regular expressions can also be used to replace or manipulate text.

The sub() function can be used to replace all matches of a pattern with a specified string.

The subn() function can be used to replace all matches of a pattern with a specified string, and return the number of replacements made.

```python
import re

# Replacing text
text = "The cat's name is Whiskers. The dog's name is Buddy."
new_text = re.sub("[Tt]he", "A", text)
print(new_text)
# Output: "A cat's name is Whiskers. A dog's name is Buddy."

# Replacing text with groups
text = "The cat's name is Whiskers. The dog's name is Buddy."
new_text = re.sub("The (\w+)'s name is (\w+)", "A \\1's name is \\2", text)
print(new_text)
# Output: "A cat's name is Whiskers. A dog's name is Buddy."
```

## Conclusion

Regular expressions are a powerful tool for manipulating text. They provide a concise way to search and extract information from strings, as well as replace or manipulate text.

With the re module in Python, you can easily work with regular expressions to improve your text processing capabilities.

This guide covered the basics of regular expressions in Python and provided several examples of how to use them in your code.

Keep in mind that regular expressions can be complex, and take time to master, but with practice and using the reference manual you'll be able to solve many text manipulation tasks.
