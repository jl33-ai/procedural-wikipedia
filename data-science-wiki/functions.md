
**Created by @jl33-ai 👦🏻**

---

## Table of Contents

1. [Introduction](#introduction) 👋
2. [Defining a Function](#defining-a-function) ✍️
3. [Calling a Function](#calling-a-function) 📞
4. [Function Arguments](#function-arguments) 💼
5. [Return Values](#return-values) 💡
6. [Lambda Functions](#lambda-functions) 🚀
7. [Conclusion](#conclusion) ❗

---

<a name="introduction"></a>
## Introduction 👋

Hello there! This guide covers the basics and importance of **Functions** in Python. Functions are reusable pieces of programs. They allow you to give a name to a block of statements, allowing you to run that block using the specified name anywhere in your program.

---

<a name="defining-a-function"></a>
## Defining a Function ✍️

Functions in Python are defined using the keyword `def`. Here's an example:

```python
def my_function():
    print("Hello, World!")
```

In this example, `my_function` is the function name, while `print("Hello, World!")` is the function body.

---

<a name="calling-a-function"></a>
## Calling a Function 📞

After defining a function, you must call it to execute. Use the function name followed by parentheses to call it.

```python
my_function()  # outputs "Hello, World!"
```

---

<a name="function-arguments"></a>
## Function Arguments 💼

Functions can also take arguments, which are values you supply to the function so it can perform operations using those values. Here's how we define a function with arguments:

```python
def greet(name):
    print(f"Hello, {name}")
```

---

<a name="return-values"></a>
## Return Values 💡

A function can return a value that you can use elsewhere in your code. Use the `return` keyword:

```python
def square(number):
    return number * number

print(square(3))  # outputs 9
```

---

<a name="lambda-functions"></a>
## Lambda Functions 🚀

Python supports the creation of anonymous functions (i.e., functions that are not bound to a name), using the `lambda` keyword.

```python
square = lambda x: x * x
print(square(5))  # outputs 25
```

---

<a name="conclusion"></a>
## Conclusion ❗

Functions in Python provide organized, reusable and modular code to perform a set of specific actions. Functions improve modularity of your code, your reusability of code, and your code readability.

---
