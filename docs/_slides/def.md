---
---

## Function definition

We already saw examples of a few built-in functions, such as `type()` or `len()`.
You can define your own Python functions as a block of code starting with a `def`
statement.


~~~python
def add_two(num):
    result = num + 2
    return result
~~~
{:.text-document title="worksheet.py"}



~~~python
>>> add_two(10)
12

~~~
{:.output}



===

The `def` keyword is followed by the function name, its arguments enclosed in
parentheses (separated by commas if there are more than one), and a colon. The
`return` statement passes the specified result as the output of the function. 
A simple `return` line with no output value just exits the function.

After it is defined, the function is invoked using its name and specifying the
arguments in parentheses, in the same order as in its definition.

===


~~~python
def add_any(num, x=0):
    result = num + x
    return result
~~~
{:.text-document title="worksheet.py"}



~~~python
>>> add_any(10, 5)
15

~~~
{:.output}



===

## Exercise 5

Create a function that takes a list as an argument and returns
its first and last elements as a new list.