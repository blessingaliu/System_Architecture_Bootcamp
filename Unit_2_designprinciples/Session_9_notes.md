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


## Encapsulation

- This is exactly what is sounds like: encapsulating your stuff so that no one else can see it or touch it without your explicit approval.
- eg You can drive a car, but don't need to know how the engine works.
- Meaning data and the programs that manipulate those data are bound together and their complexity is hidden

Encapsulation: You need me to run to the grocery store for you every week. All you do is hand me your credit card, your grocery list, and your car keys and I go. Then after some time, I come back with everything you ask for. You don't know how I get there, what I do on the way, etc. You just know that when you give me the list, money, and keys, I turn it into groceries somehow.

Encapsulation is just the idea that no one outside of the programmer needs to know how parts of objects work. There is a certain part they can see and use, but that's it. So if the implementation changes because the original programmer modified something, the user of their code doesn't have their code suddenly not work

- Here, we define a Computer class.
- We used __init__() method to store the maximum selling price of Computer.
- Here, we have tried to modify the value of __maxprice outside of the class.
- However, since __maxprice is a private variable, this modification is not seen on the output.
- **To change the value, we have to use a setter function i.e setMaxPrice() which takes price as a parameter.**

```python
class Computer:

	def __init__(self):
		self.__maxprice = 900

	def sell(self):
		print("Selling Price: {}".format(self.__maxprice))

	def setMaxPrice(self, price):
		self.__maxprice = price

c = Computer()
c.sell

# Change the price
c.__maxprice = 1000
c.sell()

# Using the setter function
c.setMaxPrice(1000)
c.sell()

# Output 

Selling Price: 900
Selling Price: 1000
```

-----


## Polymorphism

- ***Polymorphism*** is an ***object-oriented*** programming concept that refers to the ability of a variable, function, or object to take on multiple forms.
- **Polymorphism is the ability of an object to take on many forms.**
- **Different subclasses of the same superclass, can implement their shared interface in different ways**
- eg Brother and sister are two different people but have the same parents.
- eg You can eat both an icecream and sushi, both are food but the way you would eat them would be slightly different
- The two objects can perform the same action even though the objects are not necessarily the same type

So polymorphism is a way to write code concerning a parent class, and any class that inherits from that parent class is valid input for that piece of code.

- We define two classes Parrot and Penguin.
- Each of them have a common fly() method. However, their functions are different.
- To use polymorphism, we created a common interface i.e flying_test() function that takes any object and calls the object's fly() method.
- Thus, when we passed the blu and peggy objects in the flying_test() function, it ran effectively.

```python
class Parrot:

	def fly(self):
		print("Parrot can fly")

	def swim(self):
		print("Parrot can't swim")

class Penguin:

	def fly(self):
		print("Penguin can't fly")

	def swim(self):
		print("Penguin can swim")

# common interface
def flying_test(bird):
	bird.fly()

# instantiate objects
blu = Parrot()
peggy = Penguin()

# passing the object 
flying_test(blu)
flying_test(peggy)

# Output 
Parrot can fly
Penguin can't fly
```