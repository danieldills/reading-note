# Game of Greed 3: List Comprehensions

List comprehension provide a concise way to create lists.

Old:

```py
new_list = []
for i in old_list:
    if filter(i):
        new_list.append(expressions(i))
```

New:

```py
new_list = [expression(i) for i in old_list if filter(i)]
```

new:

```py
[ expression for item in list if conditional ]
```

old:

```py
for item in list:
    if conditional:
        expression
```

Creating a list:

```py
x = [i for i in range(10)]
print x

# This will give the output:
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Create a list using loops and list comprehension:

```py
# You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Multiplying parts of a list:

```py
list1 = [3,4,5]
 
multiplied = [item*3 for item in list1] 
 
print multiplied 
[9,12,15]
```

Show the first letter of each word:

```py
listOfWords = ["this","is","a","list","of","words"]

items = [ word[0] for word in listOfWords ]

print items
```

[source](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python) for the above code can be found here.
