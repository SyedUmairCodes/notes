# Introduction to Python

Python is a high-level general purpose programming language used to build all kinds of websites and applications, having a major use-case in Artificial Intelligence.

Python code is written in UTF-8 formatted plain text files that end with the `.py` extension so that the code editor and the Python interpreter can understand which files are to be treated as Python source code files.

> The simplest program that you can write in any programming language including Python is to print the statement `Hello World!` on the screen or the console/command line of your computer.

In Python, you use the built-in `print()` function that comes with almost all version of Python version 3 and will print whatever you have written between the parenthesis of the print function to your console.

Code editors and IDEs like Visual Studio code and Jetbrains Pycharm are built with the functionality of syntax highlighting that means that each part of your code will be a different color if it's written correctly so that you can easily distinguish a variable from a function.

## Commenting code

Comments are used to add notes and provide context about the code that you have wrote. It can be extremely useful if you are working with a team or are working on a big project.

In Python, comments start with the `#` symbol and are ignored by the interpreter when the code is run. The main reason to write comments is to explain what your code is supposed to do and how you are making it work.

## The Zen of Python

The Zen of Python are philosophical principles written by Tim Peters that the Python community follows when writing Python code. Following these principles makes your code pythonic.

> They are available in the official documentation and the IDLE editor that comes with default Python installs as well.

## Variables

A variable is like a container. Every variable has a value that has been assigned to it and whenever you use the variable the value that was assigned to it will actually be used. A variable's value can be changed dynamically through code and it will hold the last value that was assigned to it.

> Python allows you to assign more than one variable in a single line by separating their names and values with commas.

```Python
name, age, gender = "John", 12, "male"
```

### Naming Constraints

In Python, there are a few rules that need to be followed when you're working with variables so that your code is easier to read and doesn't cause unnecessary errors. The name of a variable can only contain numbers, letters, and underscores and must start with an underscore or a letter and not a number.

If you're variable name contains two words then join them together with a underscore because spaces shouldn't be used in variable names since adding a space makes them two different words. Python comes with some restricted keywords that are used in programming and those words can't be used as the name of a variable since Python has assigned a special function to them already.

### Constant Variables

In Python, and other programming languages, constant variables are variables whose values cannot be changed once they have been declared. Any variable whose name is written in all capital letters will be treated as a constant variable in Python.

```Python
 VALUE_OF_PI = 3.14
```

---