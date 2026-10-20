---
updated_at: 2026-10-20T17:33:57.132-04:00
edited_seconds: 300
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
Recall that previously, to solve $A\vec{x}=\vec{0}$, we previously factored $A\vec{x}$ into $CR\vec{x}$ to solve correspondingly; where $C\vec{x}=0$ holds the solution to $A\vec{x}=0$. 

Recall that from [[10 — Matrix Multiplication]], we can multiply both sides of an equation **by the same matrix, in the same order**; that is $A\vec{x}=\vec{b}$, multiplying by the same matrix $E_{1}$ maintains this equality: $(A\vec{x}=\vec{b}) = (M_{1}A\vec{x}=M_{1}\vec{b})$. Using this property of matrix multiplication, we can solve a system of linear equations through multiplying by certain set of matrices; called Elementary Row Operations. 

## Upper Triangular Matrix
For a square system (i.e. $n\times n$ matrices), an upper triangular matrix is defined as the following: 
$$U=\begin{bmatrix}u_{11} & u_{12} & u_{13} \\0 & u_{22} & u_{23} \\0 & 0 & u_{33}\end{bmatrix}$$
Where all terms to the bottom left of the main diagonal of a matrix are defined as being equal to 0. Note that this form is useful, as in the case where we are solving a $A\vec{x}=\vec{0}$, we can easily solve this into our system of equations: 
$$U\vec{x}=\vec{b}=\begin{bmatrix}u_{11} & u_{12} & u_{13} \\0 & u_{22} & u_{23} \\0 & 0 & u_{33}\end{bmatrix}\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix}=\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}$$
As from here, $x_{3}=u_{33}=b_{3}$, then this can be solved from here. Note that we can get any matrix from $A$ to $U$ by performing a set of matrix multiplications: 
$$
E_{k}\dots E_{2}E_{1}A\vec{x} = Ek\dots E_{2}E_{3}
$$

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