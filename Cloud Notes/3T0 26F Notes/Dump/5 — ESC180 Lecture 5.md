---
updated_at: 2026-09-21T17:11:56.933-04:00
edited_seconds: 230
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
Next: [[6 —ESC180 Lecture 6]]

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

### Finding Primes
Recall that `a%b = some remainder`, and recall that a prime is defined by having no divisors divide it cleanly except itself. Using for loops, we can naiively implement this through the following: 
```python
#check if value n is prime and return True if it is. 
def IfPrime(n):
	for i in range(n): 
		if n % i == 0: #run through all divisors, if n!=i and n/i = some integer, then n is some multiple of i, ergo not prime. 
			return False
	return True

```

We can improve this algorithm. 
```python
def ImprovedIfPrime(n): 
	for i in range(2,n): 
		if n % i == 0: 
			return False
	return True
```

Recall, generally `range(a,b,c)` is `[a,b) with steps of c between`. We can also eliminate all of our even numbers: 
```python
def ImprovedIfPrime(n):

	if n == 0 or n==1: 
		return False #by definition
		
	#check even numbers
	if (n%2) == 0: 
		return False
	
	# Change bounds since we already compare [0,2]
	for i in range(3,n,2): 
		if (n % i) == 0: 
			return False
			
	return True
```