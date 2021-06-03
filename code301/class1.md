## Introduction to React and Components

### What is React?
"React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”." [source](https://reactjs.org/tutorial/tutorial.html)

### Hello World!
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
- React is a JavaScript library

### Introducing JSX
"Consider the variable declaration:
```
const element = <h1> Hello, world!</h1>;
```
This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.

JSX produces React “elements”. We will explore rendering them to the DOM in the next section. Below, you can find the basics of JSX necessary to get you started." [source](https://reactjs.org/docs/introducing-jsx.html)

### Rendering Elements
- React elements are plain objects
- React DOM takes care of updating the DOM to match the React elements
- To render a React element into a root DOM node, pass both to ReactDom.render():

```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
- React elements are immutable
- React only updates what's necessary

### Components and Props
[source](https://reactjs.org/docs/components-and-props.html)

- Components let you split the UI into independent, resuable pieces and think about each piece in isolation
- Rendering a Component
    - When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”
- Composing Components
    - Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

[<== Back](README.md)