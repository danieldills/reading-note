## Putting it all together
[source](https://reactjs.org/docs/thinking-in-react.html)

### Step 1: Break UI Into A Component Hierarchy

- Single responsibility principle: components should only do one thing, if they are changing, it should be composed into smaller subcomponents

### Step 2: Build A Static Version in React

- Build a static version of your app that renders your data model, you'll build components that resuse other components and pass data using props. Props area  way of passing data from a parent to child. State not needed because state is interactive, static version isn't necessary.

### Step 3: Identify The Minimal (but complete) Representation of UI State

- To make UI interactive, changes need to be triggered to the underlying data model. React achieves this with state.

### Step 4: Identify Where Your State Should Live

- Identify every component that renders something based on that state

- Find a common owner of the component (a single component above all the components that need the state in the hierarchy).

- Either the common ownder or another component higher up in the hierarchy should own the state.

If you can't find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

Step 5: Add Inverse Data Flow

- Information can be passed from child to parent using a function, form components deep in the hierarchy need to update the state in parent components. Think about what you want to happen, and use accordingly. 

[<== Back](README.md)
