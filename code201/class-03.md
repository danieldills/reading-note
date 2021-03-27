## HTML Lists, Control Flow w/ JS, and the CSS Box Model

### Lists Chapter 3
There are three types of lists
- Ordered Lists each item list is numbered
- Unordered Lists lists that begin with bullet points
- Definition Lists made up of set of terms, including definitions of those terms

- Ordered Lists ```<ol>``` element
    - ```<li>``` each item is placed between tag

- Unordered Lists ```<ul>``` 
    - ```<li>``` each item is placed between tag

- Definition Lists ```<dl>```
    - ```<dt>``` each item is placed between tag

- Nested Lists capability of putting second list inside ```<li>``` element

### Boxes Chapter 13
Using CSS, each HTML element lives in its own box

- Box Dimensions width, height
- Limiting Width min-width, max-width
- Limiting Height min-height, max-height
- Overflowing Content informs browser what to do with the content in the event the content contained is larger than the box
- Border Width border-width
- Border Style border-style
- Border Color border-color
- Padding specifies how much space wshould appear between content and element
- Margin gap between boxes

### Chapter 2 Review
- Arrays special type of variable that stores list of values
- Creating an array ex. (provided by Duckett JS book)
var colors;
colors = ['white', 'black', 'custom'];

var el = document.getElementBYId('colors');
el.textContent = colors[0];

### Chapter 4 Decisions and Loops
- If...Else Statements allows you to provide two sets up code
- Switch Statements begins with variable called switch value, each case indicates a possible value for variable and code that should run if variable matches that value (Ducket JS Book)
- Loops check a conditon
- Loop Counters uses counter as a condition, instructs code to run a specified number of times

[<== Back](README.md)