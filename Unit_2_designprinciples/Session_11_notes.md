## 11th Session: Test Driven Development (TDD), Behaviour Driven Development (BDD) and Testing

# **Test-Driven Development (TDD)**

**Test-driven development (TDD)** is a style of programming where coding, testing, and design are tightly interwoven.

- **focuses on creating unit test cases before developing the actual code**
- **It is an iterative approach that combines programming, the creation of unit tests, and refactoring.**

**Red-Green-Refactor-Commit**

1. **RED** - The first step is to write a failing test for some new feature or behavior. To ensure the test is, in fact, failing, you must run it, in which case the test runner should display a failure
2. **GREEN** - The goal is to get to a passing test as quickly and simply as possible.
3. **REFACTOR** - Clean up your code
4. **COMMIT** - When you are done with this, commit your changes to a version control system like GitHub

----

## Refactoring

Refactoring consists of improving the internal structure of an existing program’s source code, while preserving its external behavior.

- ***Refactoring*** is the process of restructuring code, while not changing its original functionality.
- It turns messy and/or repetitive code into clean code.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/404de004-2321-4fee-a399-008efc7acc96/Untitled.png)

----

# Behaviour**-Driven Development (BDD)**

- Software development process that closes the gap between business people and technical people by
    - Encouraging collaboration across the roles to build shared understanding of the probelm to be solved
    - Working in rapid, small iterations to increasee feedback and the flow of value
    - Producing system documentation that is automatically checked against the system’s behaviour
    

## BDD

- Works by focusing collaborative work around concrete, real-world examples that illustrate how we want a system to behave
- We use those examples to guide us from concepts throught to implementation, in a process of continuous collaboration

1. **Discovery**  - The team creates User stories 
2. **Formulation** - Document these user stories in a way that can be automated and check for agreement 
3. **Automation** - Implement each user story, starting with an automated test to guide the development of the code. 

![Screenshot 2022-04-26 at 19.57.57.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/804f904f-d6b5-47dd-9b9d-7f47a78ea84b/Screenshot_2022-04-26_at_19.57.57.png)

----

## TDD vs BDD

**TDD is Test Driven Development**. This means writing a test that fails because the specified functionality doesn't exist, then writing the simplest code that can make the test pass, then refactoring to remove duplication, etc. You repeat this Red-Green-Refactor loop over and over until you have a complete feature.

**BDD is Behavior Driven Development**. This means creating an executable specification that fails because the feature doesn't exist, then writing the simplest code that can make the spec pass. You repeat this software is complete.

- **BDD is designed to test an application's behavior from the end user's standpoint, whereas TDD is focused on testing smaller pieces of functionality in isolation**.

- In TDD, unit tests are technical by nature, which limits readers and writers to developers or testers. However in BDD, Behavioral Tests are usually dictated by people who understand the customer more, such as product owner or manager. Due to their nature being relatively similar to plain English, Behavioral Tests can be read and evaluated by just about anybody — stakeholders, business owners, product managers, developers and testers.

- TDD may also be faster than BDD in that BDD requires more setup and communication across teams prior to writing the tests.

----


# Types of Software testing

## Unit-testing

- Software testing where indiviudal units or components of a software are tested
- The purpose is to validate that each unit of the software performs as designed.

## Integration-testing

- Software testing in which the different units, modules or components are tested as a combined entity (group)
- individual units are combined and tested to verify if they are working as they were intended

## System-testing

- Testing of the complete and fully integrated software product

## Acceptance-testing

- This is testing done by users, customers to determine whether or not the software has met the requirement specification

----


# Writing unit tests in Python using pytest

Installing pytest using pip (python package manager)

```python
python -m pip install pytest
```

## Writing a test for a calculator method

- **In the calculator.test.py**

```python
# import name of file
import calculator

# test_nameOfFunction 
def test_add():
    assert calculator.add(3,5) == 8
    assert calculator.add(1, 0) == 1

def test_subtract():
    assert calculator.subtract(10,5) == 5
    assert calculator.subtract(1, 0) == 1

# Can also use these:
# assertEqual
# assertNotEqual
# assertTrue
# assertFalse
# assertIs
# assertIsNot
```

- **In the calculator.test.py**

```python
def add(a,b):
    return a + b

def subtract(a,b):
    return a - b
```

- **To run the unit tests**

```python
pytest
```