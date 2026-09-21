---
updated_at: 2026-09-21T12:34:32.976-04:00
edited_seconds: 660
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 4
Lecture Date: 2026-09-21
Week: -13
created:
Created: September 14th 2026, 9:16:00 pm
---
Hub: [[ESC103 Hub]]
Previous: [[03 — Vector Projection]]
Next: [[05 — Equations of Lines and Planes]]

--- 

# Lecture Notes
## Definition
We generally define the cross product from following: 
$$
\vec{i} \times \vec{j} = \vec{k} \text{ and } \vec{j}\times \vec{i} = -\vec{k}
$$
$$
\vec{j}\times \vec{k} = \vec{i} \text{ and } \vec{k} \times \vec{j} = \vec{i}
$$
$$
\vec{k} \times \vec{i} = \vec{j} \text{ and } \vec{i}\times \vec{k} = -\vec{j}
$$
Where $\vec{k}$ is perpendicular to both $\vec{i}$ and $\vec{j}$, that is these are unit vectors, the cross products of $\vec{i},\vec{j},\vec{k}$ result in one of the other unit vectors parallel to them; note that : 
$$
\vec{j} \times \vec{i} = -\vec{k}
$$
Therefore, we can derive the general equation, take the following: 
$$
\vec{a} \times \vec{b} = (
a_{1}\vec{i} + a_{2}\vec{j} + a_{3}\vec{k} ) \times (b_{1}\vec{i} + b_{2}\vec{j} + b_{3}\vec{k})
$$
From our properties above: 
$$
= a_{1}b_{2}\vec{k}- a_{1}b_{3}\vec{j}  + -a_{2}b_{1}\vec{k} + a_{2}b_{3}\vec{i}  + a_{3}b_{1}\vec{j} -a_{3}b_{2}\vec{i}
$$
$$
=(a_{1}b_{2}-a_{2}b_{1})\vec{k} + (-a_{1}b_{3} + a_{3}b_{1}) \vec{j} + (a_{2}b_{3} - a_{3}b_{2})\vec{i}
$$
Therefore: 
$$
\vec{a}\times \vec{b} = \begin{bmatrix}
a_{2}b_{3} - a_{3}b_{2} \\
-(a_{1}b_{3} - a_{3}b_{1}) \\
a_{2}b_{3} - a_{3}b_{2} \\
\end{bmatrix}
$$
### Properties
$$
\vec{a}\times(\vec{b}+\vec{c}) = \vec{a}\times \vec{b} + \vec{a}\times \vec{c} \tag{Distributive Property}
$$
$$
\vec{a} \times \vec{b} = -\vec{a}\times \vec{b} \tag{Anticommunicative Property}
$$
$$
c(\vec{a}\times \vec{b}) = c\vec{a}\times \vec{b} = \vec{a}\times x\vec{b} \tag{Given c is a scalar}
$$

### Lagrange Identity
Given two vectors $\vec{a}$ and $\vec{b}$ with an angle $\theta$ between them; we can define the following: 
$$
||\vec{a}\times \vec{b}||^2 = ||\vec{a}||^2||\vec{b}||^2 - (\vec{a}\cdot \vec{b}_{})^2
$$
## Geometric Definition
Recall our definition of a dot product, sub it into our above expression: 
$$
||\vec{a}\times \vec{b}||^2 = ||\vec{a}||^2||\vec{b}||^2 - (||\vec{a}||*||\vec{b}|| \cos\theta)^2
$$
$$
||\vec{a}\times \vec{b}||^2 = ||\vec{a}||^2||\vec{b}||^2 - ||\vec{a}||^2*||\vec{b}||^2 \cos^2\theta
$$
$$
||\vec{a}\times \vec{b}|^2 = ||\vec{a}||^2 ||\vec{b}||^2\left[1-\cos^2\theta\right]
$$
$$
||\vec{a}\times \vec{b}|^2 = ||\vec{a}||^2 ||\vec{b}||^2\sin^2\theta
$$
Taking the square root, then: 
$$
||\vec{a}\times \vec{b}|| = ||\vec{a}||*||\vec{b}|| * |\sin\theta|
$$
Note what this geometrically means: If we take $\vec{a}$ and $\vec{b}$ with the angle $\theta$ between them, $||\vec{b}||*\sin\theta$ gives us the height of the parallelogram formed between them, and since $||\vec{a}||$ is the base, then the **Magnitude of a Cross Product** gives us the *area of the parallelogram formed by those two vectors*. 
# Pre-Lecture Notes
## Cross Product
A cross product of two vectors $\vec{a}$ and $\vec{b}$ is generally defined as the following: 
$$
\vec{a} = \begin{bmatrix}
a_{1} \\
a_{2} \\
a_{3}
\end{bmatrix}, \vec{b}=\begin{bmatrix}
b_{1} \\
b_{2} \\
b_{3}
\end{bmatrix}
$$
One of the means to determine the cross product is the following: 
$$\vec{a}^T, \vec{b}^T$$
$$\vec{a}\times \vec{b} = \det\begin{bmatrix}
\hat{i}& \hat{j} & \hat{k}\\
a_{1} & a_{2} & a_{3}\\
b_{1} & b_{2} & b_{3}
\end{bmatrix}$$
Breaking up the matrix via co-factor expansion gives us: 
$$
\vec{a} \times \vec{b} = \hat{i}\det \begin{bmatrix}
a_{2} & a_{3}  \\
b_{2} & b_{3}
\end{bmatrix} - \hat{j}\det\begin{bmatrix}
a_{1} & a_{3} \\
b_{1} & b_{3} \\
\end{bmatrix}
+ \hat{k}
\det\begin{bmatrix}
a_{1} & a_{2} \\
b_{1} & b_{2}
\end{bmatrix}
$$
Or, alternatively: 
$$
\vec{a} \times \vec{b} = \begin{bmatrix}
\det\begin{bmatrix}
a_{2} & a_{3}  \\
b_{2} & b_{3}
\end{bmatrix} \\
-\det\begin{bmatrix}
a_{1} & a_{3} \\
b_{1} & b_{3} \\
\end{bmatrix} \\
\det\begin{bmatrix}
a_{1} & a_{2} \\
b_{1} & b_{2}
\end{bmatrix}
\end{bmatrix} = 
\begin{bmatrix}
a_{2}b_{3} - a_{3}b_{2} \\
-(a_{1}b_{3} - a_{3}b_{1}) \\
a_{1}b_{2} - a_{2}b_{1}
\end{bmatrix}
$$
(You can simply the determinants inside into the equations on the right.)
## Geometric Interpretation
An alternate mean for defining *a* cross product is: 
$$
||\vec{a}\times \vec{b}|| = ||\vec{a}||*||\vec{b}||\sin\theta
$$
or, conversely where $\hat{n}$ is a vector normal to the plane:
$$
\vec{a} \times \vec{b} = ||\vec{b}|| * ||\vec{a}||*\sin\theta * \vec{n}
$$
Where $\theta$ is the angle between $\vec{a}$ and $\vec{b}$. Cross product results are generally defined as being perpendicular to the plane formed by the other two vectors listed. 