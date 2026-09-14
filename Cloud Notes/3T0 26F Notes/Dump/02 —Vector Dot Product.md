---
updated_at: 2026-09-14T12:48:13.128-04:00
edited_seconds: 530
course: ESC103H1
tags:
  - ESC103H1
  - TBF
"Lecture #": 2
Date: 2026-09-10
Week: 2
---
Hub: [[ESC103 Hub]]
Previous: [[01 — Vector Review]]
Next: [[03 — Vector Projection]]

--- 
# Lecture Notes
A good amount of the notes within these sections / this lecture (at least for the first half) have been covered within the previous note as is. 
## Vector Definition
Note that we don't really define the *starting points* of vectors. A vector with the same magnitude and angle are identical regardless of location; however we do have specific terms for these: 
* A vector $\vec{v}$ at the origin is in the *standard position*. 
# Pre-Lecture Notes

## Dot Product / Scalar Product
The Dot Product of two vectors is defined as the following equation below. Let $\vec{a}$ and $\vec{b}$ be vectors; their dot product is defined as: 
$$\vec{a}\cdot \vec{b} = ||\vec{a}||*||\vec{b}||\cos(\theta)$$
Where $\theta$ is the angle between the vectors. The Dot Product is generally used as a concept to measure how much these two vectors are roughly pointing in the same direction. If two vectors are orthogonal to each other, the Dot Product resolves to zero. 

Algebraically; the Dot Product is defined as the respective sum of their components. Take two $n$-dimensional vectors: 
$$
\vec{a} = \begin{bmatrix}
a_{1}&a_{2}&a_{3}&\dots&a_{n}
\end{bmatrix}
$$
$$
\vec{b}=\begin{bmatrix}
b_{1}&b_{2}&b_{3}&\dots&b_{n}
\end{bmatrix}
$$
$$
\vec{a}\cdot \vec{b} = \sum^n_{i=1}a_{i}b_{i}
$$
Note that if $\vec{a} = \vec{b}$; this simplifies to $\vec{a}\cdot \vec{a}=||\vec{a}||^2$. 
### Properties
The Dot Product operation is: 
* Distributive:
	* ($\vec{a} \cdot(\vec{b} + \vec{c}) = \vec{a}\cdot \vec{b} + \vec{a} \cdot \vec{c}$)
* Commutative:
	* $\vec{a}\cdot \vec{b} =\vec{b}\cdot \vec{a}$
* Associative w/Scalars: 
	* $c(\vec{a}+\vec{b}) = c\vec{a} \cdot \vec{b} = c\vec{b}\cdot \vec{a} \neq c\vec{b}\cdot c\vec{w}$
	* Scalars do not fully distribute; they only distribute to one pair. 

## Geometric Interpretation

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

A proof of this is available on [[02 — The Real Number System#Triangle Inequality Theorem| The Calculus Page that Proves it]]. 