---
updated_at: 2026-11-02T10:00:37.407-05:00
edited_seconds: 310
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 14
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
1x_{2} + 1x_{3} &  = 1
\end{align}
$$
Letting $x_{3}=t$ (that is, $x_{3}$) is a free variable, then: 
$$
x_{1}=-2-2t\\
x_{2}=1-t
$$
Or: 
$$
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix} = \begin{bmatrix}
-2\\1\\0
\end{bmatrix} + \begin{bmatrix}
-2\\-1\\1
\end{bmatrix}t
$$
In other words, the solution space of this (note since it was equal to zero, this is it's nullity) is equivalent to a line. Or in other words, infinitely many solutions. 
## Implications
* Columns corresponding to leading ones correspond to leading/pivot variables. Other columns represent to free variables.
* Number of leading ones (leading pivot variables) are equivalent to the number of **linearly independent** vectors that span column space; that is the number of leading ones represent $\text{rank}(a)$. 
* If there exists a line where $0=1$, (that is, a row of zeros equalling a non-zero on the corresponding $\vec{b}$), our system is stated to be inconsistent; that is no solutions exist: 
	* This means that either $\vec{b}\not\in$ the column space of $A$ (in terms of the column picture) 
	* The planes in row picture do not ever intersect at **one point**. 