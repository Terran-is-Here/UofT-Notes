---
updated_at: 2026-10-19T22:13:22.865-04:00
edited_seconds: 260
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 12
Lecture Date: 2026-10-19
Week: 7
Created: October 13th 2026, 5:17:25 pm
---
Hub: [[ESC103 Hub]]
Previous: [[11 — A-CR Matrix Factorization]]
Next:

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Elementary Row Operations
Elementary Row Operations can be generally defined as one of the three following operations: 
1. Exchanging any two rows. 
2. Scalar Multiplication: Multiplying a row by a scalar.
3. Row Sum: Adding a multiple of one row to another row. 
Note that we did this partially in terms of our $\mathbf{A=CR}$ factorization in terms of $\mathbf{R}$, although it is not exactly the same. To begin with, we will formally define the concept of an Identity Matrix: 
### Identity Matrix
Identity Matrices are defined by the term $I$, and are solely defined by the **diagonal entries** being a term of $1$, and the rest being 0: 
$$
I = \begin{bmatrix}1 & 0 \\0 & 1\end{bmatrix} = \begin{bmatrix}1 & 0 & 0 \\0 & 1 & 0 \\0 & 0 & 1\end{bmatrix} = \begin{bmatrix}
1 & 0 & 0 & \dots & 0 \\
0& 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \dots & 1
\end{bmatrix}
$$
Note that $I$ follows the concept that for any matrix $A$, $AI=A$. 
### Row Operations
The Identity Matrix forms the basis in which we actually define the matrices of our row operations. 

> Exchanging two rows: $$\begin{bmatrix}1 & 0 & 0 \\0 & 0 & 1 \\0 & 1 & 0\end{bmatrix}$$
> This is the equivalent of changing row 2 and row 3 with eachother, for instance: $$\begin{bmatrix}1 & 0 & 0 \\0 & 0 & 1 \\0 & 1 & 0\end{bmatrix}\begin{bmatrix}a & b & c\\d & e & f\\g & h & i\end{bmatrix} = \begin{bmatrix}a & b & c\\g & h & i\\d & e & f\end{bmatrix}$$

> Scalar Row Multiplication: 
> $$\begin{bmatrix}1 & 0 & 0 \\0 & k & 0 \\0 & 0 & 1\end{bmatrix}$$
> Equivalent to multiplying row $2$ by some constant $k$.

> Row Adding Operation
> $$\begin{bmatrix}1 & 0 & 0 \\0 & 1 & 0 \\0 & k & 1\end{bmatrix}$$
> Adds $k$ row 2s to row 3. 