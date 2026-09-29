---
updated_at: 2026-09-29T17:13:03.702-04:00
edited_seconds: 300
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 8
Lecture Date: 2026-09-28
Week: 4
---
Hub: [[ESC103 Hub]]
Previous: [[06 — Solving Linear Equations, Intro to Matrices]]
Next: [[8 — Basic Linear Algebra Concepts]]

--- 
# Lecture Notes
# Pre-Lecture Notes
## Matrix-Vector Products
Recall what we previously defined as a means to solve a linear system, that being that it is the corresponding set of solutions to the following system: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix} = \begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}
$$
This is in principle the operation of performing a Matrix-Vector multiplication, which can be defined in two ways: 
### Ax=B
This method is essentially what formed [[06 — Solving Linear Equations, Intro to Matrices#AX=B Matrix|Ax=B Matrices (ESC103-6)]] in the previous note, that is: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix} = 
\begin{bmatrix}
\vec{r_{1}}^T \cdot x \\
\vec{r_{2}}^T \cdot x \\
\vdots \\
\vec{r_{m}}^T \cdot x
\end{bmatrix}=\begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}
$$
### Linear Combination
Or, this can also be shown as the following (essentially [[06 — Solving Linear Equations, Intro to Matrices#Backing Logic|Backing Logic (ESC103-6)]]): 
$$
\begin{align}
&=\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix}  =\begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}\\
&= \begin{bmatrix}a_{11} \\a_{21} \\\vdots \\a_{m{1}}\end{bmatrix}x_{1} +\begin{bmatrix}a_{12} \\a_{22} \\\vdots \\a_{m2}\end{bmatrix}x_{2}  + \dots+  \begin{bmatrix}a_{1n} \\a_{2n} \\\vdots \\a_{mn}\end{bmatrix}x_{n} = \begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}
\end{align}
$$
That is, it can be said that the above Matrix-Vector multiplication is equivalent to the linear combination of the $n$ column vectors of $\mathbf{A}$ with the coefficients being the members of $\vec{x}$, with it being mapped to some $\vec{b}$. 