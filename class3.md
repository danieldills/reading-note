## Passing Functions as Props

### Lifting State Up
"Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. Let’s see how this works in action." 

"There should be a single “source of truth” for any data that changes in a React application. Usually, the state is first added to the component that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor. Instead of trying to sync the state between different components, you should rely on the top-down data flow."[source](https://reactjs.org/docs/lifting-state-up.html)

### Lists and Keys
Given the code below, we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it:
```
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);
```

### The Spread Operator
JavaScript spread syntax refers to the use of ellipsis of three dots ```...``` to expand an iterable object into the list of arguments

```
Math.max(1,3,5) // 5
Math.max([1,3,5]) // NaN
```
using ```...```
```Math.max(...[1,3,5]) // 5```
The spread syntax spreads the array into separate arguments.
[source](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

[<== Back](README.md)