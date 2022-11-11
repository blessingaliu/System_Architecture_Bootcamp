## 9th and 10th Session: Understanding Inheritance, Abstraction, Encapsulation and Polymorphism in OOP

## Inheritance

Inheritance is the capability of one class to derive or inherit the properties from another class. 

- it is a way of creating a new class using the information/details of an existing class without modifying it
- The new class created is known as a **child classes** or **subclasses,** child classes inherit methods and variables from **parent classes** or **base classes**.

- **A class can derive its methods and properties from another class**

```python
# Syntax 

class BaseClass:
	Body of base class
class DerivedClass(BaseClass):
	Body of derived class 
```

- In this example, we create two classes i.e. Bird (parent class) and Penguin (child class).
- The child class inherits the functions of parent class. We can see this from the swim() method.

```python
# parent class 
class Bird:

	def __init__(self):
		print("Bird is ready")

	def whoisThis(self):
		print("Bird")

	def swim(self):
		print("Swim faster")

# child class 
class Penguin(Bird):

	def __init__(self):
		print("Penguin is ready")

	def whoisThis(self):
		print("Penguin")

	def run(self):
		print("Run faster")

peggy = Penguin()
peggy.whoisThis()
peggy.swim()
peggy.run()

# Outputs
Penguin is ready
Penguin
Swim faster
Run faster
```

- Again, the child class modified the behavior of the parent class.
- We can see this from the whoisThis() method.
- Furthermore, we extend the functions of the parent class, by creating a new run() method.
    - Additionally, we use the super() function inside the __init__() method. This allows us to run the __init__() method of the parent class inside the child class.

****



## Abstraction

- Used to simplify reality and focus only on the data and processes relevant to the application being built.
- It is a **process of handling complexity by hiding unnecessary information from the user.**
- In Python, we can achieve abstraction by incorporating abstract classes and methods.
- We will get into this in a later post.

-----

