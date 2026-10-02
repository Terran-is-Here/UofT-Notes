---
updated_at: 2026-10-02T12:22:24.732-04:00
edited_seconds: 330
course:
tags:
"Lecture #": 0
Lecture Date: 2026-09-28
Week:
---
Hub:  N/A 
Previous: [[8 — ESC180 Lecture 8]]
Next: [[10 — ESC180 Lecture 10]]

--- 
# Lecture Notes
## Factorials 
Recall the definition of a factorial: 
$$
\begin{align}
n! = n *(n-1)!
\end{align}
$$
We haven't fully learned the concept of a Recursive function *just* yet, so we can implement this as the following loop: 
```python
def fact(n): 
	output = 1 
	for number in range(2,n+1): 
		output = output * number 
	return output
```

## Trailing Zeros 
We can define the concept of a trailing zero by seeing what is the equivalent base of our number in scientific notation? 

```python
def trailing_zeros(n): 
	trailingZeros = 0 
	while (n % 10 == 0): 
		n = n // 10 ## since Factorials map to N, we can keep it as an integer. 
		trailingZeros += 1 
	return trailingZeros
```

In lecture, we defined this with respects to having an input of a factorial, that is: 

```python
def trailing_zeros(n):
	n = fact(n) #From our previous statemnet.  
	trailingZeros = 0 
	while (n % 10 == 0): 
		n = n // 10 ## since Factorials map to N, we can keep it as an integer. 
		trailingZeros += 1 
	return trailingZeros
```


## List Question
Write a function to return the sum of the numbers in the list, except ignore sections of numbers starting with a 6 and extending to the next 7 (every 6 will be followed at least one 7). Return 0 for no numbers. 

This can be trivially defined as the following: 
```python
def add67(listOfNumbers): 
	sum = 0
	sumFlag = True: 
	for element in listofNumbers: 
		if element == 6: 
			sumFlag = False
			continue
		elif element == 7: 
			sumFlag = True 
			continue 
		if sumFlag: 
			sum += element 
	return sum 
```