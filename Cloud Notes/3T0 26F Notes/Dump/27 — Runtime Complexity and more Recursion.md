---
updated_at: 2026-11-20T12:29:30.359-05:00
edited_seconds: 220
course:
tags:
  - ESC180H1
"Lecture #": 0
Lecture Date: 2026-11-20
Week:
---
Hub: [[ESC180 Hub]]
Previous: [[26 — ESC180 Lecture 26 — Recursive Functions]]
Next:

--- 
# Lecture Notes

## Analyzing Recursive Runtime Complexity
Recall that the factorial function that we defined recursively previously: 
```python
def fact(n): 
	if n == 0:
		return 1
	return n * fact(n-1)
```
Note that without a recursive call, this takes $O(1)$ time to perform. With a recursive call, we note that this steps for some: 
$$
n, n-1, n-2, \dots, 1, 0
$$
Or in other words, thus runs for $n+1$ times. If you consider the call tree, this is a linear call tree, where: 
```
fact(n) -> fact(n-1) -> fact(n-2) -> ... -> fact(1) -> fact(0)
```

Consider now a different implementation of a factorial function, now with $O(n)$ time complexity: 
```python
def mult(n,m): #solves n*m 
	out = 0
	for i in range(n):
		out+=m
	return out

def fact_slow(n): 
	if n == 0:
		return 1
		
	return mult(n, fact_slow(n-1))
```

Note that due to the introduction of `mult(n,m)`, A single call to `fact_slow(n)` now takes $O(n)$ time to compute. Note that the call tree is still linear, but each operation now takes $O(n)$ time to run. Thus we can observe that this would therefore have a runtime complexity of $O(n^{2})$. 

* Or, in other words, each operation takes $n*(n-i)$ operational time, where $i$ is the number of times we call this function. In other words, we have an arithmetic sequence when we sum this up, giving us $\frac{kn(n+1)}{2}$ implying $O(n^{2})$ time complexity. 
### Further Analysis
Consider now our recursive list sum operator: 
```python
def sum_list(L): 
	if len(L) == 0: 
		return 0
	
	return L[0] + sum_list(L[1:])

sum_list(5)
```
We can assume that `sum_list(L)` takes $O(1)$ time, and thus this gives us a linear call tree, giving us a time complexity of $O(n)$. 

Consider now if we rewrote this through a "divide and conquer" strategy, where the sum of a list is equivalent to the sum of the first half and the second half of the list. Implementation wise, we can get this as the following function: 

```python

def sum_list_2(L): 
	if len(L) == 0: 
		return 0
	
	if len(L) == 1: 
		return L[]
```

