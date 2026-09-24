---
updated_at: 2026-09-24T11:13:41.585-04:00
edited_seconds: 470
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
> Expand $\sin^2\theta \to 1-\cos^2\theta$: $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2(1-\cos^2\theta)$$
> Distribute: $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2-||\vec{u}||^2||\vec{v}||^2\cos^2\theta)$$
> Note that $||\vec{u}||^2||\vec{v}||^2\cos^2\theta = (\vec{u}\cdot \vec{v})^2$, ergo: $$||\vec{u}\times \vec{v}||^2 = ||\vec{u}||^2||\vec{v}||^2-(\vec{u}\cdot \vec{v})^2$$
> Which is the statement we wanted to prove earlier. 

> Question 9
> > True or false? If $\vec{u}$ is orthogonal to $\vec{v}+\vec{w}$, then $\vec{u}$ is orthogonal to both $\vec{v}$ and $\vec{w}$. Justify your answer with a proof, or a counter example (for false). 
> 
> Note that this statement equates to the following: $$\vec{u}\cdot(\vec{v}+\vec{w})=0\implies \vec{u}\cdot \vec{v} =0, \vec{u}\cdot \vec{w}=0$$
> Take the case when $\vec{w} = -\vec{v}$, then $\vec{v} -\vec{v} = \vec{0}$, thus: 
> $$\vec{u}\cdot \vec{0} = 0 \tag{by definition}$$
> By this, $\vec{u}$ would by definition be proportional to some $\vec{v}+\vec{w}$, Let's take a further case where we let $\vec{u}=\begin{bmatrix}1\\1\end{bmatrix}$ and $\vec{v}=\begin{bmatrix}0\\1\end{bmatrix}$, then: 
> $$\vec{u}\cdot \vec{v} = 1*0 + 1* 1 = 1$$
> $$\vec{u} \cdot \vec{w} = \vec{u}\cdot-\vec{v} = -(\vec{u}\cdot \vec{v}) \to -1 $$
> Hence, $\vec{u}$ can be proportional with some $(\vec{v}+\vec{w})$, but it isn't inherently orthogonal to it's component vectors.
> > Note an alternate solution exists; expand our original dot product: 
> > $$\vec{u} \cdot(\vec{v} + \vec{w}) = 0 \to \vec{u}\cdot \vec{v} + \vec{u}\cdot \vec{w} = 0 \implies \vec{u}\cdot \vec{v} = -\vec{u}\cdot \vec{w}$$
> > This implies that for our term to be perpendicular, both $\vec{u}\cdot \vec{v}$ and $\vec{u}\cdot \vec{w}$ have to do is either be *equal to 0 (i.e. perpendicular)*, or *equal and opposite in sign*. 
> > 

> Question 10
> > True or false? If $\vec{u}$ and $\vec{v}$ are non-zero vectors such that $$||\vec{u}+\vec{v}||^2 = ||\vec{u}||^2 + ||\vec{v}||^2$$then $\vec{u}$ and $\vec{v}$ are orthogonal.
> 
> To prove this, we can expand our magnitudes into dot products: 
> $$(\vec{u}+\vec{v})\cdot(\vec{u}+\vec{v}) = \vec{u}\cdot \vec{u} + \vec{v}\cdot \vec{v}$$
> Distribute the terms on the left side (from [[02 —Vector Dot Product#Properties|Dot Product Properties]]): 
> $$\vec{u}\cdot \vec{u} + 2\vec{u}\cdot \vec{v} + \vec{v}\cdot \vec{v}= \vec{u}\cdot \vec{u} + \vec{v}\cdot \vec{v}$$
> Remove the terms present on both sides, then: 
> $$2\vec{u}\cdot \vec{v}=0 \implies \vec{u}\cdot \vec{v}=0$$
> This means that $\vec{u}$ and $\vec{v}$ are orthogonal to each other by definition. 

> Question 11: 
> > True or False? If $\vec{u}$ and $\vec{v}$ are non-zero vectors, then $||\vec{u}+\vec{v}|| = ||\vec{u}|| + ||\vec{v}||$ if and only if $\vec{u}$ and $\vec{v}$ are parallel vectors. 
> 
> Square both sides of the equation: 
> $$||\vec{u}+\vec{v}||^2 = (||\vec{u}|| + ||\vec{v}||)^2$$
> $$||\vec{u}+\vec{v}||^2 = ||\vec{u}||^2 + 2||\vec{u}||||\vec{v}|| + ||\vec{v}||^2$$
> Convert our terms of $||\vec{u}+\vec{v}||^2, ||\vec{u}||^2, ||\vec{v}||^2$ into their corresponding dot product versions: 
> $$\vec{u}\cdot \vec{u} + 2\vec{u}\cdot \vec{v} + \vec{v}\cdot \vec{v} = \vec{u}\cdot \vec{u} + 2||\vec{u}||||\vec{v}|| + \vec{v}\cdot \vec{v}$$
> Cancel out terms present on both sides and divide by 2: 
> $$\vec{u}\cdot \vec{v} = ||\vec{u}||||\vec{v}||$$
> Recall that $\vec{u}\cdot \vec{v} = ||\vec{u}||||\vec{v}||\cos\theta$; then: 
> $$||\vec{u}||||\vec{v}||\cos\theta = ||\vec{u}||||\vec{v}||$$
> Cancel out magnitudes: 
> $$\cos\theta = 1 \implies \theta=0\degree$$
> Since $\theta=0$, this implies that $\vec{u},\vec{v}$ are parallel to each other. Note that since $\cos\theta >0$, this only applies within the range of $0<\theta< \frac{\pi}{2}$, that is in the positive quadrant of $\cos\theta$. Taking the case in which $\vec{u}=-\vec{v}$, then we get in the case of $||\vec{0}|| = 2||\vec{u}||$, which will never hold true for our conditions, thus this only holds 