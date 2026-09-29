---
updated_at: 2026-09-29T17:32:17.118-04:00
edited_seconds: 380
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 7
Lecture Date: 2026-09-29
Week: 4
Created: September 29th 2026, 5:12:54 pm
---
Hub: [[ESC103 Hub]]
Previous: [[06 — Solving Linear Equations, Intro to Matrices]]
Next: [[08 — Matrix Vector Products]]

> [!caution] Note
> This note was written primarily in-lecture, as we became out of sync on my pre-written notes. The note for this section was previously [[08 — Matrix Vector Products]].

--- 
# Lecture Notes
## Matrix Operations
Recall the definition of a matrix in our context: 
$$
\mathbf{A} = m\times n \text{ matrix}
$$
Where:
* $m$ is the number of rows, essentially the number of equations.
* $n$ is the number of columns, essentially the number of variables. 

If $m=n$, $\mathbf{A}$ is a square matrix. We define Matrix Addition through Square Matrices: 


$$
\mathbf{A} + \mathbf{B} = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{bmatrix}+\begin{bmatrix}b_{11} & b_{12} \\b_{21} & b_{22}\end{bmatrix} = \begin{bmatrix}
a_{11}+b_{11} & a_{12}+b_{12} \\
a_{21}+b_{21} & a_{22}+b_{22}
\end{bmatrix}
$$
## Solving Linear Systems
We can apply this into a linear system of equations with 3 variables: 
$$
\begin{align}
x_{1} + 0x_{2} + 0x_{3}&= b_{1} =1 \\
2x_{1} + 4x_{2} +0x_{3}&= b_{2} =-2  \\
3x_{1} + 5x_{2} + 6x_{3} &= b_{3} = 4
\end{align}
$$
This system can be represented as the following matrix in the form of $\mathbf{A}\vec{x}=\vec{b}$; where $\mathbf{A}$ is our coefficient matrix, $\vec{x}$ being our unknown/variable matrix, and $\vec{b}$ being our constant matrix. 
$$\begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} =\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}= \begin{bmatrix}1\\-2\\4\end{bmatrix}$$
Now comes the question: *how do we solve for our variables* in this context? We can solve it algebraically, or by the two pictures that we learned. 

> [!theorem] Note
> Our $\mathbf{A}$ is actually in the form of a lower-triangular matrix, where the values above the main diagonal are $0$.
> > The counterpart to this is the upper-triangular matrix, where the values *below* the main diagonal are $0$
> 
> For the purposes of analysis though, this simply rearranges the order we solve our system from (i.e. from top to bottom or bottom to top)

> [!ila] In-Lecture Addendum
> The following matrix is something that we denote as an *identity matrix*: $$\begin{bmatrix}1 & 0 & 0 \\0 & 1 & 0 \\0 & 0 & 1\end{bmatrix}$$
> Where the sole values present are on the main diagonal, and these values are the value $1$. This plane has the interesting property of the following: 



> We can solve this algebraically trivially. Note however that this simply solves for a set of *values* without giving us any form of geometric interpretation. 

## Row Picture 
Taking the row picture; then this comes as the intersection of 3 2-dimensional hyperplanes: 
$$
\begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} =\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}= \begin{bmatrix}1\\-2\\4\end{bmatrix}
$$
Then it comes that: 
$$
\begin{align}
x_{1}+0x_{2}+0x_{3} = b_{1} = 1 \implies x_{1}&=1 & \tag{1}\\
2x_{1} + 4x_{2} + 0x_{3} = b_{1} = -2 \implies x_{2}&=-1 \tag{2} \\
3x_{1}+5x_{2}+6x_{6} =4\implies x_{3}=1 \tag{3}
\end{align}
$$
Note that the following planes represent the following: 
* $(1)$ represents a plane in $\mathbb{R}^3$ with a normal vector of $\begin{bmatrix}1\\0\\0\end{bmatrix}$. 
* $(2)$ represents a plane in $\mathbb{R}^2$ with a normal vector of $$b$$
That is: 
$$
\vec{x} = \begin{bmatrix}
1\\-1\\1
\end{bmatrix}
$$