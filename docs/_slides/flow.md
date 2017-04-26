---
---

## Loops and conditionals

A `for` loop takes any "iterable" object and executes a block of code once for each
element of the list.


~~~python
squares = []
for i in range(1, 5):
    j = i ** 2
    squares.append(j)
~~~
{:.text-document title="worksheet.py"}



~~~python
>>> squares
[1, 4, 9, 16]

~~~
{:.output}



The `range(i, j)` function creates a list of integers from `i` up through `j - 1`; just
like in the case of list slices, the upper bound is excluded. 

===

Note the pattern of the block above: the `for` statement is followed by a colon,
each line in the following block is indented at the same level, and there is no
delimiter or statement indicating the end of the block.

Compared with other programming languages where code indentation only serves to
enhance readability, code blocks in Python are defined **only** by changes in
indentation.

===

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

Write a loop that prints all even numbers between 1 and 9 using the modulo
operator (`%`) to check for evenness. If `i` is even, then `i % 2`
returns `0`, because `%` gives the remainder after division of the first number by the second.