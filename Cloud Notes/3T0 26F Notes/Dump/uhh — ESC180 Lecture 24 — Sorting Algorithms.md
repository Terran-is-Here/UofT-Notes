---
updated_at: 2026-11-11T17:59:51.349-05:00
edited_seconds: 740
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
* If we measure our time complexity with respects to **how many times the code within the loop runs** (as we did in lecture), then the best case time complexity is actually still $O(n)$ (as we still have to compare all elements at least once). 

To define / find this runtime complexity, consider that we analyze this function using the **loop within** as our measurement, that is: 
```python
def bubblesort(L)
	loops = 0 
	hasSwapped = True 
	while hasSwapped: 
		hasSwapped = False 
		for i in range(len(L)-1-loops): 
			if L[i] > L[i+1]:               # \
				L[i+1], L[i] = l[i], L[i+1] #  > Let this take some time c
				hasSwapped = True           # /
				continue 
		loops += 1 
```
If our list is in it's worst case, then we note that our `hasSwapped` term will not ever tick early. 
* For our for loop, this runs for `k` times, where `k` is some function of `k`
```python
		for i in range(len(L)-1-loops): 
			if L[i] > L[i+1]:               # \
				L[i+1], L[i] = l[i], L[i+1] #  > Let this take some time c, and uses some term of looks n 
				hasSwapped = True           # /
				continue 
```
* Note that the loop within will run progressively less times, that is for the iterations it goes from n-1, n-2, n-3 ... 3, 2, 1 times

Thus we find that the inner number of the inner loop iterations is simply the sum of the arithmetic sequence: 
$$
\frac{n(n-1)}{2} \to \frac{n^{2}}{2}-\frac{n}{2}
$$
The runtime of this function / sorting algorithm is therefore $O(n^{2})$ for some large $n^{2}$. 
## Insertion Sort
Insertion Sort basically operates with the principle of finding the largest value within the set, and simply moving it to the end of the list; then we simply take the next value. We note that this value is going to be sorted, and thus sort the corresponding sub list. In practice, this means that we create a "semi-sorted" list, where the sublist within is relatively sorted to itself.  

```python
def insertionSort(L): 
	
	for k in range(1,len(L)):  #unsorted values
		val = L[k] #value attempting to insert into our semi-sorted list...
		loc = k-1 #initialize location to be some value before; where val could go
		while val < L[loc] and loc >= 0: #If this is true; then value needs to move towards the left by one space
			L[loc+1] = L[loc] #shift elements to the right by one to make space 
			loc -= 1 #checking next term of our value should be swapped 
		
		#val should go at some loc+1 to the right, then
		L[loc+1] = val #inserting value at the right location
	
```
* Consider that `k` gives us the start of the unsorted list, and `loc` simply lets us shift the values to eventually sort the sorted value into the list. 

Consider now, what is the runtime complexity of *insertion sort*? We can define our metric of time as the amount of times that the inner-most loop literates. 
* The while loop occurs per every "right shift" where we shift elements towards the right; 

> For the best case scenario, where the list becomes fully sorted; then the while loop only runs *once* (to evaluate if `val < L[loc]`). This runs for every for loop iteration, which runs n-1 times, which means $O(n)$ for the best case scenario. 

> For the worst case scenario, where the list is in a reverse sorting order: 
> Then our while loop within runs when we have to perform multiple right shifts to make room for our value; thus our while loop runs for some $k$ times, where this corresponds to the length of the semi-sorted region of our list. 
> 
> Considering this in terms of the number of outer for loop iterations: 
> $$k=1,2,\dots,n-1$$
> Which is also another arithmetic sequence, then this is equivalent to $\frac{n(n-1)}{2}$, meaning that $O(n^{2})$. 