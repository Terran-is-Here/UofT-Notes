---
updated_at: 2026-11-01T16:09:28.577-05:00
edited_seconds: 240
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-01
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[13 — Ax=0 Via EROs]]
Next: N/A

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Gaussian Elimination
Gaussian Elimination is a simplified means of how we performed the actions we took in the previous note to get a matrix in a form $U$ or $R_{0}$, that is in Row-Echelon form and Row-Reduced Echelon Form, which will now be fully defined below. 

A Matrix $A$ is said to be in REF (Row-Echelon Form) if: 
1. Any and all zero rows are located at the bottom. 
2. All leading non-zero terms are to the right of all the leading terms in the row above it. 
A matrix $A$ is said to be in RREF (Row-Reduced Echelon Form) if it is in REF and: 
3. All leading terms are equal to one. 
4. All entries in the column containing a leading 1 are zero. 

In terms of Gaussian Elimination, we rewrite a matrix-vector multiplication into a form we term as an Augmented Matrix; that is given $A\vec{x}=\vec{b}$, the augmented matrix is written as $[A|\vec{b}]$. For instance, take the following matrix: 
$$
\begin{bmatrix}
1 & 3 & 5 \\
2 & 3 & 7 \\
1 & 3 & 5
\end{bmatrix}
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix}=
\begin{bmatrix}
1\\-1\\1
\end{bmatrix}
$$
In an augmented matrix, this is expressed as: 
$$
\left[\begin{array}{ccc|c}
1 & 3 & 5 & 1 \\
2 & 3 & 7 & -1 \\
1 & 3 & 5 & 1
\end{array}\right]
$$
Since we perform the same $E_{u}$ / EROs to both sides of a Matrix-Vector Multiplication (see our previous notes), then we can simply perform them on this augmented matrix on both sides. If we wanted to get this into REF, then: 
$$
\begin{align}
 & \to \left[\begin{array}{ccc|c}
1 & 3 & 5 & 1 \\
2 & 3 & 7 & -1 \\
1 & 3 & 5 & 1 
\end{array} \right]  & \text{Retaking the original...}\\
 & \to \left[\begin{array}{ccc|c}
 1 & 3 & 5 & 1 \\
 2 & 3 & 7 & -1 \\
 0 & 0 & 0 & 0 
 \end{array} \right]  & r_{3}:r_{3}-r_{1}\\
 & \to \left[\begin{array}{ccc|c}
  1 & 3 & 5 & 1 \\
  0 & -3 & -3 & -3 \\
  0 & 0 & 0 & 0
 \end{array} \right]  & r_{2}:r_{2}-2r_{1}\\
  & \to \left[\begin{array}{ccc|c}
   1 & 3 & 5 & 1 \\
   0 & 1 & 1 & 1 \\
   0 & 0 & 0 & 0
  \end{array} \right]  & r_{2}:-\frac{1}{3}r_{2}\\
   & \to \left[\begin{array}{ccc|c}
    1 & 0 & 2 & -2 \\
	0 & 1 & 1 & 1 \\
	0 & 0 & 0 & 0
   \end{array} \right] & r_{1}:r_{1}-3r_{2}
\end{align}
$$
From here, the following system of equations arise: 
$$
\begin{align}
1x_{1} + 2x_{3} &  = -2 \\
1x_{2} + 1x_{3}
\end{align}
$$

