---
updated_at: 2026-11-13T13:08:18.533-05:00
edited_seconds: 360
course:
tags:
  - ESC180H1
"Lecture #": 0
Lecture Date: 2026-11-13
Week:
---
Hub: 
Previous: [[uhh — ESC180 Lecture 24 — Sorting Algorithms]]
Next:

--- 
# Lecture Notes
## Creating Semantic Descriptors & Project 3
Consider the problem for trying to relate the relatedness of a word to another word, that is how close is "cow" to "vehicle" over "animal"? We can't directly compare these values, but we can define them as vectors; where for a certain word, we can link it as a vector where the other elements are simply the words that appear in the other words. 

For instance: 
```python
matrix_man_relatedness = {"i": 3, "am": 3, "a": 2, "sick": 1, "spiteful": 1, "an": 1, "unattractive": 1} #For the sentences where the word "man" is found; these are the pieces of text found. 
```

> [!ila] In Lecture Idea
> Maybe consider implementing this as a set of nested dictionaries: one to correspond to the word, and the corresponding value representing the key value pair present. 

> [!ila] Another Idea
> Consider, when processing a sentence, we can simply make a dictionary counting the number of words present within that string. Then, we can simply iterate over the keys within that dictionary, and increment corresponding values within the dictionary. This should theoretically ensure $O(n)$ computational complexity. 
> > A naïve solution where you simply iterate per word, and then count all the rest of the words and increment accordingly, would be the one that forces a $O(n^{2})$ time complexity wise. 
> > As for every $n$ word, you loop over the $n-1$ words present within a sentence, meaning a time complexity of $n^{2}-n$ or $O(n^{2})$. 
> 
> > With further thought, this would still be $O(n^{2})$, albeit with slight optimizations we are simply iterating over a sparse dictionary. 



We can compare their similarity by using the cosine similarity: 
$$
\text{cosine similarity}(a,b) = \frac{\vec{a}\cdot \vec{b}}{\sqrt{ \sum_{i=1}^{N} a_{i}^{2}* \sum_{i=1}^{N} b_{i}^{2} }}
$$
Note that the dot product above mainly applies for words which are present in both sentences. If we define each dimension as some word present, then the corresponding dot product will solely link to the words which are present in both; whilst the magnitude will be present in regardless of both. Note that the $\vec{a}\cdot \vec{b}$  term above relates to the relatedness of those words; whilst as the magnitude in the denominator point to the other semantic directions present in some higher-dimensional space. 

## String Methods
Recall that Strings by themselves are immutable; we cannot inherently change the data present within a string. Consider the problem if we wanted to reverse a string, we can implement this trivially using string slicing: 

```python
def reverse_string(s): 
	return s[::-1] #reverse order, include both endpoints in terms of indices. 
```

Consider if slicing is not available; maybe we can do this as an iteration: 
```python
def reverse_string(s): 
	out = ""
	for i in range(len(s)-1,-1,-1): 
		out += s[i]
	return out 
```
Where we build up a string and eventually return it afterwards. Alternatively: 
```python
def reverse_string(s): 
	out = ""
	for character in s: 
		out = s + out #where we add it to the start of the string, "A" + "PO" = "APO"
	return out 
```

