---
updated_at: 2026-10-21T09:29:01.674-04:00
edited_seconds: 760
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

> [!ila]- In Tutorial Addendum - Gaussian Elimination
> We can put the following system into the following matrix: 
> $$\begin{bmatrix}2 & 3 \\10 & 9\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1\\11\end{bmatrix}$$
> We want to transform our matrix $\mathbf{A}$ into  upper triangular matrix; note that we can do this by multiplying by $\begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}$: $$\begin{align}\begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}\begin{bmatrix}2 & 3\\ 10 & 9\end{bmatrix} \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1 & 0\\-5 & 1\end{bmatrix}\begin{bmatrix}1\\11\end{bmatrix} \\\begin{bmatrix}2 & 3 \\0 & -6\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}1\\6\end{bmatrix} \\\implies \begin{bmatrix}2\\0\end{bmatrix}x + \begin{bmatrix}3\\-6\end{bmatrix}y = \begin{bmatrix}1\\6\end{bmatrix} \\\implies \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}2\\-1\end{bmatrix}\end{align}$$
> > This is an example of Elementary Row Operations, where we multiply by some matrix with the same rank. 

> [!theorem] Question 2
> Consider the system of linear equations given below: $$\begin{align}ax+by=f \\cx+dy = g\end{align}$$
> We will assume that the first pivot $a\neq0$.
> 1. Elimination produces *what formula* for the second pivot? 
> 2. What condition must hold for the second pivot to be nonzero? 
> 3. Assuming the condition in part (2) holds, what is the value of $y$? 
> 
> > [!caution]- Answer
> > Gaussian Elimination provides the following: 
> > $$\begin{bmatrix}a & b \\c & d\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f\\g\end{bmatrix}$$For some value $t$ where $c-ta=0$; then note that $t=\frac{c}{a}$; 
> > $$\begin{bmatrix}a & b \\0 & d-bt\end{bmatrix} \begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f \\g - ft\end{bmatrix}$$The second pivot is then defined by some $d-bt$; where $t \neq 0$. 
> > For the second pivot to be nonzero, $d>bt$ or $d <bt$, but $d \neq bt$. 
> > 
> > Plugging in $t=\frac{c}{a}$; then: 
> > $$\begin{bmatrix}a & b \\0 & d-\frac{bc}{a}\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix} = \begin{bmatrix}f\\g-\frac{fc}{a}\end{bmatrix}$$
> > Then: $$\begin{align}\left( d-\frac{bc}{a} \right)y = g-\frac{fc}{a} \\y = \frac{\left( g-\frac{fc}{a} \right)}{d-\frac{bc}{a}} -= \frac{ga-fc}{da-bc}\end{align} $$

> Question 3
> A system of linear equations cannot have just two solutions. Let's examine why this is the case.
> 1. Consider a system of linear equations with 3 unknowns. Assume that two solutions are known: $(x,y,z)$ and $(X,Y,Z)$. What is another solution? 
> 2. If you know that $25$ planes in $\mathbb{R}^3$ meet in two points; where else do they meet? 
> > Answer
> > 1. Any solution that lies on a line between $(x,y,z)$ and $(X,Y,Z)$, Consider the system above; of $3$ hyperplanes in $\mathbb{R}^3$ (or in other words, three 2d planes). If they have two solutions; they can have either be collectively intersecting in a line. 
> > 	2. Or in other words, any solution of $\left( \frac{x+X}{2},\frac{y+Y}{2},\frac{z+Z}{2}  \right)$; since we have two equations within our system. 
> > 3. The $25$ planes in $\mathbb{R}^3$ meet in a line in R3 with the points included within that line;
> > 	4. Or any solution of points within each plane would work (if all of them are colinear). 

Question 4: 
> Consider the system of linear equations below: $$\begin{align}2x+5y+z & =0 \\4x+dy+z & =2 \\y-z & =3\end{align}$$
> The objective is to determine the equivalent upper triangular system. 
> 1. What is the upper triangular system for the value of $d$ in Part 1? 
> 2. What value of $d$ produces a zero pivot in row 3? 
> 3. Is there a solution to this system for the value of d in Part 3? 
>
> > Answer
> > Rewriting this into a matrix: 
> > 

$$
\begin{bmatrix}
2 & 5 & 1 \\
4 & d & 1 \\
0 & 1 & -1
\end{bmatrix} = \begin{bmatrix}
0\\2\\3
\end{bmatrix}
$$
Subtracting two row two from row three: 
$$
\begin{bmatrix}
2 & 5 & 1 \\
0 & d-10 & -1 \\
0 & 1 & -1
\end{bmatrix}=\begin{bmatrix}
0\\2\\3
\end{bmatrix}$$
Then subtracting row 3 by some multiple row two: 
$$
\begin{bmatrix}
2 & 5 & 1 \\
0 & d-10 & -1 \\
0 & 1-kd-10k & -1+1k
\end{bmatrix} = \begin{bmatrix}
0 \\2\\3-2k
\end{bmatrix}
$$
Then, solving the last line gives us: 
$$
\begin{align}
1-kd-10k-1+k & =3-2k \\
kd-10k+k & =3-2k \\
kd-7k=3 \\
kd-7k-3=0 \\
d=\frac{7k+3}{k}
\end{align}
$$
Note that if we define this matrix to be an upper triangular matrix; then $1-kd-10k=0$ as well, then
$$
\begin{align}
1-\frac{k(7k+3)}{k} - 10k  & = 0 \\
1-7k+3-10 & =0 \\
 k& =-\frac{6}{7}
\end{align}
$$
Then for $d$: 
$$
d=\frac{-6*3}{6}
$$

> Question 5
> Consider matrix $A$ given below: 

$$\begin{bmatrix}a & 2 & 3 \\a & a & 4 \\a & a & a\end{bmatrix}$$
For which three values of $a$ will elimination fail to product 3 non-zero pivots? 

Consider if we try to eliminate this into it's $U$ matrix form. 