# Table of Contents

1. [F-Strings: Formatting and Interpolating Strings in Python](#fstringsintro)
    1. [The Percent Operator Method](#printf)
    2. [The String Format Method](#strformat)
2. [The Formatted string literals Method](#fstringsmethod)

---

# F-Strings: Formatting and Interpolating Strings in Python <a name="fstringsintro"></a>

Python f-strings, or **formatted string literals**, <a href="https://docs.python.org/3/whatsnew/3.6.html#pep-498-formatted-string-literals" style="color:#c9d1d9; text-decoration:underline;">were introduced in Python 3.6 with PEP 498</a> to make string formatting better. Before that, Python used other  string interpolation methods. This article explains those methods and demonstrates how f-strings simplify and improve formatting.

### The Percent Operator Method <a name="printf"></a>

This is also called the **modulo operator**, and <a href="https://realpython.com/python-f-strings/#the-modulo-operator" style="color:#c9d1d9; text-decoration:underline;">this was Python’s first tool for string interpolation</a>. You use the inbuilt `%` operator to embed variables directly into strings.

Here’s an example:

```python
name = "Alice"
age = 30

print("Hello %s, you are %d years old." % (name, age))
```
In the code example above, `%s` and `%d` are placeholders that get replaced by the values of `name` and `age`. While this works for simple cases, it can become cumbersome with many variables or complex expressions.

### The String Format Method <a name="strformat"></a>

The `str.format()` method offers more flexibility than the percent operator.
With this method, <a href="https://www.w3schools.com/python/ref_string_format.asp" style="color:#c9d1d9; text-decoration:underline;">you call `.format()` on a string containing the curly braces placeholders</a> `{}` to replace them with specific values.

Here’s an example:

```python
name = "Alice"
age = 30

print("Hello {}, you are {} years old.".format(name, age))
```
In the code example above, the curly braces `{}` are placeholders replaced by the values passed to `.format()`, helping you insert multiple values in a clear and organized way.

You can also also use named placeholders for more clarity and readability.

Here’s an example:

```python
name = "Alice"
age = 30

print("Hello {n}, you are {a} years old.".format(n=name, a=age))
```
In the code example above, `{n}` and `{a}` are replaced by the corresponding variables. This approach avoids confusion when formatting strings with multiple values and improves readability over empty `{}` placeholders.

## The Formatted String Literals Method <a name="fstringsmethod"></a>
Formatted string literals, or f-strings, were introduced in Python 3.6 with PEP 498. The beauty with this is that they make string interpolation fast and concise, avoiding the verbosity of the `%` formatting or the `.format()` method.  
<a href="https://docs.python.org/3/whatsnew/3.6.html#pep-498-formatted-string-literals" style="color:#c9d1d9; text-decoration:underline;">F-strings start with `f` and embed variables or expressions in curly braces</a> `{}`, making code clearer and more readable.

Here’s an example:

```python
name = "Alice"
age = 30

print(f"Hello {name}, you are {age} years old.")
```

In the code example above, `{name}` and `{age}` are replaced by the values of the corresponding variables at runtime. This makes f-strings cleaner, better, more readable, and more flexible than the older methods, especially when combining multiple variables or expressions in a single string.
