# Testing and Modules

## In Tests We Trust -- TDD with Python

- Unit tests are some pieces of code to exercise the input, and the output and the bahavior of the code. [source](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

- In the article, the author is attempting to write code that using an API, will predict gender using a name as reference.
  - Input [name]
  - Output [gender]

- When writing tests, there are important aspects to consider 

- AAA
  - Arrange: you need to organize the data needed to execute that piece of code (input);

  - Act: here you will execute the code being tested (exercise the behaviour);
  
  - Assert: after executing the code, you will check if the result (output) is the same as you were expecting.
[source](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

The cycle is made by three steps [source](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932):

- Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

- Write the feature and make the test pass! (you can dance after that)

- Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

## Recursion

- What is Recursion?
  A recursive function is a function defined in terms of itself via self-referential expressions.

  This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. [source](https://realpython.com/python-thinking-recursively/)

- What are the disadvantages of recursive programming over iterative programming?
  Note that both recursive and iterative programs have the same problem-solving powers, i.e., every recursive program can be written iteratively and vice versa is also true. The recursive program has greater space requirements than iterative program as all functions will remain in the stack until the base case is reached. [source](https://www.geeksforgeeks.org/recursion/)

- What are the advantages of recursive programming over iterative programming?
  Recursion provides a clean and simple way to write code. [source](https://www.geeksforgeeks.org/recursion/)
