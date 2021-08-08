# Python Regular Expression

```import re```

Basic Patterns: Ordinary Characters

You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

Examples are 'A', 'a', 'X', '5'.

Ordinary characters can be used to perform simple exact matches:

```py
pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")
```

Match!

The ```match()``` function returns a match object if the text matches the pattern. Otherwise, it returns ```None```.

The + symbol used after the \d in the example above is used for repetition. You will see this in some more detail in the repetition section later on...

```\t``` - Lowercase t. Matches tab.
```\n``` - Lowercase n. Matches newline.
```\r``` - Lowercase r. Matches return.
```\A``` - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.
```\Z``` - Uppercase z. Matches only at the end of the string.
```\b``` - Lowercase b. Matches only the beginning or end of the word.
