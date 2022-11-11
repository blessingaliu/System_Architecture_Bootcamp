## Introduction to Object-oriented programming

- Everything is an Object
- Object-oriented programming is a programming paradigm
that provides a means of structuring programs so that properties and behaviors are bundled into individual **objects**
- For instance, an object could represent a Person with **properties (attributes)** like a name, age, and address and **behaviors (methods)** such as walking, talking, breathing, and running.

### Classes

- A **class** is a blueprint used to create individual objects
- An **object** is a collection of data (variables) and methods (functions) that act on those data. It is an an encapsulation of variables and functions into a single entity.
- Classes define functions called **methods**, which identify the **behaviors and actions** that an object created from the class can perform with its data. E.g A car class specifies that a model and a year are necessary for defining a car but it doesn’t contain the model or year of any specific car
- While the class is the blueprint, an **instance** is an object that is built from a class and contains real data. An instance of a dog class would be an actual car with a model of Nissan Micra and a year of 2021

```python
# Creating a new Car class with an .__init__() method 
# that creates .model and .year attributes:
class Car:
    def __init__(self, model, year):
        self.model = model
        self.year = year

# Instantiating an Object
class Car:
	pass 
# This creates a new Car class with no attributes or methods.

# To pass arguments to the model and year parameters
nissan = Car("Micra", 2020)
ford = Car("Fiesta", 2009)
# This creates two new Car instances (Objects)

# After you create the Car instances, 
# you can access their instance attributes using dot notation:
nissan.model
# Output 'Micra'

nissan.year
# Output '2020'
```

---------------------------------


### Components of a Class

<aside>
💡 Every Class contains **Attributes** and **Methods**<br>
<br>
--  **Attributes (or state)** are the characteristics of the class that help to distinguish it from other classes. eg person’s name, height<br>
<br>
-- **Behaviors (or methods)** are the tasks that an object performs eg walk, sit, eat

</aside>


---------------------------------



### Another example of Class Construction

```python
# Create the instance attributes fullname and email in the Employee class. Given a person's first and last names:

# Form the fullname by simply joining the first and last name together, separated by a space.
# Form the email by joining the first and last name together with a . in between, and follow it with @company.com at the end. Make sure the entire email is in lowercase.
# Examples
# emp_1 = Employee("John", "Smith")
# emp_2 = Employee("Mary",  "Sue")
# emp_3 = Employee("Antony", "Walker")

# emp_1.fullname ➞ "John Smith"
# emp_2.email ➞ "mary.sue@company.com"
# emp_3.firstname ➞ "Antony"

# Notes
# The attributes firstname and lastname are already made for you.

# Creating a class called Employee
class Employee:
    # Initialising the class with attributes of firstname and lastname 
    def __init__(self, first_name, last_name):
        self.first_name = first_name
        self.last_name = last_name

    # Creating a method that uses the class Employee and returns the first name + last name 
    def full_names(self):
        return self.first_name + " " + self.last_name

    # Creating a method that uses the class Employee and returns the first name + last name + String 
    def email(self):
        return self.first_name.lower() + "." + self.last_name.lower() + "@company.com"

# Creating an instance of the class Employee with arguments firstname and lastname 
employee_1 = Employee("John", "Smith")

print(employee_1.full_names())
print(employee_1.email())

# John Smith
# john.smith@company.com
```