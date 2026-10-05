---
Created: September 28th 2026, 9:46:55 pm
updated_at: 2026-10-05T12:31:36.210-04:00
edited_seconds: 480
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
## Linear Independence (LEC) 
For the purposes of this note, we will notate the $\mathbf{A}\vec{x}=\vec{b}$ as the following: 
$$\begin{bmatrix}\vdots & \vdots & \dots  & \vdots \\\vec{c_{1}} & \vec{c_{2}} & \dots  & \vec{c_{n}} \\\vdots & \vdots & \dots & \vdots\end{bmatrix}
\begin{bmatrix}
x_{1}\\x_{2}\\\vdots\\x_{n}
\end{bmatrix}=\vec{b}
$$
Recall from [[07 — Matrix Operations]], Column Vectors of $\mathbf{A}$ are *linearly independent* if each vector cannot be expressed as a linear combination of other vectors. For instance, if we define $\vec{r}_{1},\vec{r}_{2}$, where $\vec{r}_{1}+\vec{r}_{2}=\vec{r}_{3}$. Note that if we try to equate a linear combination of $\vec{r}_{1},\vec{r}_{2},\vec{r}_{3}=\vec{0}$  we can make a case where the scalar multiples of $\vec{r_{1},r_{2},r_{3}}$ are not equal to 0. 

Consider now the case where $\vec{a_{1}},\vec{a_{2}},\vec{a_{3}}$, where $\vec{a_{3}}$ is orthogonal to $\vec{a}_{1},\vec{a}_{2}$. Note that the only case for $\vec{a}_{1}+\vec{a}_{2}+\vec{a}_{3}=0$ is if $0$ is multiplied across any of our linearly independent vectors (since we can't easily combine back to where it's equal to 0). We call this system Linearly Independent. This leads us to the precise definition of linear independence. 

> Column Vectors are *linearly independent* when the only combination of $x_{1},x_{2},\dots, x_{n}$ that produces $A\vec{x}=0$ is $x_{1},x_{2},\dots,x_{n}=0$; or in other words: 
$$
\begin{bmatrix}\vdots & \vdots & \dots  & \vdots \\\vec{c_{1}} & \vec{c_{2}} & \dots  & \vec{c_{n}} \\\vdots & \vdots & \dots & \vdots\end{bmatrix}
\begin{bmatrix}
0\\0\\\vdots\\0
\end{bmatrix}=\vec{0}
$$
Then $\mathbf{A}$ is composed of linearly independent column vectors. 

Retaking an earlier example: 
$$
A_{1}\vec{x} = \begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = 0\vec{}
$$
If we do this via row picture: 
$$\begin{align}1x_{1}+0x_{2}+0x_{3} &=0 \implies x_{1}=0 \\2x_{1}+4x_{2}+0x_{3} & = 0\implies x_{2}=0 \\3x_{1}+5x_{2}+6x_{3} & = 0\implies x_{3}=0 \\& \implies \vec{x}=\vec{0}\end{align}$$
Based on this, then: 
* The combination of column vectors span all of $\mathbb{R}^3$.
* The column vectors of $\mathbf{A}$ is linearly independent. 

> Take the following example: 
> $$\mathbf{A_{2}}=\begin{bmatrix}1 & 2 & 3 \\1 & 4 & 5 \\6 & 0 & 6\end{bmatrix}, \vec{x} = \begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}$$
> Check if this is Linearly Independent via column picture. Note that at a glance, $\vec{c}_{3} = \vec{c}_{1}+\vec{c}_{2}$: 
> $$1\begin{bmatrix}1\\1\\6\end{bmatrix} + 1\begin{bmatrix}2\\4\\0\end{bmatrix} = \begin{bmatrix}3\\5\\6\end{bmatrix}$$
> Since we can express $\vec{c}_{3}$ as some linear combination of $\vec{c}_{1}+\vec{c}_{2}$, we can show the following: $$1\begin{bmatrix}1\\1\\6\end{bmatrix} + 1\begin{bmatrix}2\\4\\0\end{bmatrix} - 1\begin{bmatrix}3\\5\\6\end{bmatrix} =\begin{bmatrix}0\\0\\0\end{bmatrix}$$
> Since we can show that a non-0-scalar solution for a linear combination to 0 exists, we can say that: $$\vec{x} = \begin{bmatrix}1\\1\\-1\end{bmatrix} \to \mathbf{A_{2}}\vec{x}=0\vec{}$$
> That is, the column vectors of $\mathbf{A}$ are not linearly independent. 

> Take the following example: 
$$
\mathbf{A_{3}} = \begin{bmatrix}1 & 3 & 4 \\2 & 6 & 8 \\5 & 15 & 20\end{bmatrix}
$$


---
# Pre-Lecture Notes
## Linear Independence
A given set of vectors $S$ is linearly dependent if each vector cannot be expressed as the linear combination of another vector. This is more formally defined as: 
$$
S = \{ \vec{v}_{1},\vec{v}_{2},\vec{v} \} = \left\{ \begin{bmatrix}a_{1}\\a_{2}\\a_{3}\end{bmatrix}, \begin{bmatrix}b_{1}\\b_{2}\\b_{3}\end{bmatrix},\dots,\begin{bmatrix}?_{1}\\?_{2}\\?_{3}\end{bmatrix} \right\}
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
