---
updated_at: 2026-11-13T12:28:36.468-05:00
edited_seconds: 210
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
> Maybe 


We can compare their similarity by using the cosine similarity: 
$$
\text{cosine similarity}(a,b) = \frac{\vec{a}\cdot \vec{b}}{\sqrt{ \sum_{i=1}^{N} a_{i}^{2}* \sum_{i=1}^{N} b_{i}^{2} }}
$$
Note that the dot product above mainly applies for words which are present in both sentences. If we define each dimension as some word present, then the corresponding dot product will solely link to the words which are present in both; whilst the magnitude will be present in regardless of both. Note that the $\vec{a}\cdot \vec{b}$  term above relates to the relatedness of those words; whilst as the magnitude in the denominator point to the other semantic directions present in some higher-dimensional space. 

## String Methods
Recall that Strings by themselves are immutable; we cannot inherently change the data present within a stri.g 
