---
updated_at: 2026-10-09T12:56:08.340-04:00
edited_seconds: 560
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

> *and* ordered, though that varies between versions (mainly older, older ones). 

However, for iteration in *this* method, you need to ensure that the *size* of the Iterable remains constant; instead use dict.items() and iterate through that pointer. 
```python
for key, element in my_dict.items(): 
	if element < 95: 
		del my_dict[key] 
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
Or, they can be accessed as a list of *tuples* of key,value pairs: 
```python
# Points to a STATIC copy of the dictionary's values. 
#Returns an iterable object dict_values in terms of [(key,values)...] pairs. Cannot be cast to a list. 
L3 = my_dict.items() 


for key, element in L3: #unpacks corresponding tuple
	print(key)
	print(element) 
```
Note that since any valid element can be anything; meaning that that object's corresponding methods are extended to what's being called.

## Object Manipulation
To remove objects from an object: 
```python
del my_dict[key] #removes key and it's corresponding values in my_dict
my_dict.clear() #removes all key:value pairs, in other words my_dict = {}. 
```

## Reversing the Order 
To invert the order of key:value pairs, we need to actually define a helper function: 

```python

some_dict = {"a":1, "b":2, "c":1}
def inv_dict(dict): 
	output_dict = {}
	for key, value in dict.items(): 
		if value not in output_dict: #checks if key is already present within the list
			output_dict[value] = [key]
		else: # if not, append to a list
			output_dict[value].append(key) 
	return output_dict

print(inv_dict(some_dict)) #returns {1: ["a","b"], 2:["b"]}. 
```
