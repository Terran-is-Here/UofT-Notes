---
Created: September 28th 2026, 9:46:55 pm
updated_at: 2026-09-29T17:48:53.052-04:00
edited_seconds: 220
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 8
Lecture Date: 2026-09-29
Week: 4
---
Hub: [[ESC103 Hub]]
Previous: [[08 — Matrix Vector Products]], [[07 — Matrix Operations]] (In-Lecture Insertion)
Next: [[09 — Matrix Multiplication]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Linear Independence
A given set of vectors $S$ is linearly dependent if each vector cannot be expressed as the linear combination of another vector. This is more formally defined as: 
$$
S = \{ \vec{v}_{1},\vec{v}_{2},\vec{v} \} = \{ \begin{bmatrix}a_{1}\\a_{2}\\a_{3}\end{bmatrix}, \begin{bmatrix}b_{1}\\b_{2}\\b_{3}\end{bmatrix},\dots,\begin{bmatrix}?_{1}\\?_{2}\\?_{3}\end{bmatrix} \}
$$
The set above is linearly independent if the only valid linear combination for this to be equal to $\vec{0}$ is for all the coefficients to be 0, that is: 
$$
0\vec{v}_{1} + 0\vec{v}_{2} \dots +0\vec{v}_{n} = \vec{0} \implies \text{Set S is Linearly Independent}
$$
Geometrically, what this means is that none of our vectors are parallel to each other. 


## Vector Space
* A vector space for a set of *vectors* is defined as the space *formed* by all linear combinations of these vectors; otherwise known as the *span* of the set of vectors. 
* The *dimension* of a vector space is equivalent to the number of *linearly independent vectors* which can span this space. 
* The basis of a vector space is any set of linearly independent vectors that *span* the space. The number of basis vectors can be called the dimension of such a space. 
	* For instance, a plane defined by two basis vectors has a dimension of two. 

## Column Space
* The column space of a matrix $\mathbf{A}$ is defined as the *span* of all the column vectors of $A$, that is, it is equivalent to the *vector space* formed by the column vectors of $\mathbf{A}$. 
	* Alternatively, the column space is all linear combinations of the columns of $\mathbf{A}$
	* Alternatively, the column space is all possible $\mathbf{A}\vec{x}$ for all possible $\vec{x}$. 

* The *rank* of a matrix $\mathbf{A}$ is the *dimension* of the Column Space, or in other words, $n$ value of an $m\times n$ $\mathbf{A}\vec{r} = \vec{b}$. 
