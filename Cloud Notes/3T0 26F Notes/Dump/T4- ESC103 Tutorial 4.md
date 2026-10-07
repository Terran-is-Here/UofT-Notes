---
updated_at: 2026-10-07T09:22:00.510-04:00
edited_seconds: 110
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
```query
tag:#ESC103H1 [week:5]
```
--- 
## Questions: 

> Question 1
> 1. Find a 3x3 matrix with 3 independent columns and all nine entries equal to 1 or 2. 
> 2. In part (1), what is the maximum possible number of 1's? 
> > Answer
> > 1. $\begin{bmatrix}1 & 1 & 2\\1 & 2 & 1\\2 & 1 & 1\end{bmatrix}$
> > 2. $7$ maximum: $\begin{bmatrix}1 & 1 & 2\\1 & 1 & 1\\2 & 1 & 1\end{bmatrix}$

> Question 2: 
> Suppose matrix $\mathbf{A}$ is $5\times2$, with column vectors $\vec{a}_{1}$ and $\vec{a}_{2}$. We are now going to add one more column ($\vec{a}_{3}$) to produce matrix $\mathbf{B}$, now $5\times3$. Do $\mathbf{A}$ and $\mathbf{B}$ has the same column space if: 
> 1. $\vec{a}_{3}=\vec{0}$
> 2. $\vec{a}_{3}=\begin{bmatrix}1\\1\\1\\1\\1\\\end{bmatrix}$
> 3. $\vec{a}_{3}=\vec{a}_{2}-\vec{a}_{1}$
> > Answer
> > 1. Yes, column space remains the same. 
> > 2. No, $\vec{a}_{3}$ could be linearly independent to $\vec{a}_{1}$ and $\vec{a}$
