---
updated_at: 2026-10-14T10:27:16.557-04:00
edited_seconds: 340
course: ESC103H1
tags:
  - Tutorial
  - ESC103H1
"Tutorial #": 6
Lecture Date: 2026-10-21
Week: 8
---
Hub: [[ESC103 Hub]]
Connected Notes: [[T5 — ESC103 Tutorial 5]]
```query
tag:#ESC101H1 [week:7]
```
--- 

> Question 1
> Consider the system of linear equations given below: $$\begin{align} 2x+3y & =1 \\10x+9y  & =11\end{align}$$

> [!ila] In Tutorial Addendum
> We can put the following system into the following matrix: 
> $$\begin{bmatrix}2 & 3 \\10 & 9\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1\\11\end{bmatrix}$$
> We want to transform our matrix $\mathbf{A}$ into  upper triangular matrix; note that we can do this by multiplying by $\begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}$: $$\begin{align}\begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}\begin{bmatrix}2 & 3\\ 10 & 9\end{bmatrix} \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}\begin{bmatrix}1\\11\end{bmatrix} \\\begin{bmatrix}2 & 3 \\0 & -6\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1\\6\end{bmatrix} \\\implies \begin{bmatrix}2\\0\end{bmatrix}x + \begin{bmatrix}3\\-6\end{bmatrix}y = \begin{bmatrix}1\\6\end{bmatrix} \\\implies \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}2\\-1\end{bmatrix}\end{align}$$
> > This is an example of Elementary Row Operations, where we multiply by some matrix with the same rank. 

> Question 2
> Consider the system of linear equations given below: $$\begin{align}ax+by=f \\cx+dy = g\end{align}$$
> We will assume that the first pivot $a\neq0$.
> 1. Elimination produces *what formula* for the second pivot? 
> 2. What condition must hold for the second pivot to be nonzero? 
> 3. Assuming the condition in part (2) holds, what is the value of $y$? 
> 
> > Answer
> > Gaussian Elimination provides the following: 
> > $$\begin{bmatrix}a & b \\c & d\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f\\g\end{bmatrix}$$For some value $t$ where $c-ta=0$; then note that $t=\frac{c}{a}$; 
> > $$\begin{bmatrix}a & b \\0 & d-bt\end{bmatrix} \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f \\g - ft\end{bmatrix}$$The second pivot is then defined by some $d-bt$; where $t \neq 0$. 
> > For the second pivot to be nonzero, $d>bt$ or $d <bt$, but $d \neq bt$. 
> > 
> > Plugging in $t=\frac{c}{a}$; then: 

$$\begin{bmatrix}a & b \\0 & d-\frac{bc}{a}\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f\\g-\frac{fc}{a}\end{bmatrix}$$
