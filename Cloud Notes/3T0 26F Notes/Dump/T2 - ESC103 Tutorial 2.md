---
updated_at: 2026-09-24T10:53:24.069-04:00
edited_seconds: 230
course: ESC103H1
tags:
  - Tutorial
  - ESC103H1
"Tutorial #": 2
Lecture Date: 2026-09-22
Week: 3
---
Hub: [[ESC103 Hub]]
Connected Notes: [[04 — Vector Cross Product]], [[05 — Equations of Lines and Planes]]
```query
tag:#ESC103H1 [week:3]
```

--- 
This note will have the questions and / answers from Tutorial 2 of ESC103. 

# Questions
1. idk
2. idk
3. idk
4. idk
5. idk
6. Using projections, show that the sum of the squares of the distances from a point $P=(x_{1},y_{1})$ to the perpendicular vectors $ax+by=0$ and $bx-ay=0$ is equal to the square of the length of the vector $\vec{OP} = \begin{bmatrix}x_{1}\\y_{1}\end{bmatrix}$. 
7. Prove that if $\vec{u}$ and $\vec{v}$ are vectors in $\mathbb{R}^3$, then $\vec{u}\cdot(\vec{u}\times \vec{v}) = 0$.
8. Prove the Lagrange Identity, that is if $\vec{u}$ and $\vec{v}$ are in $\mathbb{R}^3$, then $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2 - (\vec{u}\cdot \vec{v})^2$$
9. True or false? If $\vec{u}$ is orthogonal to $\vec{v}+\vec{w}$, then $\vec{u}$ is orthogonal to both $\vec{v}$ and $\vec{w}$. Justify your answer with a proof, or a counter example (for false). 
10. True or false? If $\vec{u}$ and $\vec{v}$ are non-zero vectors such that $$||\vec{u}+\vec{v}||^2 = ||\vec{u}||^2 + ||\vec{v}||^2$$then $\vec{u}$ and $\vec{v}$ are orthogonal.
11. True or False? If $\vec{u}$ and $\vec{v}$ are non-zero vectors, then $||\vec{u}+\vec{v}|| = ||\vec{u}|| + ||\vec{v}||$ if and only if $\vec{u}$ and $\vec{v}$ are parallel vectors. 


# Answers

> Question 7
> > Given $\vec{u},\vec{v}\in \mathbb{R}^3$, then $\vec{u}\cdot(\vec{u}\times \vec{v})=0$. Prove this statement. 
> 
> Note that by definition, $\vec{u}\cdot \vec{v}=\vec{r}$ where $\vec{r}\cdot \vec{u} = 0$ and $\vec{r}\cdot \vec{v}$ = 0, ergo with this, then this holds true. 

> Question 8 
> > Prove the Lagrange Identity, that is if $\vec{u},\vec{v}\in \mathbb{R}^3$, then the following is true: 
> > $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2 - (\vec{u}\cdot \vec{v})^2$$
> 
> Start from the definition of a cross product's magnitude: 
> $$||\vec{u}\times \vec{v}|| = ||\vec{u}||||\vec{v}||\sin\theta$$
> Square on both sides: $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2\sin^2\theta$$
> Expand $\sin^2\theta \to 1$