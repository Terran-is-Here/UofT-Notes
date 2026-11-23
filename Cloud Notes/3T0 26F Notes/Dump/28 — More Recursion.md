---
updated_at: 2026-11-23T17:31:56.570-05:00
edited_seconds: 350
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": 28
Lecture Date: 2026-11-23
Week:
---
Hub: 
Previous: 
Next:

--- 
# Lecture Notes

## Deep Copy Function
Recall that if we want to make a copy, we want to prevent any aliasing of elements. 

Recall the issues with some shallow copy function, that is: 
```python
L1 = [[1,2],[3,4]]
L2 = L1[:] #makes a shallow coppy
L2[0][1] = "CHANGED" 
print(L1) #returns [[1,"CHANGED"],[3,4]] as expected
```

Recall that the Copy Library lets us do the following: 
```python
copy = []
for e in L1: #this makes a "deep copy". 
	copy.append(e[:])
	
L1[0][1] = "CHANGED"
print(copy) #unaliased
```
The thing is though, this only works for a depth of 1. If we want to nest this, we can consider making a recursive function, where the interior function is an iterable function: 

```python
# Let L be a nested list of integers; for now. 
def deepcopy(obj): 
	if type(obj) is not list: #If our object is not a list: 
		return obj
	
	# if our object IS a list: 
	out = []
	for elem in obj: 
		out.append(deepcopy(elem)) #append to empty list what the deep copy is 
	
	return out #once all elements in obj are copied, then we simply return. 
```
For instance: 
```python
L1 = [[1,2],[3,[4,5]]]
L2 = deepcopy(L1)
L1[1][1][0] = "CHANGED"
print(L2) #returns: [[1, 2], [3, [4, 5]]]
print(L1) #returns: [[1, 2], [3, ['CHANGED', 5]]]
```

Note that this could break if you have a circular reference: 
```python
L1 = [1,2]
L1.append(L1) #L1 now has infinite "depth" 
```

> Technically we can account for this if we keep track of the corresponding ID values of the objects present, and that if the same ID exists, we simply return / append it as per usual. 

## Fibonacci Function
Recall how we programmed the Fibonacci Function from earlier: 

```python
def fib(n): 
	if n <=2: 
		return 1
	return fib(n-2) + fib(n-1)
```
If we wanted to find the runtime complexity of this, we note that each tree branches out in a different manner. In other words, the tree is not inherently symmetrical. We note that function itself is $O(1)$ time, which means we just need to figure out the depth / call count of the tree for some value $n$. 

For the case of this, we will take the lower and upper bound of the number of calls, based on the shortest and longest branches respectively. Recall that the sum of the geometric series is defined as :
$$
\sum_{i=0}^{N} r^{i} = \frac{r^{n+1}-1}{r-1}
$$
Then, we note that the longest branch is the branch that scales by some $n-1$, then: 
$$
2^{0} + 2^{1} + 2^{2}  +\dots + 2^{n-1}
$$
Then we find that $r = 2$, and $n=n-1$, thus: 
$$
\frac{2^{n}-1}{1} = 2^{n}
$$
Taking the limit, then we find that $O(2^{n})$, that is an exponential time complexity. 

If we take the shortest branch, something that scales by some $n-2$, then: 
$$
2^{0} + 2^{1} + 2^{2} + \dots + 2^{n/2}
$$
As we take essentially half the effective steps, then: 
$$
\frac{2^{(n/2)+1}-1}{1}  = 2\sqrt{  }
$$