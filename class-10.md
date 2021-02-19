## Error Handling & Debugging Chapter 10

- Order of Execution to find source of error, it's important to know how scripts are processed
- Execution Context

Every statement in a script lives in one of three execution contexts:
1. Global Context code that is in the script, but not in a function. There is only one global context in any page
1. Function Context code that is being run within a function. Each function has its own function context.
1. Eval Context text is executed like code in an internal function called eval()

- Variable Scope first two execution contexts correspond with the notion of scope
1. Global Scope if variable is declared outside function, it can be used anywhere, if you don't use var keyword when creating a variable, it is placed in global scope
1. Function-level scope when variable is declared within a function, it can only be used within the function, making it local

### Execution Context & Hoisting (pg 457)
Each time a script enters a new execution context, there are two phases of activity
- Prepare
    - new scope is created
    - variables, functions, and arguments are created
- Execute
    - now it can assign values to variables
    - reference functions and run their code
    - execute statements

- Understanding Scope
In the interpreter, each execution context has its own variables object. It holds the variables, functions, and parameters available within it. Each execution context can also access its parents variables object

- Understanding Errors
If a JavaScript statement generates an error, then it throws an exception. At that point, the interpreter stops and looks for exception-handling code.
- Error Objects can help find mistakes, browsers help you read them - think console

Error Object is created it will contain the following properties: 
1. name
2. message
3. fileNumber
4. lineNumber

JavaScript built-in error objects:
- Error generic error
- SyntaxError Syntax has not been followed
- ReferenceError tried to reference a variable that is not declared/ within scope
- TypeError unexpected data type that cannot be coerced
- RangeError numbers not in acceptable range
- URIError encodeURI(), decodeURI(), and similar methods used incorrectly
- EvalError eval() function used incorrectly

[<== Back](README.md)
