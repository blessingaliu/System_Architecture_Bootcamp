## 1st session: Fundamentals of coding with Python

## Python

- An interpreted high level and general programming language
- Can be used on a server to create web applications
- Can be used alongside software to create workflows
- Python relies on indentation

## IDE (Integrated Development Environment)

- VSCode
- PyCharm
- Google Colab (alternative to Jupyter notebook)

## Objects

- Every entity is an object
- Each object is allocated some space in memory and each object has a type (data type) and some value
- You can check the type of an object using object()

## Built-in Data types

**Text type** - String

**Numeric type** - Integer, Float, Complex

**Sequence type** - List, Tuple, Range

**Mapping type** - Dict

**Set type** - Set, Frozenset

**Boolean type** - Bool

**Binary type** - Bytes, ByteArray, Memoryview

- **String** - “This is a string”
- **Integer** - 3, 6 (whole numbers)
- **Float** - 1.332, 5.6 (decimal numbers)
- **Boolean** - True or False
- **Complex number** is a number that can be written in the form of (a+b j) where a and b are real numbers, j is an imaginary number.

```powershell
# Example of a Complex 
The Number is:
(3+2j)

Data type of Number is:
<class 'complex'>
```

- You can get the data type of any object by using the `type()` function:

```python
type(10)
<class 'int'>

type(4.2)
<class 'float'>

type(2+3j)
<class 'complex'>

type('I am too.')
<class 'str'>

type(True)
<class 'bool'>
```

## Expressions

- You can combine objects with operators like + and - to form expressions
- A sequence of operands and operators, like `a + b - 5`
, is called an expression.

### **Arithmetic operators**

- **Order of operators follows BIDMAS**

**Addition** - Sum of two a and b

```python
# Operator sign +(binary)
a + b
```

**Subtraction** - b subtracted from a 

```python
# Operator sign -(binary)
a - b
```

**Multiplication** - Product of a and b

```python
# Operator sign *
a * b
```

**Division** - Quotient when a is divided by b, the result is always a float.

```python
# Operator sign /
a / b
```

**Modulo** - The remainder when a is divided by b

```python
# Operator sign %
a % b
```

**Floor Division** - Quotient when a is divided by b, which is rounded down

```python
# Operator sign //
a // b
```

**Exponentiation** - a is raised to the power of b

```python
# Operator sign **
a ** b
```

> "python" + 3

TypeError: can only concatenate str (not "int") to str

- You can only add two strings together, you cannot add a string to an integer
> 

### Comparison operators

Comparison operators are used to compare values. It returns either `True` or `False` according to the condition.

### Logical operators

Logical operators are the `and`, `or`, `not` operators.

## Variables Naming

- Use PEP8 style guide
- Variable names can contain letters, numbers and underscore
- Variable names cannot contain spaces
- Variable names cannot start with a number
- Python is case sensitive - separated by underscores
- There are a list of reserved words in python that cannot be used as variable names

## Variables

- A Variable is a name that refers to an object
- One of the main purposes of a variable is to remember a value from one part of a program so that it can be used in another part of the program
- We can assign an object to a variable with an assignment operator (=)
- Double equals (==) checks for equality

## Printing

- The print function requires parenthesis around its arguments

```powershell
print('3+4') // outputs 3+4
print(3+4) // outputs 7
```

- To print several things at once, separate them by commas. Python will automatically insert spaces between them.

```python
print('The value of 3+4 is', 3+4) 

// outputs The value of 3+4 is 7
```

## Inputs

- An input function is a simple way for your program to get information from people using your program

```python
name = input("Enter your name: ")

<variable name> = input("Message")
```

- using **fstrings**

```python
Literal String Interpolation or more commonly as F-strings

To create an f-string, prefix the string with the letter “ f ”. 
The string itself can be formatted in much the same way that you would with str.format().

# This is a program that asks for user name and prints it using a fstring

name = input("Please enter your name: ")
print(f"Welcome, {name}")
```

- Input functions (user input) are always stored as a string
- **To store it as a integer, wrap it in an integer function**
```python
age = int(input("Enter your age: "))
print(f"You are {age}, you are too old")
```