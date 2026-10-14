---
updated_at: 2026-10-14T09:46:16.631-04:00
edited_seconds: 510
course:
tags:
  - Tutorial
"Tutorial #": 0
Lecture Date: 2026-09-22
Week:
---
Hub: [[ESC103 Hub]]
Connected Notes: [[T4- ESC103 Tutorial 4]]
```query
tag:#ESC103H1 [week:6]
```
--- 

> Question 1
> Test the "truth" of the associative law: $(AB)C = A(BC)$: 
> * $\begin{bmatrix}1 & 1\end{bmatrix}\begin{bmatrix}1\\1\end{bmatrix}\begin{bmatrix}1 & 1 & 1\end{bmatrix}$
> * $\begin{bmatrix}1 & 2\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 3\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 4\\0 & 1\end{bmatrix}$
> > Answer

$$
\begin{align}
(\begin{bmatrix}1 & 1\end{bmatrix}\begin{bmatrix}1\\1\end{bmatrix})\begin{bmatrix}1 & 1 & 1\end{bmatrix} = \begin{bmatrix}2\end{bmatrix}\begin{bmatrix}1 & 1 & 1\end{bmatrix} = \begin{bmatrix}2 & 2 & 2\end{bmatrix} \\
\begin{bmatrix}1 & 1\end{bmatrix}\begin{bmatrix}1\\1\end{bmatrix} \begin{bmatrix}1 & 1 & 1\end{bmatrix} = \begin{bmatrix}1 & 1\end{bmatrix} \begin{bmatrix}1 & 1 & 1 \\1 & 1 & 1\end{bmatrix} = \begin{bmatrix}
2 & 2 & 2
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
\begin{bmatrix}1 & 2\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 3\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 4\\0 & 1\end{bmatrix} = \begin{bmatrix}1 & 5 \\0 & 1\end{bmatrix}\begin{bmatrix}1 & 4\\0 & 1\end{bmatrix} = \begin{bmatrix}1 & 9 \\0 & 1\end{bmatrix} \\
\begin{bmatrix}1 & 2\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 3\\0 & 1\end{bmatrix}\begin{bmatrix}1 & 4\\0 & 1\end{bmatrix} = \begin{bmatrix}1 & 2\\0 & 1\end{bmatrix}\begin{bmatrix}1  & 7\\0 & 1\end{bmatrix} = \begin{bmatrix}1 & 9 \\0 & 1\end{bmatrix}
\end{align}

$$



> Question 2
> Let $A = \begin{bmatrix}2 & -2 & 1 & 6 & 0 \\  1 & -1 & 0 & 2 & 0 \\  3 & -3 & 0 & 6 & 1\end{bmatrix}$; We want to factorize this matrix into $A=CR$. 
> 1. Construct matrix $C$ from matrix $A$ by going left to right and putting each column of $A$ into $C$ if that column is not a combination of earlier columns. 
> 2. Construct matrix $R$. Note: If $C$ has $r$ columns, then $R$ must have $r$ rows. 
> > Answer
> > 1. $$C = \begin{bmatrix}2 & 1 & 0\\1 & 0 & 0\\3 & 0 & 1\end{bmatrix}$$
> > 2. $$R = \begin{bmatrix}1 & -1 & 0 & 2 & 0 \\0 & 0 & 1 & 2 & 0 \\0 & 0 & 0 & 0 & 1\end{bmatrix}$$

> Question 3
> If all columns of $A = \begin{bmatrix}\vec{a} & \vec{a} & \vec{a}\end{bmatrix}$ are vectors in $\mathbb{R}^n$ and where $\vec{a} \neq \vec{0}$, what are $C$ and $R$, where $A=CR$? 
> > Answer
> > $C=\begin{bmatrix}\vec{a}\end{bmatrix}$, $R=\begin{bmatrix}1 & 1 & 1\end{bmatrix}$. 


> Question 4
> Why is it not possible for a matrix with 4 rows and 7 columns to have 5 independent columns? 
> Answer: 
> > Consider: 4 Rows imply the existence of 4 basis vectors. Having 5 columns implies that we can reach R5 with R4 vectors, which is a contradiction. 

> Question 5
> Complete the following $2\times2$ matrices to meet the requirements specified: 
> 1. $\begin{bmatrix}3 & 6\\5 & x\end{bmatrix}$ (Rank 1) 
> 2. $\begin{bmatrix}6 & a\\7 & b\end{bmatrix}$( Orthogonal Columns)
> 3. $\begin{bmatrix}2 & a\\3 & 6\end{bmatrix}$ ( Rank 2) 
> 4. $\begin{bmatrix}3 & 4\\? & -3\end{bmatrix}$ $A^2 = I$
> > Answer
> > 1. $x=10$
> > 2. $\begin{bmatrix}6\\7\end{bmatrix}\cdot \begin{bmatrix}a\\ b\end{bmatrix} = 0 =6a+7b$

> Question 6

> Question 7

> Question 8

> Question 9