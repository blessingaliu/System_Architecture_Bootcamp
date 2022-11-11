## 4th Session: Fundamentals of coding with Python continued - Dictionaries, Conditional statements and  Functions


## Dictionaries { }

- Dictionaries are used to store data values in **key:value pairs**.
- A dictionary is a collection which is **ordered**, **changeable** and **do not allow duplicates**.
- You cannot have two items with the same key in a dictionary

```python
# Dictionary Syntax
dictionary = {
	"Key": Value, 
	"Key": Value, 
	"Key": Value
}

# Example of a Dictionary 
my_dict = {
	"city": "London", 
	"food": "Sherperds pie", 
	"year": 2021,
	"languages": ["javascript", "python", "ruby"],
	"finished_all_udemy_courses": False
}

print(len(my_dict)) # Prints the number of items in the dictionary 
# Outputs 5

print(type(my_dict)) # Prints the data type of the dictionary
# Outputs <class 'dict'>

# Returns the value of the key specified
my_dict.get("Key")

OR 

my_dict["Key"]["Nested Key"]

# Print out all the values 
my_dict.values()

# Print out all the keys
my_dict.keys()

# Print out everything in the dictionary
my_dict.items()

# Changing value of any item in dictionary
my_dict["Key"] = new_value

# Remove any key and value in the dictionary
my_dict.pop("Key")

```

### **Accessing dictionary items**

- **dictionary_name[”key”]**
- **dictionary_name.get(”key”)**

```python
# Accessing items in a dictionary by referring to its key name
my_dict = {
	"city": "London", 
	"food": "Sherperds pie", 
	"year": 2021,
	"languages": ["javascript", "python", "ruby"],
	"finished_all_udemy_courses": False
}

my_dict["city"]
# Ouputs London

# Access items in a nested dictionary
cars = {
"car1" : {"brand": "Dodge", "model": "Black Mamba", "year": 2019},
"car2" : {"brand": "Mercedes", "model": "Classics", "year": 1905},
"car3" : {"brand": "Tesla", "model": "CS50", "year": 2025}
}

for i in cars["car1"].items():
  print(i)

# Outputs
('brand', 'Dodge')
('model', 'Black Mamba')
('year', 2019)
```

### **Accessing dictionary items**

- **dictionary_name[”key”] =  New value**
- **dictionary_name.update({”key”: new value})**

```python
# This is also a way to add new items to the dictionary by 
# adding a new key and value 
my_dict["food"] = "Spaghetti bolognese"
print(my_dict)
# Outputs 
{'city': 'London', 'food': 'Spaghetti bolognese', 'year': 2021, 'languages': ['javascript', 'python', 'ruby'], 'finished_all_udemy_courses': False}

# This is used to update the dictionary 
my_dict.update({"year": 2022})
print(my_dict)
# Outputs 
{'city': 'London', 'food': 'Spaghetti bolognese', 'year': 2022, 'languages': ['javascript', 'python', 'ruby'], 'finished_all_udemy_courses': False}
```

### Removing **dictionary items**

- **dictionary_name.pop(”key”)** (removes the item with the specified key name)
- **dictionary_name.popitem()** (removes the last inserted item)
- **del dictionary_name[”key”]** (removes the item with the specified key name)
- **del dictionary_name** (can also delete the dictionary completely)
- **dictionary_name.clear()** (this empties the dictionary)


### Looping through a dictionary

```python
# Print all key names in the dictionary, one by one:
for i in thisdict:
  print(i)

# Print all values in the dictionary, one by one:
for i in thisdict:
  print(thisdict[i])

# Use the values() method to return values of a dictionary:
for i in thisdict.values():
  print(i)

# Use the keys() method to return the keys of a dictionary:
for x in thisdict.keys():
  print(x)

# Loop through both keys and values, by using the items() method:
for x, y in thisdict.items():
  print(x, y)

```

-----------------------------------------------------------------------------------------------------------

## Conditional expressions (if statements)

- If <expr> is true, then <statement> is executed. If <expr> is false, then <statement> is skipped over and not executed.
- <expr> is a condition that needs to be checked

```python
# Syntax: relies on indentation
if <expr>:
	<statement>

# Create variables called bank_balance = 10 and access_code = “niyo”, or set to whatever you like.
# Create a program that asks the user to input price of product and access code, 
# and prints ‘Card declined’ if the bank_balance is less than price of product OR the access_code is not equal to “niyo”
# otherwise program prints “Payment Accepted”

bank_balance = 10
access_code = "niyo"

user_input_price = int(input("Enter the price of product: "))
user_input_access_code = input("Enter the access code: ")

if bank_balance < user_input_price:
  print("Card declined")
elif user_input_access_code != "niyo":
  print("Card declined")
else:
  print("Payment Accepted")

# Write a program that stores your name as a variable.
# Write an ‘if statement’ that prints ‘access denied’ if your name variable does not equal ‘John’.
# If the name variable equals ‘John’, then the program should print ‘Welcome John. How are you?’

user_name = input("Enter your name: ")
if user_name != "John":
  print("access denied")
else:
  print("Welcome John")
```

-----------------------------------------------------------------------------------------------------------

## for loop

- A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).
- With the **break** statement we can stop the loop before it has looped through all the items
- With the **continue** statement we can stop the current iteration of the loop, and continue with the next:

```python
**range(start, stop, step)**

# print all odd numbers from 1 to 20 (2 is to skip each other number) 
for i in range(1, 20, 2):
  print(i)

****
# Using for loop through items in a list 
list = [1, 3, 5, 5, 6, 7]
for i in list:
	print(i**2)

# Create a sequence of numbers from 0 to 10, and print each item in the sequence:
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
for x in numbers:
  print(x)

# Write a program that will print ‘A’, then ‘B’, then it will 
# alternate C's and D's five times and then finish with the letter E once.

print("A")
print("B")
for i in range(5):
  print("C")
  print("D")
print("E")
```

-----------------------------------------------------------------------------------------------------------

### Print statement vs Return statement

- **The print() function writes, i.e., "prints" a python object (a string or a number) on the console.**
- `print` just shows the human user a string representing what is going on inside the computer, the computer cannot make use of that printing.
- Printing has no effect on the ongoing execution of a program. It doesn’t assign a value to a variable. It doesn’t return a value from a function call.
- **Return is used to return a value from a function and exit the function**
- All functions will return a value, and if there is no `return`
 statement it will return `None`. The value that is returned by a function can then be further used as an argument passed to another function, stored as a variable, or just printed for the benefit of the human user.

## Functions

- A function is a ready-made building block of code that you can just reuse in your program
- A return statement by itself can be used to end a function early

```python
# Creating a function syntax 
def my_function(parameter):
  print("This is a function")

# Calling a function 
my_function(argument)

# An argument is the value that is sent to the function when it is called.

# A parameter is the variable listed inside the parentheses in the function definition.
```

-----------------------------------------------------------------------------------------------------------


### Error handling (try and except)

- The `try` block lets you test a block of code for errors. If an exception is raised, it jumps straight into the except block.
- The `except` block lets you handle the error. This code is only executed *if an exception occurred* in the try block.
- The `else` keyword is used to define a block of code to be executed if no errors were raised in the try block.

**Optional keyword**

- The `finally` block, will always be executed regardless of if an exception was raised in the try block or not

```python
try:
    x = input("Enter number: ")
    x = x + 1
    print(x)
except:
    print("Invalid input")
```

### Using eval() to handle errors

- `eval()` will interpret any string argument parsed into it and execute it as Python code.
- eval only works with an expression (no equals sign)