---
updated_at: 2026-11-24T18:00:43.258-05:00
edited_seconds: 290
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 20
Lecture Date: 2026-11-24
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[19,20 — Boundary Value Problems]] 
Next: Final Unit! No more note sets from here! 

> [!caution] Note
> This is an extended noteset for this topic. 
> This also continued from content in the previous lecture. 

--- 
# Lecture Notes (20) 
## Linear Transformations / Linear Maps 
A Linear Transformation is defined as the following: 

> [!theorem] Linear Transformation
> A linear transformation which maps a vector (or a set of vectors) to another set of vectors: 
> $$T: \mathbb{R}^{m} \mapsto \mathbb{R}^{n}$$

A linear transformation has to satisfy the following: 
1. Addition is preserved: $$T(\vec{u}+\vec{v}) = T(\vec{u}) + T(\vec{v})$$
2. Scalar Multiplication is Preserved:$$T(k\vec{u}) = kT(\vec{u})$$
3. A zero vector remains a zero vector (origin is preserved):    $$T(\vec{0}) = \vec{0}$$
For instance, take the following examples: 

### Examples
For instance, take the following linear transformation: 
$$
\begin{align}
T: \mathbb{R}^{2} \mapsto \mathbb{R}^{2} \\
\end{align}
$$
Where $T$ represents rotating a vector by $90\degree$ in the counter clockwise direction. This is a linear transformation. Consider now the following linear transformation: 
$$
T: \mathbb{R}^{2} \mapsto \mathbb{R}^{2}, \begin{bmatrix}
x_{1}\\x_{2}
\end{bmatrix} \mapsto \begin{bmatrix}
x_{1} + x_{2} + 5\\2x_{2}
\end{bmatrix}
$$
Note that in this context, the $0$ vector is not preserved. 

Consider now the following linear transformation: 
$$
\begin{align}
T: \mathbb{R}^{n} \mapsto \mathbb{R}^{n}: \vec{x} \mapsto A\vec{x}
\end{align}
$$
Where this is some $nm$ matrix. Checking this: 

$$
\begin{align}
T(\vec{u}+\vec{v})  & = A(\vec{u} + \vec{v}) = A\vec{u} + A\vec{v} = T(\vec{u}) + T(\vec{v}) \tag{matrix distribution} \\
T(k\vec{u}) & = A(k\vec{u}) = kA(\vec{u}) = kT(\vec{u}) \\
T(\vec{0})  & = A \vec{0} = \vec{0}
\end{align}
$$
## Inverse Matricese
Thus, with all these parameters, then this shows that multiplying a vector by a matrix is actually a linear transformation in disguise: 

> [!ila] Important Idea
> Given some linear transformation, where: 
> $$T(\vec{u}) \mapsto \vec{w} = T\vec{u}$$
> We let the matrix $A$ be the standard matrix of $T$, then: 
> $$T(\vec{u}) \mapsto A\vec{u} = T\vec{u} = \vec{w}$$

The question then arises, can we have some $T^{-1}=Q$? Some inverse transformation, and thus some inverse of $A$, where this returns us back to $\vec{U}$? We need the following requirement: 

> [!theorem] Invertibility
> A linear transformation $R:\mathbb{R}^{n} \mapsto \mathbb{R}^{n}$ is invertible if there exists some linear transformation $Q$ such that: 
> $$Q(T(\vec{u})) = \vec{u} = T(Q(\vec{u}))$$
> If some $Q$ exists, then we note that $Q$ is the inverse of $T$, and $T$ is a inversible matrix, defined by the following notation: 
> $$Q = T^{-1}$$

Note that we also have the additional requirement for a linear transformation to be invertible; it must be: 
1. Injective: 
   If, for some vector $T(\vec{u}) \mapsto \vec{v}$, and for some $T(\vec{w}) \mapsto \vec{v}$, then $\vec{u}=\vec{w}$. In other words, if two vectors map to the same vector, then they must be the same vector. 
   
   Recall that we pragmatically already saw this in [[11 — A-CR Matrix Factorization]], such as $A\vec{x}=\vec{b}$, where solutions are unique if and only if $T(\vec{x})$ is injective 
2. Surjective: 
   For some linear transformation $T$, $T$ reaches all vectors in the target space, that is:$$\text{surjective}\iff T(\vec{a}):\mathbb{R}^{n} \mapsto \mathbb{R}^{n}$$
   Then this implies that this linear transformation reaches **all** of $\mathbb{R}^{n}$. Or, in the converse, a function is not surjective if it does not reach all of $\mathbb{R}^{n}$. 
   In terms of a geometric interpretation, then for some $A\vec{x}=\vec{b}$, the column space of $A$ with respects to the dimension $\mathbb{R}^{n}$ of $\vec{x}$, then the column space of $A$ does not reach all of $\mathbb{R}^{n}$. 