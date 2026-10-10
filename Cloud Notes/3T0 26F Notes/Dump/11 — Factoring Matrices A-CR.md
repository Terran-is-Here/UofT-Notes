---
updated_at: 2026-10-10T11:29:39.167-04:00
edited_seconds: 340
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 11
Lecture Date: 2026-10-09
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[10 — Matrix Multiplication]]
Next:
> [!quote] Learning Objectives 
> * Construct a matrix $\mathbf{C}$ from matrix $\mathbf{A}$ using the definition of independent vectors. 
> * Construct a matrix $\mathbf{R}$ such that $\mathbf{A}=\mathbf{CR}$
> * Explain the significance of $\mathbf{R,C}$ with respects of $\mathbf{A}$

> [!quote] Recommended Reading 
> [[08 — Matrix Vector Products]], and [[09— Basic Linear Algebra Concepts]] are also useful for this section as they pop up again and again. 
--- 
 
# Lecture Notes

---
# Pre-Lecture Notes
## CR Matrices 
Given the following matrix: 
$$
\mathbf{A} = \begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix}
$$
A matrix $\mathbf{C}$ can be created from the linearly independent columns of $\mathbf{A}$: 
$$\mathbf{C} = \begin{bmatrix}1 & 4 \\3 & 2 \\0 & 2\end{bmatrix}$$
Note; that $\begin{bmatrix}7\\11\\2\end{bmatrix} = 3\begin{bmatrix}1\\3\\0\end{bmatrix}+ 1\begin{bmatrix}4\\2\\2\end{bmatrix}$, That is to say that this matrix is *linearly* dependent. Then we can express the matrix $\mathbf{R}$ as the following matrix: 
$$
\mathbf{R} = \begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & 1
\end{bmatrix}
$$
Where: 
$$
\begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix} = \begin{bmatrix}1 & 4\\3 & 2\\0 & 2\end{bmatrix}\begin{bmatrix}1 & 0 & 3\\0 & 1 & 1 \end{bmatrix}
$$
Recall that matrix multiplication **always** works in a row-column arrangement. That is; we iterate through rows of $\mathbf{A}$ before iterating through columns of some $\mathbf{B}$ in $\mathbf{AB}$. 
> [!ila] Important Idea
> Note that the Column Vectors of $\mathbf{C}$ are the basis vectors of the column space of $\mathbf{A}$, or in other words; they represent the linearly independent vectors in $\mathbf{A}$ (and thus it's corresponding rank and dimensions).
> 

### Significance of R
Note however that the matrix $\mathbf{R}$ is something special: it is the Row-Reduced Echelon Form of $\mathbf{A}$; though it's kind of outside the bounds of this note for now to work on it. 

