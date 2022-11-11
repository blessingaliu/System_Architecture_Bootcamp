## 2nd session: Fundamentals of coding with Python continued (Syntax and lists)

## Python Syntax (Important bits)

- Indentation
- Variables (case-sensitivity) - **camelCase, snake_case and PascalCase**
- Python comments
- Casting
- Global and local scoping

-----------------------------------------------------------------------------------------------------------


### Comments

```python
# This is a single line comment 

'''
This is the first comment
This is the second
third 
'''
```

-----------------------------------------------------------------------------------------------------------


### Casting

- **Changing the data type of a variable** (from int to str)

```python
var_name = int(var_name)
type(var_name)

// output int
```

-----------------------------------------------------------------------------------------------------------


### Global Scope vs Local Scope

- ***Scope*** has to do with where you can access your variables

The explanation is that 

- **Local scope includes all variables declared inside a function. A local variable is only accessible where it’s declared.**
- **Global scope includes variables declared outside of the function. This variable can be accessed anywhere within the script.**

-----------------------------------------------------------------------------------------------------------


## Python Operators summarised

- **Arithmetic operators** (+, -, *, /, %, **, //)
- **Comparison operators** (==, =!, >, <, >=, <=)
- **Logical operators** (AND [both sides true], OR [one side true], NOT [no side true])
- **Membership operators** to check whether a value or variable exists in a sequence (string, list, tuples, sets, dictionary) or not(in, not in)


-----------------------------------------------------------------------------------------------------------

## Python Data Types continued

### Lists (and their methods)

- Lists are used to store multiple items in a single variable [ ].

```python
# This is an example of a list
names = ['David', 'Blessing', 'Sarah', 'Dayo']
print(names)
# Ouputs ['David', 'Blessing', 'Sarah', 'Dayo']


- copy()	Returns a copy of the list (creates a new list)
names.copy()
# Ouputs ['David', 'Blessing', 'Sarah', 'Dayo']


- count()	Returns the number of elements with the specified value
names.count('Blessing')
# Outputs 1


- index()	Returns the index of the first element with the specified value
names.index('David')
# Outputs 0


- extend()	Add the elements of a list (or any iterable), to the end of the current list
# You can use multiple values to extend the list
new_elements = ['Bayo', 'James', 'Solomon']
names.extend(new_elements)
print(names)
# Outputs ['David', 'Blessing', 'Sarah', 'Dayo', 'Bayo', 'James', 'Solomon']


- append()	Adds an element at the end of the list (modifies the original list)
# You can only insert one value at a time
names.append('Toye')
print(names)
# Outputs ['David', 'Blessing', 'Sarah', 'Dayo', 'Bayo', 'James', 'Solomon', 'Toye']


- insert()	Adds an element at the specified position
names.insert(4, 'Joe')
# Ouputs ['David',
 'Blessing',
 'Sarah',
 'Dayo',
 'Joe',
 'Bayo',
 'James',
 'Solomon',
 'Toye']


- pop()	Removes the element at the specified position
names.pop(2)
# Outputs 'Sarah'


- remove()	Removes the first item with the specified value
names.remove('Blessing')
# Outputs ['David', 'Dayo', 'Joe', 'Bayo', 'James', 'Solomon', 'Toye']


- clear()	Removes all the elements from the list
names.clear()
# Outputs []


- reverse()	Reverses the order of the list
names = ['David', 'Blessing', 'Sarah', 'Dayo']
names.reverse()
# Outputs ['Dayo', 'Sarah', 'Blessing', 'David']


- sort()	Sorts the list
names.sort()
# Outputs ['Blessing', 'David', 'Dayo', 'Sarah']
```