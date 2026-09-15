---
updated_at: 2026-09-15T17:15:16.021-04:00
edited_seconds: 270
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 4
Lecture Date: 2026-09-14
Week: 2
created:
Created: September 14th 2026, 9:16:00 pm
---
Hub: [[ESC103 Hub]]
Previous: [[03 — Vector Projection]]
Next: N/A

--- 

# Lecture Notes
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
-(a_{1}b_{3} - b_{3}b_{1}) \\
a_{1}b_{2} - a_{2}b_{1}
\end{bmatrix}
$$
(You can simply the determinants inside into the equations on the right.)
## Geometric Interpretation
An alternate mean for defining *a* cross product is: 
$$
||\vec{a}\times \vec{b}|| = ||\vec{a}||*||\vec{b}||\sin\theta
$$
or, conversely: 
$$
\vec{a} \times \vec{b} = ||\vec{b}|| * ||\vec{a}||
$$
Where $\theta$ is the angle between $\vec{a}$ and $\vec{b}$. A result of a cross-oprodu