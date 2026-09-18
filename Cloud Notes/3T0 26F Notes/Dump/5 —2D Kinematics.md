---
updated_at: 2026-09-17T22:05:19.919-04:00
edited_seconds: 220
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 5
Lecture Date: 2026-09-14
Week: 2
created:
Created: September 14th 2026, 5:22:05 pm
---
Hub: [[PHY180 Hub]]
Previous: [[4 — 1D Kinematics]]
Next: [[6 — Rotational Kinematics]]

> [!quote] Textbook Reading: 
> 4.1-4.3 
--- 

# Lecture Notes
# Pre-Lecture Notes

### 2D Extension
One of the core principles which allow us to analyze multi-dimension kinematics (not just $\mathbb{R}^2$, but $\mathbb{R}^n$) is the concept that dimensions within kinematics problems are linearly independent of each-other: that is $x$ and $y$ dimensions have their own movement / kinematics. 

This means that in general, we can break up any $n$-dimensional kinematics problem into an analysis of $n$ $1$-dimensional kinematics problems. Note that depending on the context, what we can learn in one axis may help us analyze another. 
#### Projectile Motion
Projectile Motion is generally defined as a 2d kinematics equation, where our $y$ axis is defined as a free-fall problem (i.e. $a_{y}=g$), and our $x$-axis (unless otherwise stated) has no acceleration. 

This means that kinematics equations for our $x$-dimension are simplified, since $v=v_{0}$. 

Our $y$-dimension does provide us with some interesting context: 
* When $\Delta y=0$, whatever object we have projectile motion on has hit the ground. 
* When $v_{y}=0$, our object is at it's "apex" (i.e. turn around window).
	* The time at this moment gives us time of max height, which can be used to solve for actual max height. 

Analysis of these one-dimensional fragments is trivial, as these can be done independently.

For instance, let us take: $\vec{v_{0}} \in \mathbb{R}^2$, then: 
$$
\vec{v_{0}} = \begin{bmatrix}
\cos\theta *|\vec{v}|  \\
\sin\theta * |\vec{v}|
\end{bmatrix}
$$
That is, $\vec{v_{0x}} = |\vec{v}|\cos\theta$ and $\vec{v_{0y}}=$