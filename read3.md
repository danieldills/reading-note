# FileIO & Exceptions

## What is a File?

At its core, a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer. [source](https://realpython.com/read-write-files-python/)

Files are composed of three main parts [source](https://realpython.com/read-write-files-python/):

  1. Header: metadata about the contents of the file (file name, size, type, and so on)

  2. Data: contents of the file as written by the creator or editor

  3. End of file (EOF): special character that indicates the end of the file

## File Paths

When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

  1. Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)
  2. File Name: the actual name of the file
  3. Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

## Opening and Closing a File in Python

When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:

```python
file = open('dog_breeds.txt')
```

Once you open a file, don't forget to close it!

```python
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```

## Python Exceptions: An Introduction

A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception. In this article, you will see what an exception is and how it differs from a syntax error. After that, you will learn about raising exceptions and making assertions. Then, you’ll finish with a demonstration of the try and except block. [source](https://realpython.com/python-exceptions/)

## Exceptions versus Syntax Errors

Syntax errors occur when the parser detects an incorrect statement. Observe the following example [source](https://realpython.com/python-exceptions/):

```python
>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax
```

The arrow indicates where the parser ran into the syntax error. In this example, there was one bracket too many. Remove it and run your code again:

```python
>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
```

### Raising an Exception

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

If you want to throw an error when a certain condition occurs using raise, you could go about it like this [source](https://realpython.com/python-exceptions/):

```python
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```
