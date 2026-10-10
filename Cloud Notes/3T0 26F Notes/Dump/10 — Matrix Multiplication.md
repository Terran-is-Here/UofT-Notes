---
updated_at: 2026-10-09T16:47:53.397-04:00
edited_seconds: 1030
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 10
Lecture Date: 2026-10-06
Week: 5
---
Hub: [[ESC103 Hub]]
Previous: [[09— Basic Linear Algebra Concepts]]
Next: [[11 — A-CR Matrices]]
> [!quote] Learning Objectives
> * Perform matrix multiplication $\mathbf{AB}$ using the linear combination of the columns of matrix $\mathbf{A}$.
> * Perform matrix multiplication $\mathbf{AB}$ using the dot products of rows of matrix $\mathbf{A}$ with the columns of matrix $\mathbf{B}$
--- 
# Lecture Notes
## Matrix Multiplication (LEC) 
Recall from when we defined the $\mathbf{A}\vec{x}=\mathbf{B}$ operation: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix} = \begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}
$$
If we add more rows into $\vec{x}$, then the corresponding rows of $\vec{b}$ will scale accordingly: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{11} & x_{12} \\x_{21} &x_{22} \\\vdots & \vdots \\x_{n1} & x_{n2}\end{bmatrix} = \begin{bmatrix}b_{11}&b_{12} \\b_{21} &b_{22}\\\vdots & \vdots\\b_{m1} & b_{m 2}\end{bmatrix}
$$
In other words; $\mathbf{AB}$'s $j$th column is a column vector equal to $\mathbf{A}$ times the $j$-th column of $B$, that is $A\vec{b}_{j}$.
### Example
Given the two matrices: 
$$
\mathbf{A=}\begin{bmatrix}1 & 2 \\3 & 4\end{bmatrix}
$$
$$
\mathbf{B}=\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
$$
Then $\mathbf{AB}$ would give the following $2\times {2}$ square matrix: 
$$
\begin{bmatrix}
\mathbf{A}\vec{b}_{1} & \mathbf{A}\vec{b}_{2}
\end{bmatrix} = 
\begin{bmatrix}
1(5)+2(7) & 1(6)+2(8) \\
3(5)+4(7)& 3(6) + 4 (8)
\end{bmatrix} = \begin{bmatrix}
19 & 22 \\
43 & 50
\end{bmatrix}
$$
**Remember**, we can always represent an $\mathbf{A\vec{r}}$ as the linear combination of the column vectors of $\mathbf{A}$ with the scalar coefficients present in $\vec{b}_{n}$. 
## Alternate Notation
We can redefine $\mathbf{AB}$ as the following: 
$$
\begin{bmatrix}\dots  & \vec{a}_{1} & \dots \\\dots & \vec{a}_{2} & \dots \\& \vdots \\\dots & \vec{a}_{m} & \dots\end{bmatrix}
\begin{bmatrix}
\vdots & \vdots &  & \vdots \\
\vec{b}_{1} & \vec{b}_{2} & \dots & \vec{b}_{p} \\
\vdots & \vdots &  & \vdots
\end{bmatrix}
=\begin{bmatrix}
\vec{a_{1}}\cdot \vec{b_{1}} & \vec{a_{1}}\cdot \vec{b_{2}}  & \dots & \vec{a}_{1}\cdot \vec{b}_{p}\\
\vec{a_{2}}\cdot \vec{b_{1}} & \vec{a_{2}}\cdot \vec{b_{2}} & \dots & \vec{a_{2}}\cdot \vec{b}_{p} \\
\vdots & \vdots & \ddots & \vdots \\
 &  & & \vec{a}_{i}\cdot  \vec{b}_{j}
\end{bmatrix}
$$
Where the $i$ row and $j$ th column is represented as $M_{ij}=\vec{a_{i}}^T\cdot \vec{b}_{j}$

