---
updated_at: 2026-09-11T16:11:58.517-04:00
edited_seconds: 350
course: ESC103H1
tags:
  - ESC103H1
  - TBF
"Lecture #": 2
Date: 2026-09-10
Week: 2
---
Previous: [[Vector Review]]
Next: N/A 

--- 

## Dot Product
The Dot Product of two vectors is defined as the following equation below. Let $\vec{a}$ and $\vec{b}$ be vectors; their dot product is defined as: 
$$\vec{a}\cdot \vec{b} = ||\vec{a}||*||\vec{b}||\cos(\theta)$$
Where $\theta$ is the angle between the vectors. The Dot Product is generally used as a concept to measure how much these two vectors are roughly pointing in the same direction. If two vectors are orthogonal to each other, the Dot Product resolves to zero. 

Algebraically; the Dot Product is defined as the respective sum of their components. Take two $n$-dimensional vectors: 
$$
\vec{a} = \begin{pmatrix}
a_{1}&a_{2}&a_{3}&\dots&a_{n}
\end{pmatrix}
$$
$$
\vec{b}=\begin{pmatrix}
b_{1}&b_{2}&b_{3}&\dots&b_{n}
\end{pmatrix}
$$
$$
\vec{a}\cdot \vec{b} = \sum^n_{i=1}a_{i}b_{i}
$$
Note that if $\vec{a} = \vec{b}$; this simplifies to $\vec{a}\cdot \vec{a}=||\vec{a}||^2$. 
## Triangle Inequality 
The Triangle Inequality is a useful identity that arises out of the way Vector addition operates. Given two vectors $\vec{a}$ and $\vec{b}$; $\vec{a} + \vec{b}$ effectively creates the third side of a triangle. 

> [!abstract] Triangle Inequality Theorem
> Let $a$, $b$ and $c$ denote the side lengths of the 3 distinct sides of a triangle. The sum of two sides of the triangle will always be greater than or equal to the last remaining side.
> Can be mathematically expressed as: 
> $$a + b \geq c$$

For the case of our vectors; we can adapt this to instead take the vectors present. Note that $\vec{c} = \vec{a} + \vec{b}$; ergo:
> [!abstract] Triangle Inequality Theorem
> Let $\vec{a}$ and $\vec{b}$ denote two vectors; whose sum is $\vec{a} + \vec{b} = \vec{c}$. Ergo: 
> $$||\vec{a}|| + ||\vec{b}|| \geq ||\vec{a} + \vec{b}||$$

A proof of this is available on [[02 — The Real Number System#Triangle Inequality Theorem| The Calculus Page that Proves it ]]