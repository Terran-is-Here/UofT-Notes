---
updated_at: 2026-10-07T09:40:24.577-04:00
edited_seconds: 220
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

> Question 3: 
> Assume the vectors $\vec{v},\vec{w}$ are non-zero and non-parallel. Which of the following sets of vectors are linearly independent? 
> 1. $\{ \vec{0},\vec{v},\vec{w} \}$
> 2. $\{ \vec{v},\vec{w},3\vec{v}-4\vec{w} \}$
> 3. $\{ \vec{v},\vec{w},\vec{v}\times \vec{w} \}$
>
> > Answer
> > 1. Yes, linearly independent (since $\vec{v},\vec{w}$ are non-zero)
> > 2. No, third vector is a linear combination of the other. 
> > 3. Yes, $\vec{v}\times \vec{w}$ provides a vector orthogonal to $\vec{v},\vec{w}$, meaning it is linearly independent. 

> Question 4: 
> If two matrices $5\times2$ 