---
updated_at: 2026-09-21T21:33:38.337-04:00
edited_seconds: 440
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 6
Lecture Date: 2026-09-28
Week: 4
created:
Created: September 21st 2026, 9:13:07 pm
---
Hub: [[ESC103 Hub]]
Previous: [[05 — Equations of Lines and Planes]]
Next: N/A 

--- 
# Lecture Notes
# Pre-Lecture Notes
For the purposes of this note, consider the problem where we are trying to solve for a solution for a system of 3 equations with 3 unknowns ($x,y,z)$, that is the intersection points of 3 planes if they exist: 
$$
a_{11}x + a_{12}y + a_{13}z = b_{1}
$$
$$
a_{21} x+a_{22}y+a_{23}z = b_{2}
$$
$$
a_{31}x + a_{32}y + a_{33}z = b_{3}
$$
Or, in augmented matrix form, they can be expressed as: 
$$
\left[\begin{array}{ccc|c}
a_{11} & a_{12} & a_{13} & b_{1} \\
a_{21} & a_{22} &a_{23}&b_{2} \\
a_{31} & a_{32} & a_{33} & b_{3}
\end{array}
\right]
$$
## Row Picture
The row pictures deal with considering our equations above as a series of $3$ planes, and simply solving for the solution of $x,y,z$ that satisfies all the values; where the resultant intersection gives you the point at which all three planes intersect. In other words, we want to return that augmented matrix above us into a row-echelon / row-reduced matrix. 

## Column Picture
The Column Picture of solving for the solution of a system of 3 equations deals with solving for a linear combination that solves for our solution set of $x,y,z$. 

Note that we can define 3 vectors from the equations above based on if they're in terms of $x$, $y$, or $z$: 
$$
\vec{v_{x}} = \begin{bmatrix}a_{11} \\a_{21} \\a_{31}\end{bmatrix},
\vec{v}_{y} = \begin{bmatrix}a_{12} \\a_{22} \\a_{32}\end{bmatrix}, 
\vec{v}_{z} = \begin{bmatrix}a_{13} \\a_{23} \\a_{33}\end{bmatrix}
$$
Our solutions / $b$ values can also be defined by their own vector: 
$$
\vec{b} = \begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix}
$$

Therefore, we can define the following as an alternate means of viewing how to solve our expression above: 
$$
x\vec{v}_{x} + y\vec{v}_{y} + z\vec{v}_{z} = \vec{b}
$$Subbing in our values: 
$$
x\begin{bmatrix}a_{11} \\a_{21} \\a_{31}\end{bmatrix} + y\begin{bmatrix}a_{12} \\a_{22} \\a_{32}\end{bmatrix}+z\begin{bmatrix}a_{13} \\a_{23} \\a_{33}\end{bmatrix} =\begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix}$$
Where our goal now is to solve for a set of solutions of $x,y,z$ to solve for a linear combination of the vectors $\vec{v}_x,\vec{v}_{y}, \vec{v}_{z}$ that equals $\vec{b}$. 
