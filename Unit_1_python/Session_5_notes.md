## 5th Session: Fundamentals of coding with Python continued - List, Dictionary comprehension and Debugging your code


## List Comprehension

- A shorter syntax for creating a new list based on the values of an existing list

```python
# Syntax 
newlist = [expression for item in iterable if condition == True]
```

- **Without list comprehension, you will have to write a `for`
 statement with a conditional test inside**:

```python
# Using for loop to perform operation on list items 
list = [3, 6 , 5, 6, 7, 9]
list_2 = []

for i in list:
  list_2.append(i * 2)
print(list_2)
# [6, 12, 10, 12, 14, 18]
```

- **Using list comprehension**

```python
list_3 = [i ** 2 for i in list]
print(list_3)
# [9, 36, 25, 36, 49, 81]
```


### Some Coding Challenges

- **Print all the odd numbers between 5 and 15**

```python
for i in range(5, 15, 2):
  print(i)
# 5 7 9 11 13
```

- **Create a list of square of even numbers from 5 to 15**

```python
even_numbers = []
for i in range(6, 15, 2):
  even_numbers.append(i  ** 2)
even_numbers

# [36, 64, 100, 144, 196]

# Alternative way of doing it - list comprehension
even = [i**2 for i in range(6, 15, 2)]
print(even)

# [36, 64, 100, 144, 196]

```

-----------------------------------------------------------------------------------------------------------


## Dictionary comprehension

```python
# Syntax
dict_variable = {key:value for (key,value) in dictonary.items()}
```

```python
# A dictionary
ages = {"age1": 10, "age2": 29, "age3": 50, "age4": 25}
ages.items()

# dict_items([('age1', 10), ('age2', 29), ('age3', 50), ('age4', 25)])

# Using a for loop to change items in a dictionary
for i,j in ages.items():
  ages[i] = j+10
print(ages)

# {'age1': 20, 'age2': 39, 'age3': 60, 'age4': 35}

# Using dictionary comprehension
# i is key 
# j is the value
# dict_variable = {key:value for (key,value) in dictonary.items()}
dict = {i:j+10 for i,j in ages.items()}
print(dict)

# {'age1': 30, 'age2': 49, 'age3': 70, 'age4': 45}
```

-----------------------------------------------------------------------------------------------------------


### Some More Coding Challenges - Practicing Algorithms

- **Create a function that takes two arguments: the original price and the discount percentage as integers and returns the final price after the discount**

Example 

dis(1500, 50) ➞ 750

dis(89, 20) ➞ 71.2

dis(100, 75) ➞ 25

```python
def discount_calculator(price, discount):
  discounted_price = price * (discount/100)
  final_price = price - discounted_price
  return final_price

discount_calculator(89, 20)
# 71.2 
```

- **Given the radius of a circle and the area of a square, return True if the circumference of the circle is greater than the square's perimeter and False if the square's perimeter is greater than the circumference of the circle.**
    - **Notes**
    - **You can use Pi to 2 decimal places (3.14).**
    - **Circumference of a circle equals 2 * Pi * radius.**
    - **To find the perimeter of a square using its area, find the square root of area (to get side length) and multiply that by 4.**

```python
# Examples
# circle_or_square(16, 625) ➞ True
# circle_or_square(5, 100) ➞ False
# circle_or_square(8, 144) ➞ True

from math import *

def math(radius, area):
  circumference = 2 * 3.14 * radius
  perimeter = sqrt(area) * 4
  if circumference > perimeter:
    return True
  else:
    return False

math(8, 144)

# True
```

- **Create a function that takes a string and returns the number (count) of vowels contained within it.**

```python
# Examples
# count_vowels("Celebration") ➞ 5
# count_vowels("Palm") ➞ 1
# count_vowels("Prediction") ➞ 4

# a, e, i, o, u are considered vowels.

def count_vowels(string):
  vowels = 0 
  for i in string:
    if i in ["a", "e", "i", "o", "u"]:
      vowels += 1
  return vowels

count_vowels("Prediction")

# 4
```

