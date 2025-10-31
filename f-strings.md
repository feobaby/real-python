# Table of Contents


1. [F-Strings: Formatting and Interpolating Strings in Python](#fstrings)
<!-- 2. [String interpolation and formatting in Python before version 3.6](#methods)
    1. [The Printf-Style String Formatting Method](#tech)
    2. [The str.format() String Formatting Method](#gql)
3. [The Formatted string literals Method](#schema)
4. [Conclusion](#tools) -->

---

# F-Strings: Formatting and Interpolating Strings in Python <a name="fstrings"></a>

Python f-strings, also called **formatted string literals**, were introduced in Python 3.6 to make string formatting and interpolation much easier. Before f-strings, two common methods were used for string interpolation. In this article, you will learn how strings were formatted before, what f-strings are, and how to use them.

## String interpolation and formatting in Python before version 3.6<a name="methods"></a>
There were two widespread ways of formatting strings in Python before the introduction of Python 3.6. The first was the **printf-style string formatting** method, and the second was using the **str.format()** method, which will be discussed further.

### The Printf-Style String Formatting Method
This is also commonly known as the **percent (%) formatting** method or the **modulo operator**. This is where string objects have the `%` operator (modulo) as an inbuilt operator in Python in Python <a href="https://realpython.com/python-f-strings/#the-modulo-operator" style="color:#c9d1d9; text-decoration:underline;">and was the first tool used for string interpolation and formatting</a> in Python.


For example, here’s how you can use it:
```
name = "Alice"
age = 30
height = 1.65

print("Hello %s, you are %d years old and %s meters tall." % (name, age, height))
```
In this code example, the placeholders %s and %d are replaced by the values of name, age, and height. You can see how percent formatting lets you create a readable, dynamic message without manually converting variables to strings.

### The str.format() String Formatting Method
The **str.format()** method is quite different from **printf-style string formatting** method. With this method, you use the `.format()` method to insert specified values into placeholders defined by curly brackets `{}`. The `.format()` method then returns the formatted string.\
It was introduced as an improvement over percent formatting, giving you more precise control over how values are displayed.

For example, here’s how you can use it:
```
name = "Alice"
age = 30
height = 1.65

print("Hello {}, you are {} years old and {} meters tall.".format(name, age, height))
```
In this code example,
the curly braces {} act as placeholders that are replaced by the values passed to the .format() method, in the order they appear. This allows you to create a dynamic, readable string without manually converting variables to strings.

You should also know that placeholders can be named, which makes your code more readable and clear, instead of using empty {} curly braces. Named placeholders also promote reusability and clarity.

For example, here’s how you can use it:
```
name = "Alice"
age = 30
height = 1.65

print("Hello {n}, you are {a} years old and {h} meters tall.".format(
    n=name, a=age, h=height
))

```
In this code, the placeholders {n}, {a}, and {h} are named placeholders. They are replaced by the values provided in the .format() method. Using named placeholders makes your code more readable, easier to maintain, and allows you to reuse variables without worrying about their order.

## The Formatted string literals Method
Formatted string literals, commonly known as f-strings, were introduced in Python 3.6 with PEP 498. You will find f-strings useful because they make string interpolation quick and concise, unlike percent formatting or str.format(). <a href="https://docs.python.org/3/whatsnew/3.6.html#pep-498-formatted-string-literals" style="color:#c9d1d9; text-decoration:underline;">F-strings start with f and use a syntax similar to the format strings accepted by str.format()</a>.

For example, here’s how you can use f-strings:
```
name = "Alice"
age = 30
height = 1.65

print(f"Hello {name}, you are {age} years old and {height} meters tall.")
```

In this code example, the placeholders {name}, {age}, and {height} are replaced by the values of the corresponding variables. You can see how f-strings make it easy for you to create readable, dynamic strings without extra conversions or method calls.

## Conclusion