# F-Strings: Formatting and Interpolating Strings in Python <a name="fstringsintro"></a>

Python f-strings, also called formatted string literals, <a href="https://docs.python.org/3/whatsnew/3.6.html#pep-498-formatted-string-literals" style="color:#c9d1d9; text-decoration:underline;">were introduced in Python 3.6 with PEP 498</a> to simplify string formatting. Before f-strings, you had to use older methods that were either verbose or less readable. In this tutorial, you’ll see how strings were formatted before, how f-strings work, and why they are often the better choice.

## String Interpolation Before Python 3.6 <a name="methods"></a>

Before Python 3.6, two methods were widely used: **printf-style formatting** and **str.format()** which will be discussed below.

### Printf-Style Formatting <a name="printf"></a>

This uses the percent (%) operator to embed variables into strings.

Example:

name = "Alice"
age = 30

print("Hello %s, you are %d years old." % (name, age))


Why it works: %s and %d are placeholders replaced by name and age.

Recap: While simple, this method can become cumbersome with many variables and is less readable, especially for complex expressions.

### The str.format() Method <a name="strformat"></a>

Here, placeholders {} are replaced using the .format() method.

Example:

name = "Alice"
age = 30
height = 1.65

print("Hello {}, you are {} years old and {} meters tall.".format(name, age, height))


Why it works: Curly braces {} act as placeholders. You can also use named placeholders for clarity:

print("Hello {n}, you are {a} years old.".format(n=name, a=age))


Recap: .format() improves readability and flexibility over printf-style formatting, but it’s still more verbose than f-strings.

## Formatted String Literals (F-Strings) <a name="fstringsmethod"></a>

F-strings make string interpolation concise, readable, and fast. You prefix the string with f and embed variables or expressions directly.

Example:

name = "Alice"
age = 30

print(f"Hello {name}, you are {age} years old.")


Why it works: The placeholders {name} and {age} are evaluated at runtime, letting you include expressions without extra method calls.

Recap: F-strings reduce boilerplate, improve readability, and are generally the preferred modern approach to string formatting.

## Conclusion <a name="conclude"></a>

You now know three ways to format strings in Python. F-strings combine simplicity, clarity, and speed, making them a superior choice for most use cases. By embedding variables and expressions directly into strings, you write cleaner, more Pythonic code. For modern Python projects, f-strings are the way to go.