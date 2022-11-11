### 7th Session: Unit 2: Design Principles (Object Oriented Programming)

## Design Principles

- Guidelines that aid the software design process
- Help to handle complexity and enhance maintenance

---

## Examples of Design Principles for OOP - SOLID DRY KISS

### SOLID

- **Single Responsibility Principle:** Each class should only do one thing, have a single purpose/functionality.
- **Open Close Design Principle:** Software entities like classes, modules and functions should be open for extension (new functionality and closed for modification.
- **Liscov Substitution Principle:** Objects of a superclass shall be replaceable with objects of its subclasses without breaking the application.
- **Interface Segregation Principle:** A client should not be exposed to methods it doesn't need.
- **Dependency Inversion Principle:** Objects which a class needs should be “injected” into it, instead of constructing it internally. The injection means that the class is getting its dependencies from an external source where a class receives any objects it needs as constructor parameters.

(I may do another post on the SOLID principles in more details, let me know if this would be useful 🤗)

---


### DRY (Don’t repeat yourself)

- Avoid duplication in code

---

### KISS (Keep it Simple, Stupid)

- Keep your code simple, concise and understandable.

---


## Object Oriented Programming

- Object-oriented programming (OOP) is a way of structuring a program by bundling data with related properties and behaviors (encapsulated) into objects.

### Objects

- An object has two characteristics:
    - **attributes (properties)**
    - **behavior (methods)**
- A parrot is an object, as it has the following properties:
    - name, age, color as attributes
    - singing, dancing as behavior

### Class

- A class is a blueprint for the object, it has instructions for creating the object’s attributes (what the object looks like) and the object’s behaviour (what the object can do)
- From class, we construct instances. An instance is a specific object created from a particular class
- An object is an **instance** of a class.

```python
# Defining an empty Car class 
class Car:
	pass 

# To create a object from a class 
car_1 = Car()
```

---


## **Properties (attributes)** and **behaviors (methods)**

### Attributes

- **A class attribute** is a variable defined directly in the class that are shared by all the objects of the class. **It is defined outside the constructor function,** `__init__(self,...)`, of the class.
- **An instance attribute** is a attribute or property belonging to one, and only one, object. It is atatched to an instance of a class. 
This variable is only accessible in the scope of this object and it is **defined inside the constructor function,** `__init__(self,..)` of the class.

```python
class Parrot:

    # class attribute 
    species = "bird"

    # instance attribute
    def __init__(self, name, age):
        self.name = name
        self.age = age 

# Instiantiate the Parrot class
blu = Parrot("Blu", 10)
woo = Parrot("Woo", 15)

# Accessing the class attributes
print("Blu is a {}".format(blu.__class__.species))
print("Loo is a {}".format(blu.__class__.species))

# Accessing the instance attributes
print("{} is {} years old".format(blu.name, blu.age))
print("{} is {} years old".format(woo.name, woo.age))
```

---


### **Differences Between Class and Instance Attributes**

The difference is that class attributes are shared by all instances. When you change the value of a class attribute, it will affect all instances that share the same exact value. The attribute of an instance is unique to that instance.


---

## Methods

- **Methods are functions defined inside the body of a class.**
- **Methods are used to define the behaviour of an object.**

- Instance methods are methods called on an instance object (eg drift, accelerate)
- Using the `self` parameter, we can access the other attributes and methods on the same object and can change the object state. Also, using the `self.__class__` attribute, we can access the class attributes, and can change the class state as well. **Therefore, instance methods gives us control of changing the object as well as the class state.**

```python
# Create a python class Vehicle of type sportscar for all cars you create
# that has model, speed, colour, rim_colour
# can drift, can accelerate

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