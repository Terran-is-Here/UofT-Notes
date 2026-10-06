---
updated_at: 2026-10-06T16:33:45.228-04:00
edited_seconds: 590
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
For the purposes of this note, let us define two matrices $\mathbf{A}$ and $\mathbf{B}$ with dimensions $m\times n$ and $n\times p$ (Note, these dimensions matter, since the definition of Matrix Multiplication relies on relating the Row and column matrices of $\mathbf{A}$ and $\mathbf{B}$ respectively. Then $\mathbf{C}$ will have the resultant dimensions of $m\times p$. 
> That is, the number of columns in $\mathbf{A}$ must be equal to the number of the number of rows in $\mathbf{B}$. 
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
\vec{r_{a 1}} \cdot \vec{c_{b 1}}  & \vec{r_{a 1}} \cdot \vec{c_{b 2}} & \dots & \vec{r_{a 1}} \cdot \vec{c_{b n}} \\
\vec{r_{a 2}} \cdot \vec{c_{b 1}}  & \vec{r_{a 2}} \cdot \vec{c_{b 2}} & \dots & \vec{r_{a 2}} \cdot \vec{c_{b n}} \\
\vdots & \vdots & \ddots & \vdots \\
\vec{r_{a n}} \cdot \vec{c_{b 1}}  & \vec{r_{a 1}} \cdot \vec{c_{b 2}} & \dots & \vec{r_{a 1}} \cdot \vec{c_{b n}}
\end{bmatrix}}
$$
Note that we can rewrite this; since for the first column of $\mathbf{C}$, note how $\vec{c_{b1}}$ is always present. Also note that the column vector of: 
$$
\begin{bmatrix}\vec{r_{a 1}} \\\vec{r_{a 2}}  \\\vdots \\\vec{r_{a n}} \\\end{bmatrix} = \mathbf{A} = \begin{bmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1}  & a_{m2} & \dots & a_{mn}
\end{bmatrix}
$$
Which means $\mathbf{C}$ can be instead be written as the following: 
$$
\mathbf{C} = \begin{bmatrix}
\mathbf{A}*\begin{bmatrix}b_{11} \\b_{21} \\\vdots \\b_{n1}\end{bmatrix} & \mathbf{A}*\begin{bmatrix}b_{12} \\b_{22} \\\vdots \\b_{n_{2}}\end{bmatrix} & \dots & \mathbf{A}*\begin{bmatrix}b_{1p} \\b_{2p} \\\vdots \\b_{np}\end{bmatrix}
\end{bmatrix}
$$
Recall from [[06 — Solving Linear Equations, Intro to Matrices#AX=B Matrix|ESC103 (8) — AX=B]] matrices that some $A\vec{x}=\vec{b}$, where $\vec{b}$ is a column vector with the same number of $m$ rows as $\vec{x}$. 
## Example
Take the following set of matrices: 
$$
\mathbf{A} = \begin{bmatrix}0 & 1 \\2 & 2 \\3 & 3 \\4 & 4\end{bmatrix}, \mathbf{B} = \begin{bmatrix}
10 & 10 & 20 & 20 \\
5 & 5 & 10 & 10
\end{bmatrix}
$$
Then $\mathbf{C}$ is expressed as: 
$$
\mathbf{C} = \begin{bmatrix}
5 & 5 & 10 & 10 \\
30 & 30 & 60 & 60 \\
45 & 45 & 90 & 90 \\
60 & 60 & 120 & 120
\end{bmatrix}
$$