- **Create a function that takes three arguments a, b, c and returns the sum of the numbers that are evenly divided by c from the range a, b inclusive.**

```python
# evenly_divisible(1, 10, 20) ➞ 0
# No number between 1 and 10 can be evenly divided by 20.

# evenly_divisible(1, 10, 2) ➞ 30
# 2 + 4 + 6 + 8 + 10 = 30

# evenly_divisible(1, 10, 3) ➞ 18
# 3 + 6 + 9 = 18

def check_if_divisible(a, b, c):
 
    # Variable to store the sum
    sum = 0
 
    # Running a loop from A to B and check
    # if a number is divisible by i.
    for i in range(a, b + 1):
 
        # If the number is divisible,
        # then add it to sum
        if (i % c == 0):
            sum += i
 
    # Return the sum
    return sum
 
# Driver code
if __name__=="__main__":
     

    a = 1
    b = 10
    c = 2
 
    # Printing the result
    print(check_if_divisible(a, b, c))
	
# Outputs 30
```

- **Write a program that creates a personalised invite for your friends to your birthday party. Your program should include your friend’s name, a different pass code for each friend and the invite message.**

**NB:  You can use a dictionary to store your friends name and their pass code.**

```python
# Ask user to give name, passcode and invite message of who they want to invite
# Store information in a dictionary
party_invite = {}

for i in range(2):
  name = input("Enter your name: ")
  pass_code = input("Enter specific passcode: ")
  invite_message = input("Enter the invite message: ")
  party_invite[name] = pass_code, invite_message

print(party_invite)
```

-----------------------------------------------------------------------------------------------------------


## Debugging

Programming is a complex process. Since it is done by human beings, errors may often occur. Programming errors are called **bugs** and the process of tracking them down and correcting them is called **debugging**. Some claim that in 1945, a dead moth caused a problem on relay number 70, panel F, of one of the first computers at Harvard, and the term **bug** has remained in use since. For more about this historic event, see [first bug](http://en.wikipedia.org/wiki/File:H96566k.jpg).

Three main kinds of errors can occur in a program: **Syntax errors**, **Runtime errors**, and **Semantic errors**. It is useful to distinguish between them in order to track them down more quickly.

- **Parse Error/ Syntax error**

<aside>
💡 **Syntax** refers to the structure of a program and the rules about that structure. For example, in English, a sentence must begin with a capital letter and end with a period. 

If a program is not written in the format of the language used or the program has grammatical errors, it will throw a **syntax error**

</aside>


- **Runtime** **error**

<aside>
💡 The second type of error is a runtime error, so called because the error does not appear until you run the program. These errors are also called **exceptions** because they usually indicate that something exceptional (and bad) has happened.

Runtime errors are rare in the simple programs you will see in the first few chapters, so it might be awhile before you encounter one.

</aside>

- **Semantic error**

<aside>
💡 The third type of error is the **semantic error**. If there is a semantic error in your program, it will run successfully in the sense that the computer will not generate any error messages. However, your program will not do the right thing. It will do something else. Specifically, it will do what you told it to do.

The problem is that the program you wrote is not the program you wanted to write. The meaning of the program (its semantics) is wrong. Identifying semantic errors can be tricky because it requires you to work backward by looking at the output of the program and trying to figure out what it is doing.

</aside>

-----------------------------------------------------------------------------------------------------------


## Error Subtypes

- **TypeError**

<aside>
💡 **TypeErrors** occur when you you try to combine two objects that are not compatible. For example you try to add together an integer and a string. Usually type errors can be isolated to lines that are using mathematical operators, and usually the line number given by the error message is an accurate indication of the line.

</aside>

- **NameError**

<aside>
💡 Name errors almost always mean that you have used a variable before it has a value. Often NameErrors are simply caused by typos in your code. They can be hard to spot if you don’t have a good eye for catching spelling mistakes. Other times you may simply mis-remember the name of a variable or even a function you want to call.

</aside>

- **ValueError**

<aside>
💡 Value errors occur when you pass a parameter to a function and the function is expecting a certain limitations on the values, and the value passed is not compatible.

</aside>