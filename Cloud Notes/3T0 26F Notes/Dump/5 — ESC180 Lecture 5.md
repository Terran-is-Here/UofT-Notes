---
updated_at: 2026-09-18T12:24:32.352-04:00
edited_seconds: 100
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": 5
Lecture Date: 2026-09-14
Week: 2
created:
Created: September 14th 2026, 5:11:35 pm
---
Hub: [[ESC180 Hub]]
Previous: N/A (was lazy)
Next:

--- 
# Lecture Notes
## Variable Naming Conventions 
Generally, make variable names comprehensible.
* Note that snake_case is normally used in python for variables; or SCREAMING_SNAKE_CASE for constants: 

### Loops
In general, loops are used for repeated computation, for loops execute a code block a number of times.
* This is similar to Java's, although with simpler syntax.

```python
for x in range(0,n): 
	#code block here
```

Note for something that can be iterated through, then: 
```python
list1 = ["a","b","c"]
for element in list1: 
	print(element)
	# expected output: 
	# a
	# b
	# c
```
