## 3rd Session: Fundamentals of coding with Python continued - Lists, Tuples and Sets


## Python Collections
- **List (ordered and changeable) - Allows duplicate members**
- **Tuple (ordered and unchangeable) - Allows duplicate members**
- **Set (unordered unchangeable and unindexed) - No duplicate members**
- **Dictionary (ordered and changeable) - No duplicate members**

--------------------------------------------------------------------------


## Lists [ ]

- Lists are used to store multiple items in a single variable.
- List items are **ordered, changeable, and allow duplicate values.**
- List items are indexed, the first item has index `[0]`, the second item has index `[1]` etc.

```python
# lists are indexed so they can have items with the same value
my_list = ["jollof_rice", "asaro", "jollof_rice", "chicken", "plantain"]
print(my_list)
# Ouputs ['jollof_rice', 'asaro', 'jollof_rice', 'chicken', 'plantain']

# len() to see how many items a list has
len(my_list)
# Outputs 4 

# type() to check the data type
type(my_list)
# Outputs list
```

### **Accessing list items**

- **list_name[0]**
- **list_name[start:end:stepsize]**

```python
# Accessing list items using index number
my_list = ["jollof_rice", "asaro", "jollof_rice", "chicken", "plantain"]
my_list[1] # Ouputs 'asaro'
my_list[-1] # Ouputs 'plantain'

# List slicing and dicing
# my_list = [start:end:stepsize]

countries = ["Nigeria", "Ghana", "UK", "US"]

countries[:4] # Start at 0 index and end at index 4 (not included)
# Outputs ['Nigeria', 'Ghana', 'UK', 'US']

countries[3:] # Start at 3 index and end there
# Outputs ['US']

countries[1:3] # Start at 1 and end at 3 (not included)
# Outputs ['Ghana', 'UK']

# Check if an item exists 
my_list = ["jollof_rice", "asaro", "jollof_rice", "chicken", "plantain"]
if "chicken" in my_list:
  print("Yes, chicken is in this list")**
# Outputs **Yes, chicken is in this list**
```

### Removing **list items**

- **remove(”item_name”)**
- **pop(indexnumber)**
- **del list_name[0]** (to remove specified index of list)
- **del list_name** (to remove entire list)

```python
# remove() method to remove the specified item
another_list = ["dresses", "skirts", "trousers", "shoes"]
another_list.remove("shoes")
print(another_list)
# Ouputs ['dresses', 'skirts', 'trousers']

# pop() method to remove the specified index
another_list.pop(1) # Removes the second item 
print(another_list)
# Outputs ['dresses', 'trousers']

another_list.pop() # Removes the last item  
print(another_list)
# Outputs ['dresses']

# del method also to remove the specified index
another_list = ["dresses", "skirts", "trousers", "shoes"]
del another_list[0] # Removes the first item 
print(another_list)
# Outputs ['skirts', 'trousers', 'shoes']

del another_list
print(another_list)
# NameError: name 'another_list' is not defined

# The clear() method empties the list.
# The list still remains, but it has no content.
another_list = ["dresses", "skirts", "trousers", "shoes"]
print(another_list)
# Outputs [ ]
```

### **Sorting list items**

- **list_item.sort()**
- **list_item.sort(reverse = True)**

```python
# sort() method to sort lists alphabetically
names = ["Johnny", "Becky", "Amanda", "Zion"]
names.sort()
print(names)
# Ouputs ['Amanda', 'Becky', 'Johnny', 'Zion']

# sort() method to sort lists numerically ascending
age = [12, 4, 5, 2, 5]
age.sort()
print(age)
# Ouputs [2, 4, 5, 5, 12]

# sort() method to sort lists numerically descending
age = [12, 4, 5, 2, 5]
age.sort(reverse = True)
print(age)
# Ouputs [12, 5, 5, 4, 2]
```

### Copying **list items**

- **list_item.copy()**
- **new_list = list(old_list)**

```python
# copy() method to make a copy of the list
age = [12, 4, 5, 2, 5]
new_ages = age.copy()
print(new_ages)
# Ouputs [12, 4, 5, 2, 5]

# using list() method to make a copy
age = [12, 4, 5, 2, 5]
another_age_list = list(age)
print(another_age_list)
# Ouputs [12, 4, 5, 2, 5]
```

### Joining **list items**

- **list3 = list1 + list2**
- **list1.extend(list2)**

