## ES6 Classes

[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
### Inheritance

- JavaScript only has one construct: objects. 

- Each object has a private property which holds a link to another object called its prototype. 

- That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. 

- By definition, null has no prototype, and acts as the final link in this prototype chain.

- Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.

### This
[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

- A function's this keyword behaves a little differently in JavaScript compared to other languages. 

- The behavior of this in classes and functions is similar, since classes are functions under the hood. But there are some differences and caveats.

```
class Example {
  constructor() {
    const proto = Object.getPrototypeOf(this);
    console.log(Object.getOwnPropertyNames(proto));
  }
  first(){}
  second(){}
  static third(){}
}

new Example(); // ['constructor', 'first', 'second']
```
- Constructor: When a function is used as a constructor (with the new keyword), its this is bound to the new object being constructed.

### Classes
[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

- Classes are a template for creating objects. They encapsulate data with code to work on that data. 
- Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

- Class declarations

```
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```
- Hoisting

```
const p = new Rectangle(); // ReferenceError

class Rectangle {}
```

[<== Back](README.md)