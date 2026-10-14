---
updated_at: 2026-10-14T09:11:17.871-04:00
edited_seconds: 330
course: ESC103H1
tags:
  - Tutorial
  - ESC103H1
"Tutorial #": 4
Lecture Date: 2026-09-22
Week: 5
---
Hub: [[ESC103 Hub]]
Connected Notes: [[T3 — ESC103 Tutorial 3]]
Next: [[T5 — ESC103 Tutorial 5]]
```query
tag:#ESC103H1 [week:5]
```
--- 
## Useful Concepts
> [!caution]
> Any matrix can be defined as a transformation; that we take a vector and map it to another vector. An *inverse* maps a new vector and maps it towards our original space. We can thus only take the inverse of a full rank matrix (that is, an inverse) (bijective/surjective, 1:1 ratio for points -> corresponding linear transformations) 

## Questions & Answers 

> [!theorem] Question 1
> 1. Find a 3x3 matrix with 3 independent columns and all nine entries equal to 1 or 2. 
> 2. In part (1), what is the maximum possible number of 1's? 
> 
> > [!caution]- Answer
> > 1. $\begin{bmatrix}1 & 1 & 2\\1 & 2 & 1\\2 & 1 & 1\end{bmatrix}$
> > 2. $7$ maximum: $\begin{bmatrix}1 & 1 & 2\\1 & 1 & 1\\2 & 1 & 1\end{bmatrix}$

> [!theorem] Question 2: 
> Suppose matrix $\mathbf{A}$ is $5\times2$, with column vectors $\vec{a}_{1}$ and $\vec{a}_{2}$. We are now going to add one more column ($\vec{a}_{3}$) to produce matrix $\mathbf{B}$, now $5\times3$. Do $\mathbf{A}$ and $\mathbf{B}$ has the same column space if: 
> 1. $\vec{a}_{3}=\vec{0}$
> 2. $\vec{a}_{3}=\begin{bmatrix}1\\1\\1\\1\\1\\\end{bmatrix}$
> 3. $\vec{a}_{3}=\vec{a}_{2}-\vec{a}_{1}$
> 
> > [!caution]- Answer
> > 1. Yes, column space remains the same. 
> > 2. No, $\vec{a}_{3}$ could be linearly independent to $\vec{a}_{1}$ and $\vec{a}_{2}$. 
> >    Moreso, it depends if $\vec{a_{3}}$ can be expressed as a linear combination of $\vec{a_{1}}$ and$\vec{a_{2}}$
> > 3. Yes, $\vec{a}_{3}$ is a linear combination of $\vec{a}_{2}$, $\vec{a}_{3}$

> [!theorem] Question 3: 
> Assume the vectors $\vec{v},\vec{w}$ are non-zero and non-parallel. Which of the following sets of vectors are linearly independent? 
> 1. $\{ \vec{0},\vec{v},\vec{w} \}$
> 2. $\{ \vec{v},\vec{w},3\vec{v}-4\vec{w} \}$
> 3. $\{ \vec{v},\vec{w},\vec{v}\times \vec{w} \}$
>
> > [!caution]- Answer
> > 1. Yes, linearly independent (since $\vec{v},\vec{w}$ are non-zero)
> > 2. No, third vector is a linear combination of the other. 
> > 3. Yes, $\vec{v}\times \vec{w}$ provides a vector orthogonal to $\vec{v},\vec{w}$, meaning it is linearly independent. 

> [!theorem] Question 4: 
> If two matrices are $\mathbf{A,B}$ $5\times2$ matrices which have independent columns, then $\mathbf{A}+\mathbf{B}$ will also have independent columns. True or false? 
> > [!caution]- Answer
> > False. Take the following two matrices: $$\begin{bmatrix}1 & 0 \\0 & 0\\0 & 0\\0 & 0\\0 & 1\end{bmatrix} + \begin{bmatrix}0 & 1 \\0 & 0\\0 & 0\\0 & 0\\1 & 0\end{bmatrix} = \begin{bmatrix}1 & 1 \\0 & 0\\0 & 0\\0 & 0\\1 & 1\end{bmatrix}$$
> > Thus, this statement is false. Note that we simply swapped the columns of $\mathbf{A}$ in $\mathbf{B}$, that is $\mathbf{A}=\begin{bmatrix}c_{1}&c_{2}\end{bmatrix}$, $\mathbf{B}=\begin{bmatrix}c_{2}&c_{1}\end{bmatrix}$, then $\mathbf{A+B} =\begin{bmatrix}c_{1}+c_{2} & c_{1}+c_{2}\end{bmatrix}$. 

> [!theorem] Question 5: 
> 1. Solve this system of equations $\mathbf{S}\vec{y}=\vec{c}$ for the unknowns in $\vec{y}$ in terms of the constants in $\vec{c}$ by taking advantage of the triangular structure of matrix $\mathbf{S}$: $$\mathbf{S}\vec{y} = \begin{bmatrix}1 & 0 & 0 \\1 & 1 & 0 \\1 & 1 & 1\end{bmatrix}\begin{bmatrix}y_{1}\\y_{2}\\y_{3}\end{bmatrix} = \vec{c} =\begin{bmatrix}c_{1}\\c_{2}\\c_{3}\end{bmatrix}$$
> 2. Express the solution in part 1 for $\vec{y}$ as a matrix $\mathbf{T}$ times the vector $\vec{c}$. 
> 3. The matrix $\mathbf{T}$ is called the inverse of $\mathbf{S}$, Are the columns of $\mathbf{S}$ independent or dependent? 
> 
> > [!caution]- Answer: 
> > 1. Solving via Row picture gives us $$\begin{align}1y_{1}+0y_{2}+0y_{3} = c_{1} \to y_{1}&=c_{1} \\1y_{1}+1y_{2}+0y_{3} = c_{2} \to y_{2}&=c_{2}-c_{1} \\1y_{1}+1y_{2}+1y_{3} = c_{3} \to y_{1}&=c_{3}-c_{2}\end{align}$$
> >    Thus: $$\vec{y}=\begin{bmatrix}c_{1} \\c_{2}-c_{1} \\c_{3}-c_{2}\end{bmatrix}$$
> > 2. As some matrix $\mathbf{T}$, we need to solve for the inverse, that is: $$\begin{align}\mathbf{T}\vec{c}&=\vec{y} \\\mathbf{T}\begin{bmatrix}c_{1}\\c_{2}\\ c_{3}\end{bmatrix} &= \begin{bmatrix}c_{1} \\c_{2}-c_{1} \\c_{3}-c_{2}\end{bmatrix} \\\text{ Through inspection, }\mathbf{T} &= \begin{bmatrix}1 & 0 & 0 \\-1 & 1 & 0 \\0 & -1 & 1\end{bmatrix}\end{align}$$
> > 3. The columns of $\mathbf{S}$ are linearly independent. $\mathbf{S}$ can only have an inverse matrix $\mathbf{T}$ if and only if $\mathbf{S}$'s column vectors are independent. 

