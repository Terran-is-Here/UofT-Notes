---
updated_at: 2026-11-23T17:57:13.709-05:00
edited_seconds: 620
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": 28
Lecture Date: 2026-11-23
Week:
---
Hub: [[ESC180 Hub]]
Previous: [[27 — Runtime Complexity and more Recursion]]
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
\frac{2^{(n/2)+1}-1}{1}  = 2\sqrt{ 2^{n} }
$$
Then: 
$$
2^{n}\leq O(?)\leq \sqrt{ 2^{n} }
$$
This gives us a rough range as to what the value of $O$ is for our `fib(n)` function. If you think about the idea that this actually has the time complexity of itself ($O(fib(n))$. Following some more algebra pertaining to the theory of the Fibonacci sequence, then $O(\phi^{n})$ is the computational time complexity of `fib(n)`, where $\frac{1+\sqrt{ 5 }}{2}\approx{1}.61\approx \phi$

## Converting While Loops to Recursive Functions 
Consider implementing the Factorial function in terms of a while loop: 
```python
def fact_while(n): 
	cur_prod, i = 1,1
	while i != n+1: 
		cur_prod *= i
		i += 1
	
	return cur_prod
```
Note that we can also set this as: 
```python
def fact(n): 
	if n == 0: 
		return 1
	return fact(n-1)*n
```

### Default and Named Parameters
To do this in a recursive function, we can define default / named arguments, where these are default values without being explicitly called, and or explicitly setting specific parameters. 
```python
def myfunction(a,b=2,c=5):
	pass

myfunction(2) #b=2 and c=5 automatically
myfunction(2,c=10) #b=2, c=10 respectively.
```

For instance: 
```python
def f(a=1, b=2, c=3): 
	return a + b + C

print(f()) #returns 1+2+3 = 6
print(f(b=5)) #returns 1 + 5 + 3 = 9
```

We can implement our factorial now as: 
```python
def fact_iter(n, cur_prod = 1, i=1)
	if i == n+1: 
		return cur_prod 
	
	return fact_iter(n, cur_prod*i, i + 1)
```
Note that what this essentially is, is a recursive-type implementation of our while loop from earlier. We simply pass `cur_prod` though the calls, progressively multiplying it by larger and larger values of `i` until we hit our value. 

Tracing out the call tree, then: 
* `fact_iter(n, 1, 1)`
* `fact_iter(n, 1*1, 1+1)`
* `fact_iter(n, 1*1*2, 2+1)`
* `fact_iter(n, 1*1*2*3, 3)`
* `fact_iter(n, n!, n+1)`
Then in this context, the runtime complexity of this is also $O(n)$, though this realistically is just an iteration implementation of factorial. 

## Even More Recursion
Recall that we defined the `power_rec_fast` in terms of powers of $2$ instead to optimize our power function from previous lecture: 
```python
def power_rec_fast(x,n): 
	if n ==0: 
		return 1
	if n ==1: 
		return x
	half_power = power_rec_fact(x,n//2) 
	return half_power * half_power
```
Where this takes $O(\log(n))$ time, due to us dividing by a term of two each time. Note that we can easily change this function, but significantly changing it's runtime. 

Consider where we do this twice, without that intermediary step: 
```python
def power_rec_fast(x,n): 
	if n ==0: 
		return 1
	if n ==1: 
		return x
	return power_rec_fact(x,n//2)  * power_rec_fact(x,n//2) 
```

Where this calls itself twice per call. In this case, the tree in terms of a vertical manner is simply us dividing by two, where we eventually make $2^{k-1}=n$ calls at the end for our value of $n$, thus this gives us $O(n)$ time complexity in the end. 

We can actually implement this even slower: 
```python
def power2_slow(n): 
	if n == 1: 
		return 2
	return power2_slow(n-1)+power2_slow(n-1)
```
This makes us take the geometric sequence, where this actually takes $O(2^{n})$ time complexity.