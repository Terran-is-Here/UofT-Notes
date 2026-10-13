---
updated_at: 2026-10-13T17:33:28.732-04:00
edited_seconds: 890
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 11
Lecture Date: 2026-10-09
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[10 — Matrix Multiplication]]
Next: [[12 — Elementary Row Operations]]

> [!quote] Learning Objectives 
> * Construct a matrix $\mathbf{C}$ from matrix $\mathbf{A}$ using the definition of independent vectors. 
> * Construct a matrix $\mathbf{R}$ such that $\mathbf{A}=\mathbf{CR}$
> * Explain the significance of $\mathbf{R,C}$ with respects to $\mathbf{A}$

> [!quote] Recommended Reading 
> [[08 — Matrix Vector Products]], and [[09— Basic Linear Algebra Concepts]] are also useful for this section as they pop up again and again. 
--- 
 
# Lecture Notes
## Matrix Decomposition
The general concept of Matrix Decomposition, is that given some matrix $\mathbf{A}$, we should be able to express this as a product of two matrices $\mathbf{C,R}$; that is: 
$$
\mathbf{A}= \mathbf{C}\mathbf{R}
$$
The concept is that we can break up some $\mathbf{A}$ (which could be complex) into two simpler matrices $\mathbf{C,R}$. We do this to try and make some matrices much easier to compute. 

> [!theorem] Constructing $\mathbf{C}$ from $\mathbf{A}$ (where $A$ is a $m\times n$ matrix) 
> We want to construct our matrix $\mathbf{C}$ with solely the linearly independent columns of $\mathbf{A}$, or in other words, the basis column vectors of a matrix $\mathbf{A}$. 
> For instance: 
> $$\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix}$$Factoring this above requires us to note which columns are linearly independent. 
> 1. If column 1 of $\mathbf{A}$ is not $\vec{0}$, put the first column in $\mathbf{C}$. 
> 2. If column $n$ of $\mathbf{A}$ is not some multiple / scalar combination of the currently present columns, put column two into $\mathbf{C}$. Otherwise, skip. 
> 	1. In lecture, this was written as "if column two of A is not some multiple of column 1, then put column 2 in c, otherwise skip."
> 3. Repeat step 2 until all $\mathbf{A}$ have been iterated over. 
> 
> Thus, for our matrix above; then $\mathbf{C}$ per step is: 
> $$\begin{bmatrix}2\\4\\1\end{bmatrix} \to \begin{bmatrix}2\\4\\1\end{bmatrix} \to \begin{bmatrix}2 & 4 \\4 & 8 \\1 & 5\end{bmatrix}$$
> > Note then, that $\mathbf{C}$ should have $r$ columns; where $r\leq n$, and all column vectors inside are linearly independent. 
> > > In this case, the column space of $\mathbf{A}$ is equal to the column space of $\mathbf{C}$; that is the column vectors of $\mathbf{C}$ are the basis vectors of the column space of $\mathbf{A}$
> > > And $r$ represents the rank of $\mathbf{C}$, which represents the rank of $\mathbf{A}$. 
> 
> Note that for a big matrix $\mathbf{A}$, checking the linear independence of all of it's corresponding column vectors may be computationally intensive. 

> Constructing $\mathbf{R}$ from $\mathbf{C}$
> Retaking our example matrix: $$\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix}$$
> Note from the above step; that $\mathbf{C} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}$
> We now need to solve this:

$$
\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}\mathbf{R}
$$

