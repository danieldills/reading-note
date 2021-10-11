# React 1: ES6 Syntax and Feature Overview

Legend

Variable: x
Object: obj
Array: arr
Function: func
Parameter, method: a, b, c
String: str

Variables declaration

ES5

```javascript
var x = 0;
```

ES6

```javascript
let x = 0;
```

Constant declaration
ES6 introduced the const keyword, which cannot be redeclared or reassigned, but is not immutable.

```javascript
const CONST_IDENTIFIER = 0; // constants are uppercase by convention
```

Arrow functions

The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

ES5

```javascript
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {}; // function expression
```

ES6

```javascript
let func = (a) => {}; // parentheses optional with one parameter
let func = (a, b, c) => {}; // parentheses required with multiple parameters
```

Template Literals

Concatenation/string interpolation
Expressions can be embedded in template literal strings.

ES5

```javascript
var str = "Release date: " + date;
```

ES6

```javascript
let str = `Release Date: ${date}`;
```

Multi-line strings

Using template literal syntax, a JavaScript string can span multiple lines without the need for concatenation.

ES5

```javascript
var str = "This text " + "is on " + "multiple lines";
```

ES6

```javascript
let str = `This text
            is on
            multiple lines`;
```

Note: Whitespace is preserved in multi-line template literals.

# React 1

[source](https://reactjs.org/docs/hello-world.html)

## Introducing JSX

Consider this variable declaration:

```javascript
const element = <h1>Hello, world!</h1>;
```

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started.

Why JSX?
React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.

## Embedding Expressions in JSX

```javascript
const name = "Josh Perez";
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(element, document.getElementById("root"));
```

You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.

In the example below, we embed the result of calling a JavaScript function, formatName(user), into an <h1> element.

```javascript
function formatName(user) {
  return user.firstName + " " + user.lastName;
}

const user = {
  firstName: "Harper",
  lastName: "Perez",
};

const element = <h1>Hello, {formatName(user)}!</h1>;

ReactDOM.render(element, document.getElementById("root"));
```

Rendering Elements
Elements are the smallest building blocks of React apps.

An element describes what you want to see on the screen:

```javascript
const element = <h1>Hello, world</h1>;
```

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
