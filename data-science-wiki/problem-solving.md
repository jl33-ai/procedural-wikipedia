
###### Created by @jl33-ai 👦🏻

This guide is meant to serve as a reference for problem-solving techniques that can help you when faced with a difficult challenge in your coding projects. Remember that problem-solving is more of an art 🎨 than a science 🧪, but these steps can serve as a useful guide.

## Table of Contents 🗂️

- [1. Identify](#Identify-the-Problem-🔍)
- [2. Define](#Define-the-Problem-📝)
- [3. Analyze](#Analyze-the-Problem-🧐)
- [4. Generate Solutions](#Generate-Solutions-💡)
- [5. Decision Making](#Decision-Making-🎯)
- [6. Implement Solution](#Implement-Solution-🛠️)
- [7. Review](#Review-🔄)

---
## Identify the Problem 🔍

- The first step is to identify that there is a problem. This may come in the form of an error message, incorrect output, a system crash or non-functioning feature.

```python
>>> print(variableThatIsNotDeclared)

NameError: name 'variableThatIsNotDeclared' is not defined
```
---

## Define the Problem 📝

- Clearly and specifically define the problem. Try to understand what you are trying to achieve, and what is stopping you from achieving it. 

- For instance, if a function is not behaving as intended, you might state the problem as follows: "The function `calculateSum()` is not correctly adding all the elements in the list".

---

## Analyze the Problem 🧐

- Break the problem down into smaller manageable parts.
- You may use debugging tools and techniques such as `print()` statements, breakpoints, or logs.

```python
def calculateSum(myList):
    result = 0
    for element in myList:
        print(f'Result before adding {element}: {result}') # Debugging statement
        result += element
    return result
```

---

## Generate Solutions 💡

- Brainstorm 🧠 possible solutions. Don't worry at this point about if they are possible or practical.

- Try to think in different ways. For instance, if an algorithm is slow, could you use a different data structure? Or a different approach altogether?

- Feel free to research similar problems others have encountered. Sites like Stack Overflow are great for this.

---

## Decision Making 🎯

- Choose the best solution among the ones devised.

- Weigh 👀 the pros and cons. Consider factors such as whether the solution is practical, whether it is likely to work, how long it might take, and whether there are any potential side effects.

---

## Implement Solution 🛠️

- This is the step where you write code 👨‍💻. 
- Document your code well with comments.

```python
# Corrected the algorithm for summing elements in the list
def calculateSum(myList):
    return sum(myList)
```

---

## Review 🔄

- Test your solution thoroughly to ensure it works as expected. Include edge cases, error cases, large inputs, etc.
- Did it solve the problem? If not, go back to analyzing the problem and generating solutions.

---