Retaking our earlier example with this notation: 
$$
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
\begin{bmatrix}
5 & 6 \\
7 & 8
\end{bmatrix}
$$
Gives us : 
$$
\begin{bmatrix}
\begin{bmatrix}1\\2\end{bmatrix}\cdot\begin{bmatrix}5\\7\end{bmatrix} & \begin{bmatrix}1\\2\end{bmatrix}\cdot \begin{bmatrix}6\\8\end{bmatrix} \\
\begin{bmatrix}3\\4\end{bmatrix}\cdot\begin{bmatrix}5\\7\end{bmatrix} & \begin{bmatrix}3\\4\end{bmatrix}\cdot \begin{bmatrix}6\\8\end{bmatrix}
\end{bmatrix} = \begin{bmatrix}19 & 22 \\43 & 50\end{bmatrix}
$$
## Properties of Matrix Multiplication
### Identity Matrix
We will introduce the following identity matrix: 
$$
I = \begin{bmatrix}1 & 0 \\0 & 1\end{bmatrix}
$$
Where this is extended to any $m\times m$ matrix, where all the values on the main diagonal are $1$, and all the values not present on the main diagonal are $0$. Note that if we multiply this by some matrix; then: 
$$
\begin{bmatrix}a & b \\c & d\end{bmatrix} \begin{bmatrix}1 & 0 \\0 & 1\end{bmatrix} = \begin{bmatrix}
\begin{bmatrix}a\\b\end{bmatrix}\cdot \begin{bmatrix}1\\0\end{bmatrix} & \begin{bmatrix}a\\b\end{bmatrix}\cdot \begin{bmatrix}0\\1\end{bmatrix} \\
\begin{bmatrix}c\\d\end{bmatrix}\cdot \begin{bmatrix}1\\0\end{bmatrix} & \begin{bmatrix}c\\d\end{bmatrix}\cdot \begin{bmatrix}0\\1\end{bmatrix}
\end{bmatrix} = \begin{bmatrix}(1)a + (0)b & (0)a + (1)b \\(1)c + (0)d & (0)c + (1)d \end{bmatrix} = \begin{bmatrix}a & b \\c & d\end{bmatrix}
$$

That is, $\mathbf{AI=IA=A}$ (if they share the same generals). 

> [!caution] Matrix Multiplication is NOT communicative: 
$$\mathbf{AB}\neq \mathbf{BA}$$

> [!caution] It IS communicative (with the same order): 
> $$\mathbf{(AB)C}=\mathbf{A(BC)}$$

Note: 
If $\mathbf{A} = m\times n$, and $\mathbf{B}=n\times p$: 
* $\mathbf{AB}=m\times p$
* $\mathbf{BA}$ may not exist (different number of rows and columns)

### Exchange Matrix: 
The exchange matrix is the following: 
$$\mathbf{E}=
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$
Note what happens when we multiply a matrix with it: 
$$
\begin{align}
\begin{bmatrix}a & b \\c & d\end{bmatrix}\begin{bmatrix}0 & 1 \\1 & 0\end{bmatrix} = \begin{bmatrix}b & a \\d & c\end{bmatrix} \\
\begin{bmatrix}0 & 1 \\1 & 0\end{bmatrix}\begin{bmatrix}a & b \\c & d\end{bmatrix} = \begin{bmatrix}c & d \\a & b\end{bmatrix}
\end{align}

$$
If $\mathbf{AE}$, then the resultant matrix will have the corresponding columns of $A$ flipped. if $\mathbf{EA}$, the rows are reversed instead. 
## Application
Recall, if we have some $\mathbf{A}\vec{x}=\vec{b}$: 
$$
\begin{align}
\mathbf{A}\vec{x} &= \vec{b} \\
\mathbf{BA}\vec{x}&=\mathbf{B}\vec{b} \\
\mathbf{(BA)}\vec{x}&=\mathbf{B}\vec{b}
\end{align}
$$
Due to the associativity of Matrix Multiplication being associative; then this may allows us to manipulate our equation to an easier term to work with. **The order MUST be preserved since Matrix Multiplication is NOT communicative**. 

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
