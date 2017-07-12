---
---

## Flow control

The list and dictionary comprehensions embed a short form of the expression used to initiate a looping control statement.

===

## For loops

A `for` loop takes any iterable object and executes a block of code once for each
element `in` the iterable..


~~~python
squares = []
for i in range(1, 5):
    j = i ** 2
    squares.append(j)
n_squares = len(squares)
~~~
{:.text-document title="worksheet.py"}



~~~python
>>> n_squares
4
~~~
{:.output}



The `range(i, j)` function creates a list of integers from `i` up through `j - 1`; just
like in the case of list slices, the range is not inclusive of the upper bound.

===

## Indentation

Note the pattern of the block above:

- the `for x in y` expression is followed by a colon
- the following lines are indented **equally**
- un-indenting indicates the end of the loop (rather than any special character)

Compared with other programming languages in which code indentation only serves to
enhance readability, Python uses indentation (and **only** indentation) to define "code blocks", a.k.a. statements.

===

## Nesting indentation

A `for` loop can be used to iterate over the elements of any list. In the
following example, we create a contact list (as a list of dictionaries), then
perform a loop over all contacts. Within the loop, we use a conditional 
statement (`if`) to check if the name is 'Alice'. If so, print the phone 
number; otherwise print the name (`else` block).


~~~python
contacts = [
    {'name':'Alice', 'phone':'555-111-2222'},
    {'name':'Bob', 'phone':'555-333-4444'},
    ]
for c in contacts:
    if c['name'] == 'Alice':
        print(c['phone'])
    else:
        print(c['name'])
~~~
{:.text-document title="worksheet.py"}

~~~~{.python}
555-111-2222
Bob
~~~~~~~~~~~~~



===

## Exercise 4

Write a for loop that prints all even numbers between 1 and 9. Use the modulo
operator (`%`) to check for evenness: if `i` is even, then `i % 2`
returns `0`, because `%` gives the remainder after division of the first number by the second.