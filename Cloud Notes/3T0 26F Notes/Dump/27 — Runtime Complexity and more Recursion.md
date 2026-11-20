---
updated_at: 2026-11-20T12:53:36.827-05:00
edited_seconds: 530
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
		return L[0] #if list is odd / asymmetric
		
	mid = len(L) // 2  
	return sum_list_2(L[:mid]) + sum_list_2(L[mid:]) #first half + second half sum
```

Note that when you draw out the call tree, you find that we get a binary call tree. This takes $O(1)$ time (roughly[^1]). Counting the number of calls, we find that for each layer of the binary tree, we have some $2^{k-1}$, where $k$ represents the depth. Taking the sum of this, we find that: 
$$
\sum_{i=0}^{k-1}2^{i} = \frac{2^{k}-1}{2-1} = 2^{k}-1
$$
Note that, at the bottom layer, that: 
$$
\begin{align}
2^{k-1} & = n \\
\log_{2}(2^{k-1})  & =\log_{2}n \\
k-1 & = \log_{2}n  \\
k & =\log_{2}n+1
\end{align}
$$
Thus, plugging this in, we find that: 
$$
\begin{align}
2^{k}-1 \\
2^{\log_{2}n + 1} + 1 \to O(n)
\end{align}
$$
We note that this divide and conquer strategy therefore actually has $O(n)$ time complexity. 

Note that earlier, we said that slicing is an $O(n)$ time complexity operation. We can instead rewrite the function in terms of the start and end endpoints: 
```python
def sum_list_fast(L,start,end): 
	if start == end: 
		return 0
	if end == start+1: 
		return L[start]
	
	mid = (end+start)//2
	
	return sum_list_fast(L,start,mid) + sum_list_fast(L,mid,end)
```

### Computing Powers Recursively
Can we write a function that takes in two parameters, and calculates the exponent? We can express this as: 
```python
def power_rec(base,exp): 
	if exp == 0: 
		return 1
	
	if exp > 0: 
		return base*power_rec(base,exp-1) #returns b * b^exp-1
	if exp <0: 
		return 1/power_rec(base,-exp)
```
Which is a trivial case, where the computational time complexity of this operation runs for at most, what `exp` has, or letting `exp` = $n$, then this has a time complexity of $O(n)$. 

Can we write a better runtime complexity instead if $n=2^{k+1}$? What if we are just squaring repeatedly? 

```python
def power_square(base,exp): #assuming exp = 2^(k+1)
	if exp == 0: 
		return 1
	 
	 if exp == 1: 
		 return base
	 
	 half_power = power_square(base,exp//2) # Multiply by half the corresponding power, recursive call, then square back to combine
	 return half_power * half_power
```
Note that this operation individually takes $O(1)$ time (ideally, with floats). Consider however that the call tree now scales by $\frac{1}{2^{k}}$, where we halve it each time. Note that the number of calls within this call tree now approaches some $O(\log(n))$

[^1]: Slicing is an $O(n)$ time complexity operation normally.
