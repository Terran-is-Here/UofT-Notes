---
updated_at: 2026-10-09T12:39:57.320-04:00
edited_seconds: 340
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": -15
Lecture Date: 2026-10-07
Week:
---
Hub: [[ESC180 Hub]]
Previous: [[10 — ESC180 Lecture 10]]
Next:

--- 
# Lecture Notes

## Tuples
Tuples are immutable data objects: 
```python
my_tuple = (1,2,3)...
my_tuple[0] = 10 ## raises an error (no assignment operator for tuples)
```

However, they are *iterable*; that is: 
```python
my_tuple = (1,2,3,4,5)
for element in my_tuple: 
	print(element) 
```

Functionally, Tuples are immutable lists. List slicing also works in this context (following all the same logic previously): 
```python
print(my_tuple[::-1]) #Prints (5,4,3,2,1) 
#etc etc
```
## Dictionaries 
Dictionaries are mutable key/value pairs, 
```python
my_dict = {"key": "value", 1:2, (1,2): "value"} #Key objects must be hashable 
```
Or in other words, Dictionaries are actually *hash maps* (that is, they support the `__hash__` method). As per traditional in Hash Maps, we can change the values of keys with respects to their data. Because of this, Dictionaries when retrieving are $O[1]$ time to access values. : 

```python
my_dict = {"somethingHashable": "somevalue", 2:2, "six":'seven'}
my_dict["somethingHashable"] # returns "somevalue" 
my_dict[2] #returns 2 
```

> Note that with the principle of Hash Maps (and the concept of Hashes), you *cannot* have two objects with the same hash be different; that is: 
```python
hash(a) == hash(b) #only true iff a = b
```
Or in other words, Hash Map Keys must inherently be some bijective function. 

Dictionaries are Iterable: 
```python
my_dict = {"key": "value", 1:2, (1,2): "value"}
for element in my_dict: 
	print(element) #returns "value", 2, "value" in that order. 
```

### Object Assignment 
We can add elements in a dictionary with the following syntax: 
```python
my_dict[key] = value #where key is some hashable object, and value is some data. 
```

Note that all the *keys* in a dictionary can also be cast into their own list, as well as their values: 
```python
L1 = list(my_dict.keys()) #Returns an iterable object dict_keys, which can be cast into a list. 
L2 = list(my_dict.values()) # Returns an iterable object dict_values, which can be cast into a list.
```