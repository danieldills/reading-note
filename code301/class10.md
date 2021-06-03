# In memory storage

What is a 'call'?

- The call stack is primarily used for function invocation (call). [source](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

How many 'calls' can happen at once?

- Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom.

What does LIFO mean?

- When we say that the call stack, operates by the data structure principle of Last In, First Out, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns. [source](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

```sh
function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();
```

What causes a Stack Overflow?

- A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error. [source](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

What is a ‘refrence error’?

- This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

```sh
console.log(foo) // Uncaught ReferenceError: foo is not defined
```

What is a ‘syntax error’?

- A syntax error occurs when information is entered into a computer in an unrecognizable or improper format. [source](https://www.easytechjunkie.com/what-is-a-syntax-error.htm)

What is a ‘range error’?

- Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

```sh
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```

[source](https://www.easytechjunkie.com/what-is-a-syntax-error.htm)

What is a ‘type error’?

- Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable. [source](https://www.easytechjunkie.com/what-is-a-syntax-error.htm)

[<== Back](README.md)
