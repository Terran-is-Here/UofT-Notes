---
updated_at: 2026-11-11T17:26:57.977-05:00
edited_seconds: 300
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-11
Week:
---
Hub: 
Previous: 
Next:

> I for the life of me DO NOT CARE for taking notes in things, but it would be helpful.

--- 
# Lecture Notes

## Insertion Sot
Insertion sort works by simply going through the list, swapping it to the highest value; then sorting the smaller value of the list. Note that this has a worst asymptotic time complexity of $O(n^{2})$, where $n$ represents the length of the list (regardless of the *format* of the list, that is this is how well it operates regardless of what kind of list is passed into it.)

## Bubble Sort
We simply pass through the list and swap elements in a locality, and let us define the runtime complexity of the function. Or in other words, we check adjacent elements 

```python
def bubblesort(L)
	hasSwapped = True #assume initial pass is not swapped
	while hasSwapped: 
		hasSwapped = False # reset value to check if list has been fully sorted
		for i in range(len(L)-1): 
			if L[i] > L[i+1]: 
				L[i+1], L[i] = l[i], L[i+1] #swap elements 
				hasSwapped = True #a swap has occured 
				continue 
```

This is the base implementation, but note that we can optimize it further. Note that for the number of loops that we swap for, we note that each iteration sorts the list, making the section of the list that we have to sort slightly shorter by one element (as by this point, the last element should be sorted). 
* Thus, we simply do not need to sort the largest element, or in other words, for $n$ loops of sorting, we only need to check a list of $L-n$ of length, where $L$ represents the original length of the list $L$. 
```python
def bubblesort(L)
	loops = 0 
	hasSwapped = True #assume initial pass is not swapped
	while hasSwapped: 
		hasSwapped = False # reset value to check if list has been fully sorted
		for i in range(len(L)-1-loops): #increment by loops to minimize amount needed to sort 
			if L[i] > L[i+1]: 
				L[i+1], L[i] = l[i], L[i+1] #swap elements 
				hasSwapped = True #a swap has occured 
				continue 
		loops += 1 
```

Note that now, this sorting algorithm has a *best case* run time complexity of $O(n)$, as we simply only need to iterate through the length of the list. This sorting algorithm however now has a *worst-case* run complexity of $O(n^{2})$. 

To define / find this runtime complexity, consider that we analyze this function using the comparison within as our measurement, that is: 
```python
def bubblesort(L)
	loops = 0 
	hasSwapped = True 
	while hasSwapped: 
		hasSwapped = False 
		for i in range(len(L)-1-loops): 
			if L[i] > L[i+1]:               # \
				L[i+1], L[i] = l[i], L[i+1] # | c 
				hasSwapped = True           # /
				continue 
		loops += 1 
```