---
# Pre-Lecture Notes
## CR Matrices 
Given the following matrix: 
$$
\mathbf{A} = \begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix}
$$
A matrix $\mathbf{C}$ can be created from the linearly independent columns of $\mathbf{A}$: 
$$\mathbf{C} = \begin{bmatrix}1 & 4 \\3 & 2 \\0 & 2\end{bmatrix}$$
Note; that $\begin{bmatrix}7\\11\\2\end{bmatrix} = 3\begin{bmatrix}1\\3\\0\end{bmatrix}+ 1\begin{bmatrix}4\\2\\2\end{bmatrix}$, That is to say that this matrix is *linearly* dependent. Then we can express the matrix $\mathbf{R}$ as the following matrix: 
$$
\mathbf{R} = \begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & 1
\end{bmatrix}
$$
Where: 
$$
\begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix} = \begin{bmatrix}1 & 4\\3 & 2\\0 & 2\end{bmatrix}\begin{bmatrix}1 & 0 & 3\\0 & 1 & 1 \end{bmatrix}
$$
Recall that matrix multiplication **always** works in a row-column arrangement. That is; we iterate through rows of $\mathbf{A}$ before iterating through columns of some $\mathbf{B}$ in $\mathbf{AB}$. 
> [!ila] Important Idea
> Note that the Column Vectors of $\mathbf{C}$ are the basis vectors of the column space of $\mathbf{A}$, or in other words; they represent the linearly independent vectors in $\mathbf{A}$ (and thus it's corresponding rank and dimensions).
> 

### Significance of R
Note however that the matrix $\mathbf{R}$ is something special: it is the Row-Reduced Echelon Form of $\mathbf{A}$; though it's kind of outside the bounds of this note for now to work on it. 

## Solving Ax=0 using A=CR 
> [!caution] Note
> This section is *technically* meant for next lecture, though I wouldn't be surprised if it's not mentioned in this lecture. Will edit in the future if it is moved to a future lecture. 


A = CR provides us a useful tool for solving our previous $\mathbf{A}\vec{x} = \vec{b}$ equations that we have tackled in the past in a bit more of an algebraic method. Take the following matrix: 
$$
\mathbf{A}=\begin{bmatrix} 
1 & 3 \\
2 & 3 \\
1 & 3
\end{bmatrix} = \begin{bmatrix}1 & 3\\2 & 3\\1 & 3\end{bmatrix}\begin{bmatrix}
1 & 0\\0 & 1\end{bmatrix}
$$
That is, the corresponding $\mathbf{R}=\mathbf{I}$ and $\mathbf{C}=\mathbf{A}$. We know that the span of $\mathbf{A}$ is entirely composed of linearly independent vectors then: 
$$
\begin{bmatrix}1 & 3\\2 & 3\\ 1 & 3\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\end{bmatrix} = \begin{bmatrix}0\\0\\0\end{bmatrix}
$$
The only solutions to this are if $\vec{x}=\vec{0}$. 

However, now consider the following linearly dependent matrix: 
$$
\begin{bmatrix}1 & 3 & 5 \\2 & 3 & 7 \\1 & 3 & 5\end{bmatrix} = \begin{bmatrix}1 & 3 \\2 & 3\\1 & 3\end{bmatrix}\begin{bmatrix}1 & 0 & 2 \\0 & 1 & 1\end{bmatrix}
$$
Now broken up into some $\mathbf{A=CR}$; then resubstituting this into $\mathbf{A}\vec{x}=\vec{0}$: 
$$
\begin{bmatrix}1 & 3\\2 & 3\\ 1 & 3\end{bmatrix}\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}=\begin{bmatrix}0\\0\\0\end{bmatrix}
$$
Note that $\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}$ Results in some vector $\begin{bmatrix}b_{1}\\b_{2}\end{bmatrix}$ (we lose a row in $\mathbf{R}$ over $\mathbf{A}$). Since $\begin{bmatrix}1 & 3\\2 & 3\\1 & 3\end{bmatrix}$ is linearly independent; taking our case above; then the only way this equals 0, is if it's multiplied by 0. 
Or in other words: 
$$
\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = \vec{0}
$$
Thus: 
$$
x_{1}\begin{bmatrix}1 \\0\end{bmatrix} + x_{2}\begin{bmatrix}0\\1\end{bmatrix} + x_{3}\begin{bmatrix}2\\1\end{bmatrix} = \begin{bmatrix}0\\0\end{bmatrix}
$$
$$
x_{1}\begin{bmatrix}1 \\0\end{bmatrix} + x_{2}\begin{bmatrix}0\\1\end{bmatrix} = -x_{3}\begin{bmatrix}2\\1\end{bmatrix}
$$
Note that the solution of this now; is: 1
$$
\begin{align}x_{1}=-2x_{3} \\x_{2}=-x_{3}\end{align}
$$
We can *parameterize* $x_{3}$ (or in other words, it is the *free* variable) to some value $t$, and then the corresponding systems of equations pop out: 
$$
\begin{align}
x_{1}&=-2t \\
x_{2}&=-1t \\
x_{3}&=t
\end{align}
$$
Which then implies 
$$\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = t\begin{bmatrix}-2\\-1 \\1\end{bmatrix}$$
As the solution to our above expression of $\mathbf{A}\vec{x}=\vec{0}$. Note that this entire expression leads us to two more core definitions for Linear Algebra: 
> [!theorem] Nullspace/Kernel
> The **nullspace** (otherwise known as the Kernel) of some matrix $\mathbf{A}$ is the vector space for the solution of $\vec{x}$ in $\mathbf{A}\vec{x}=\vec{0}$. 

> [!theorem] Nullity
> **Nullity** is the *Dimension* of the null space; that is it's corresponding amount of basis vectors. 


