## 8th Session: Working with Modules in Python

## What is a Module

- Modules refer to a file containing Python statements and definitions
- We use modules to break down large programs into small manageable and organised files. Furthermore, modules provide reusability of code

----

## How Python finds Modules

While importing a module, Python looks at several places. Interpreter first looks for a built-in module. Then(if built-in module not found), Python looks into a list of directories defined in sys.path. The search is in this order.

- The current directory.
- PYTHONPATH (an environment variable with a list of directories).
- The installation-dependent default directory.

----

### The sys module

```python
# The Python sys module provides functions and variables used to
# manipulate different parts of the Python runtime environment 

# First, we have to import the sys module
import sys 

# importing sys.path
print(sys.path)

# If your code has import sys - then it can use the functionality and data in it by using terms such as :
sys.argv : Returns a list of command line arguments passed to a Python script
sys.exit() : Causes the sceipt to exit back to the Python console or the command prompt
sys.version : Prints a string with the current Python version number
sys.maxsize : Returns the largest integer a variable can take
sys.path : This is an environment variable that is a search path for all Python modules

```

----

## Import statement

We can import the functions, classes defined in a module to another module using the **import statement** in some other Python source file.

```python
# Syntax 
import module_name

# Example 
# Importing  module calc.py
import calc
 
print(calc.add(10, 2)
```

### Importing and renaming a module - using as keyword

```python
# importing sqrt() and factorial from the module math
import math as nevermind
 
# if we simply do "import math", then 
# math.sqrt(16) and math.factorial() are required.
print(nevermind.sqrt(16)) # Ouputs 4
print(nevermind.factorial(6)) # Ouputs 720
```


### The from import statement

Python’s *from* statement lets you import specific attributes from a module without importing the module as a whole.

```python
# Example - importing specific attributes from the module

# importing sqrt() and factorial from the module math
from math import sqrt, factorial
 
# if we simply do "import math", then 
# math.sqrt(16) and math.factorial() are required.
print(sqrt(16)) # Ouputs 4
print(factorial(6)) # Ouputs 720
```

### The import * statement

The * symbol used with the from import statement is used to import all the names from a module to a current namespace.

```python
# Syntax 
from module_name import *

# Example 
from math import *
```

----


## Importing one file into another

```python
import file_name 

# To get the Class and its attributes and methods
file_name.class_name 
```

- **We have a file called car.py**

```python
# In the car.py file
# In the car.py file

# Create a vehicle class
class Vehicle:

    # class attribute (properties)
    type = "sportscar"

    # instance attribute (properties)
    def __init__(self, model, speed, colour, rim_colour):
        self.model = model
        self.speed = speed
        self.colour = colour
        self.rim_colour = rim_colour

    # instance method (behaviour)
    def drift(self):
        return "{} can drift".format(self.model)

    def accelerate(self):
        return "{} can go up to {}".format(self.model, self.speed)

# Create an instance of the Vehicle class
ferrari = Vehicle("ferrari", 200, "red", "black")

# Call the class attributes 
print("This car is a {}".format(ferrari.__class__.type))

# Call the instance attributes 
print("{} is {} in colour and can go up to {}mph".format(ferrari.model, ferrari.colour, ferrari.speed))

# Printing the methods 
print(ferrari.drift())
print(ferrari.accelerate())
```

- **We create a new file [app.py](http://app.py) and here we want to access the Vehicle class and it’s attributes and methods here**

```python
# In the app.py file 

# Importing the Vehicle class in the car.py to this file 
import car

# Access the Vehicle Class from the car.py file
clio = car.Vehicle("renault", 180, "blue", "red")
print(clio.model)

# If we do not want the statements in the previous file to print
if __name__ == "__car__":
   Do something here
```

----


## The dir() function

We can use the `dir()` function to find out names that are defined inside a module, it returns all the properties and methods of the specified object, without the values.

```python
# Syntax
dir(object_name)
```