```python
# using + to join two lists
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)
# Ouputs ['a', 'b', 'c', 1, 2, 3]

# using extend() method to add list2 at the end of list1
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)
# Ouputs ['a', 'b', 'c', 1, 2, 3]
```

--------------------------------------------------------------------------


## Tuple ( )

- Tuples are used to store multiple items in a single variable.
- A tuple is a collection which is **ordered** and **unchangeable (immutable)**
- Tuples are indexed so they can have items with the same value (Duplicates)

```python
# Creating a Tuple
new_tuple = ('kia', 'lexus', 3, True)
print(new_tuple)

OR 

this_tuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
print(this_tuple)

# You cannot change, add or remove items after the tuple has been created
new_tuple[0] = 26
# Throws an error, you cannot change items in a tuple
```

### **Accessing Tuple items**

- **tuple_name[0]**
- **tuple_name[2:5]** (2 is the start index ending at 5 - 5 index not included)
- **tuple_name[:4]** (starts from the first index and ends at the 4th index - not including the 4th index)
- **tuple_name[-4:-1]** returns the items from index -4 (included) to index -1 (excluded)

### Updating **Tuple items**

- Change to the tuple to a list before you can update it

```python
# Convert the tuple into a list to be able to change it
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)
type(thistuple)
# Outputs tuple

# Add a tuple to a tuple
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y
print(thistuple)
# Outputs ('apple', 'banana', 'cherry', 'orange')
```

### Unpacking a **Tuple**

```python
# When we create a tuple, we normally assign values to it. 
# This is called "packing" a tuple:

new_tuple = ('kia', 'lexus', 3, True)

# But, in Python, we are also allowed to extract the values back into variables. 
# This is called "unpacking":

new_tuple = ('kia', 'lexus', 3, True)
**car**, another_car, number, boolean = new_tuple
print(car)
print(another_car)
print(number)
print(boolean)
# Outputs 
kia
lexus
3
True
```

### Joining Tuples

- **tuple3 = tuple1 + tuple2**
- **new_tuple = initial_tuple * 3** (If you want to multiply the content of a tuple a given number of times, you can use the `*` operator)

### Tuples Methods

- **tuple.count(value)** (value is the item to search for)
- **tuple.index(value)**

```python
# using count() to return the count of the number you are searching for
my_tuple = (1, 0, 5, 8, 5, 3, 2, 4)
number = my_tuple.count(5)
print(number)
# Outputs 2

# The index() method finds the first occurrence of the specified value.
my_tuple = (1, 0, 5, 8, 5, 3, 2, 4)
number = my_tuple.index(8)
print(number)
# Outputs 3
```

--------------------------------------------------------------------------


## Set { }

- Tuples are used to store multiple items in a single variable.
- A tuple is a collection which is **unordered, unchangeable and unindexed**

```python
# In Sets, duplicate items are ignored
names = {"Blessing", "Blessing", "Joel", "Annie"}
print(names)
# Outputs {'Annie', 'Blessing', 'Joel'}

# len (length of set)
len(names)
# Outputs 3

# add (add a new element to set)
names.add('Sharon')
# Outputs {'Annie', 'Blessing', 'Joel', 'Sharon'}

# remove (remove a element to set)
names.remove('Annie')
# Outputs {'Blessing', 'Joel', 'Sharon'}

# union (adds two sets together)
countries = {"Nigeria", "Ghana", "UK", "US"}
names.union(countries)
# Outputs {'Blessing', 'Ghana', 'Joel', 'Nigeria', 'Sharon', 'UK', 'US'}

# intersection_update ()
names = {"Blessing", "Ghana", "Joel", "Nigeria"}
names_2 = {"Nigeria", "Ghana", "UK", "US"}
names.intersection_update(names_2)
names
# Outputs {'Ghana', 'Nigeria'}

# pop (removes the last element in the set)
names = {"Blessing", "Ghana", "Joel", "Nigeria"}
names.pop()
# Outputs 'Nigeria'

# del (to delete your set)
del names 
```

### **Accessing set items**

- You cannot access items in a set by referring to an index or a key.
- But you can loop through the set items using a `for` loop, or ask if a specified value is present in a set, by using the `in` keyword.
```python
# Accessing set items using for loop 
my_set = {"jollof_rice", "asaro", "jollof_rice", "chicken", "plantain"}
for chicken in my_set:
  print(chicken)
# Outputs 
jollof_rice
plantain
chicken
asaro
```