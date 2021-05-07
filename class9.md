# Functional Programming

What is functional programming? 

- Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data [source](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

  What is pure function?

- It returns the same result if given the same arguments (it is also referred as deterministic)
- It does not cause any observable side effects [source](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

It returns the same result if given the same arguments!

What are the benefits of pure functions?

The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:

- Given a parameter A → expect the function to return value B

- Given a parameter C → expect the function to return value D
[source](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

What is immutability?

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value. [source](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

What is referential transparency?

The expression referential transparency is used in various domains, such as mathematics, logic, linguistics, philosophy and programming. It has quite different meanings in each of these domain. [source](https://www.sitepoint.com/what-is-referential-transparency/)

[<== Back](README.md)
