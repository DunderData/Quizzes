# Python Quiz Solutions

This page contains the solutions to the Python quizzes. They will be posted 24 hours after the quiz is announced. The quizzes will be tagged with **#PythonQuiz** on social media to help identify them.

### Complete the Quiz

Quizzes may be completed in the Jupyter Notebooks available in this repository. You can either download them directly from here or use this link below courtesy of Binder to run a remote Jupyter Notebook.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DunderData/Quizzes/master)

### Become an Expert

If you are looking for a comprehensive path to help you become an expert at the python data science ecosystem, you might want to check out the following books I wrote.

* [Exercise Python][3]
* [Master Data Analysis with Python][4]
* [Master Machine Learning with Python][5]

### Take a live in-person class with me

Learn directly with me by taking an interactive and fun [in-person bootcamp in Toronto, Houston, New York City, Boston, or Chicago in 2020][6].

### Get started for free

Sample my material by taking my [free Intro to Pandas class][7].

[1]: twitter.com/tedpetrou
[2]: linkedin.com/in/tedpetrou
[3]: https://www.dunderdata.com/exercise-python
[4]: https://www.dunderdata.com/master-data-analysis-with-python
[5]: https://www.dunderdata.com/master-machine-learning-with-python
[6]: https://www.dunderdata.com/all-in-person-courses
[7]: https://www.dunderdata.com

## Quiz #1 - January 28, 2020

Take a look at the following two function definitions.

```python
def func1():
    return 5

def func2():
    return(5)
```

In `func1`, `return` is not a function, while in `func2` it is a function. True or False?

### Solution - January 29, 2020

**`False`** - `return` is not a function. It is always a **statement**. It is [detailed here in the official documentation][1]. Placing parentheses after it does not change what part of the language it is. See the [Python Language Reference][2] for more detail.

#### The different meaning of parentheses

Both `func1` and `func2` use the `return` statement to return the integer 5. In `func2`, the line `return(5)` is interpreted as `return` and then `(5)`. The parentheses here are the same parentheses that are used to control the order of execution. Take the expression `3 * (4 + 5)`. The parentheses mean "do the operation `4 + 5` first. With the expression `(5)` there are no operations so it evaluates as `5` and `return(5)` becomes `return 5`.

Parentheses have a completely different meaning when used to call a function. For instance, when we write `func1()`, the parentheses mean "execute the code that the function `func1` references". Most of the time, when you see parentheses appended to a word in Python, then that word is a function. But, in the case of `return`, this isn't so. `return` is not a function. It signals to Python to return the expression that immediately follows it. In this example, the expression is very simple, just `(5)`.

[1]: https://docs.python.org/3/reference/simple_stmts.html#grammar-token-return-stmt
[2]: https://docs.python.org/3/reference/index.html

---

## Quiz #2 - January 29, 2020 - difficulty (2/4)

Take a look at the following function definition.

```python
def func():
    return()
```

What is the result of executing `func()`?

a) `None`  
b) An error  
c) Tuple  
d) 0

### Solution - January 30, 2020

This function's single line, `return()`, is quite bizarre. It appears that `return` is a function and being called. From the previous quiz, we learned that `return` is never a function and python will interpret the line as `return` followed by `()`. So, what does `()` do? It creates an empty tuple, which is then returned from the function. We verify this below by defining the function, calling it, assigning the result to a variable, outputting this value, and obtaining it's type.

```python
>>> def func():
>>>    return()
>>> a = func()
>>> type(a)
tuple
```