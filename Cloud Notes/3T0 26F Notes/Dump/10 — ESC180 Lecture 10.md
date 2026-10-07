---
updated_at: 2026-10-07T17:06:52.286-04:00
edited_seconds: 380
course: ESC180H1
tags:
  - ESC180H1
"Lecture #": 0
Lecture Date: 2026-10-02
Week:
---
Hub: [[ESC180 Hub]]
Previous: [[09 — ESC180 Lecture 9]]
Next: [[11 — ESC180 Lecture 11]]

--- 
# Lecture Notes

## List Slicing
Has the general syntax of: 
```python
L[start:end:step]
```

Where given some list `L[]`, this returns a sub list formed from the members of `L` from index `start` up to but not including index `end`, with `step` indices between. 

Has alternative, we can omit our end step if needed: 
```python
L[start::step]
```
Where this starts from the start index, all to the end of the step. Note that if `step` is negative, it iterates *backwards* throughout the list—that is towards the start.

We can even omit the start index: 
```python
L[::step]
```
Where this starts from the *beginning* or *end* of the list. Note that if `step` is positive, it starts from the start moves forwards towards the end. If `step` is negative, it starts from the end and iterates towards the start. 

> Doing `L[::-1]` is often used to reverse a list. 

If no arguments are provided, as the following: 
```python
L[:]
```
It simply returns the list `L[]` as is, in the same order they were present in. Note that this is useful in the case when we want to make an instance of a list without modifying the original: 

```python
L = list(range(10))

M = L # Directly points M to L's memory 
M = L[:] # Points to a separate memory segment, with the same data as L, however separate from L. 
```

### Manual Implementation
This can be manually implemented as the following: 


```python

## With a For Loop
def ManualSlice(L,start,end,step): 
	res = [] 
	for index in range(start,end,step): # Steps from index = start, start + step, start +step + step .. end
		res.append(L[index])
	return res 
	
## With a While Loop
def ManualSliceWhile(L,start,end,step): 
	res = []
	ind = start 
	
	if step > 0: 
		while ind<end: 
			res.append(L[ind])
			ind += step 
	
	elif step < 0: 
		while ind>start :
			res.append(L[ind])
			ind+= step 
```

## Extending a List 
The following extends a list: 
```python
#list.extend(param) appends a list onto the end of another list: 
L = [0,1,2]
M = [3,4,5]
L.extend(M) # Inherently modifies the list L, such as our list.append(param) functions. 
print(L) # Expected: [0,1,2,3,4,5]
```

Note that `list.append(param)` directly appends whatever `param` is to the end of the list. Note also that `list.append(param)` solely accepts one operator, so star operators will not function. 

## Sorting Lists 
Python has a built in function for sorting lists as is: 
```python
L = [3,1,100,-5,29,50,0.1,-10]
L.sort() # Also directly changes L's structure, like list.extend and list.append
print(L) # Expected: [-10, -5, 0.1, 1, 3, 29, 50, 100]
```
Note that `list.sort()` also works with lists **solely composed of strings** (via lexicographic comparisons). It also primarily in ascending order. 