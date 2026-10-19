---
updated_at: 2026-10-19T17:35:48.294-04:00
edited_seconds: 240
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": 17
Lecture Date: 2026-10-19
Week:
---
Hub: 
Previous: 
Next:

--- 
# Lecture Notes
## Python Memory Model
The Python Memory Model is the general model for the structure of variables present within a program. Most cases; these are defined as a form of a Memory table with addresses, values, and the corresponding variables present (which point to an address, which point to a data value).

Memory tables are formed as a table linking the addresses of values, and their corresponding values. In python, we can fetch the address of a piece of data with the `id()` function. For instance, the table below prints out the id addresses of a list of numbers: 
```python
nums - list(range(0,100))
for i in nums: 
	print(i, id(i))

```

Variables are defined as address pointers; which points to an address which points to piece of data: 

| Variable | Address  |
| -------- | -------- |
| a        | @1020    |
| b        | @195192  |
| c        | @1941962 |
Where when we define the variables to a new piece of data; the pointer simply updates to a different memory address. Note that ID addresses on their own, even immutable values like ints, vary(based on block allocations, etc.) 

Strings also have memory addresses; note that the following behavior occurs when we consider the `is` operator. 
```python
a = "ESC"
b = "180" 
c = "ESC180" 
d = a +b

c is d ## returns False, different address
c == d ## returns true, same data
```

For memory and variable tables, we can express lists as a data object in memory with memory pointers stored within: 
```python
a = 1 
b = 2
c = 3 
L = [a,b,c] # data structure wise, equivalent to some L[id(a),id(b),id(c)]; but note that id(L) is something different entirely 
```

When we declare $a,b$