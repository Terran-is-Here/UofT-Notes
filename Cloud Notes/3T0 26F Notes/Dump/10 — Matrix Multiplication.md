---
updated_at: 2026-10-06T15:32:13.833-04:00
edited_seconds: 290
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 10
Lecture Date: 2026-10-06
Week: 5
---
Hub: [[ESC103 Hub]]
Previous: [[09— Basic Linear Algebra Concepts]]
Next:
> [!quote] Learning Objectives
> * Perform matrix multiplication $\mathbf{AB}$ using the linear combination of the columns of matrix $\mathbf{A}$.
> * Perform matrix multiplication $\mathbf{AB}$ using the dot products of rows of matrix $\mathbf{A}$ with the columns of matrix $\mathbf{B}$
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Matrix Multiplication
For the purposes of this note, let us define two matrices $\mathbf{A}$ and $\mathbf{B}$ with dimensions $m\times n$ and $n\times p$ (Note, these dimensions matter, since the definition of Matrix Multiplication relies on relating the Row 
$$
\mathbf{A} = \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1}  & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$
$$
\mathbf{B} = \begin{bmatrix}
b_{11} & b_{12} & \dots & b_{1p} \\
b_{21} & b_{22} & \dots & b_{2p} \\
\vdots & \vdots & \ddots & \vdots \\
b_{n1}  & b_{n2} & \dots & b_{np}
\end{bmatrix}
$$
$$
\mathbf{AB}=\mathbf{C}
$$
The $ij$'th entry of $\mathbf{C}$ (element in row $i$, column $j$) is the *dot product* of the $i$-th row vector in $\mathbf{A}$, and the $j$-th column vector in $\mathbf{B}$: 
$$
C_{ij} = \sum^n_{k=1}a_{ik}b_{kj} = a_{i1} b_{1j} + a_{i2}b_{2j} + \dots a_{in}b_{nj}
$$
Then, let's introduce the notation of: $r_{an}$ as the $n$-th row vector of $\mathbf{A}$, and $c_{bn}$ as the $n$-th column vector of $\mathbf{B}$; then: 
$$
\mathbf{C=\begin{bmatrix}

\end{bmatrix}}
$$