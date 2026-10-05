---
updated_at: 2026-09-29T17:56:01.484-04:00
edited_seconds: 700
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
> [!ila] Summary
> For all 3 methods (algebraic, row picture, column picture), we can solve $\mathbf{A}\vec{x} = \vec{b}$ for any values $b_{1},b_{2},b_{3}$; that is we can solve for the values in $\vec{x}$. 
> * The Row Picture solves for a point that is *present* within all  hyperplanes *if* they exist. 
> * The Column Picture solves for a linear combination of column vectors that points to our *resultant* vector $\vec{b}$ if a solution exists. 
> 
> Note that this can only be solved for any value of $\vec{b}$ if and only if all columns vectors of $\mathbf{A}$ are linearly independent. 
## Matrix Operations
Recall the definition of a matrix in our context: 
$$
\mathbf{A} = m\times n \text{ matrix}
$$
Where:
* $m$ is the number of rows, essentially the number of equations.
* $n$ is the number of columns, essentially the number of variables. 

If $m=n$, $\mathbf{A}$ is a square matrix. Matrix Addition is solely defined in terms of matrices **with the same dimension**


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

### Row Picture 
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
3x_{1}+5x_{2}+6x_{6} =4\implies x_{3}&=1 \tag{3}
\end{align}
$$
Note that the following planes represent the following: 
* $(1)$ represents a plane in $\mathbb{R}^3$ with a normal vector of $\begin{bmatrix}1\\0\\0\end{bmatrix}$. 
* $(2)$ represents a plane in $\mathbb{R}^3$ with a normal vector of $\begin{bmatrix}2\\4\\0\end{bmatrix}$
* $(3)$ represents a plane in $\mathbb{R}^3$ with a normal vector of $\begin{bmatrix}3\\5\\6\end{bmatrix}$
And the resulting equation for $\vec{x}$:
$$
\vec{x} = \begin{bmatrix}
1\\-1\\1
\end{bmatrix}
$$
Gives us the *point* in $\mathbb{R}^3$ where these planes intersect. Or in other words, the concept of satisfying all 3 equations is equivalent to finding a point that lies within all 3 planes. 

> [!ila] In-Lecture Addendum / Important Idea
> The solution (if it exists) of a Linear System in a Row Picture method gives us a point which is present within all planes / equations present. Take the following: 
> $$\begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} =\begin{bmatrix}b_{1}\\b_{2}\\b_{3}\end{bmatrix}= \begin{bmatrix}1\\-2\\4\end{bmatrix}$$
> In this case, $\vec{x}$ gives us the *point* that lies on all 3 planes if it exists. 

### Column Picture
Taking the Column Picture: 
$$
\begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} =\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}= \begin{bmatrix}1\\-2\\4\end{bmatrix}
$$
This now instead represents the attempt of trying to find a linear combination which results to our $\vec{b}$: 
$$
\begin{bmatrix}
1\\2\\3
\end{bmatrix}x_{1}
+ \begin{bmatrix}
0\\4\\5
\end{bmatrix}x_{2}
+ \begin{bmatrix}
0\\0\\6
\end{bmatrix}x_{3}
=\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}
 = \begin{bmatrix}
 1\\-2\\4
\end{bmatrix}
$$
We now need to find the set of scalars of $x_{1},x_{2},x_{3}$ to make this linear combination true. Our solutions above still hold true (and we'd solve it in the same way: 
$$
\begin{bmatrix}
1\\2\\3
\end{bmatrix}1
+ \begin{bmatrix}
0\\4\\5
\end{bmatrix}(-1)
+ \begin{bmatrix}
0\\0\\6
\end{bmatrix}1
=\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}
 = \begin{bmatrix}
 1\\-2\\4
\end{bmatrix}
$$
> [!ila] In-lecture Addendum \ Important Idea
> The solution of a Linear System via Column Picture method is equivalent to finding the correct linear combination of our column vectors which will result in our final, constant vector / $\vec{b}$. 

## Generalization
Can we take our system above, and solve it for all possible values of $b_{1},b_{2},b_{3}$ (or the system below attached)
$$
\begin{bmatrix}1 & 0 & 0 \\2 & 4 & 0 \\3 & 5 & 6\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} =\begin{bmatrix}
b_{1}\\b_{2}\\b_{3}
\end{bmatrix}
$$
Note that from our Column Picture, we know that this system can be expressed as some linear combination of $3$ vectors. The question that we're really asking is, can we express one of our vectors as a *linear combination* of one of our two other vectors? In this case, let's take $\vec{c_{3}}$ :
$$
c\begin{bmatrix}
1\\2\\3
\end{bmatrix}
+ d\begin{bmatrix}
0\\4\\5
\end{bmatrix}
= \begin{bmatrix}
0\\0\\6
\end{bmatrix} \to 
\left[\begin{array}{cc|c}
1c & 0d & 0 \\
2c & 4d & 0 \\
3c & 5d & 6
\end{array}\right]
$$
Using some quick algebra, we can see that $c,d=0$, which means that there exists no linear combination (specifically, $0=6$ is required, which is false.) This means that $\vec{c}_{3}$ cannot be expressed as a linear combination of 3 other vectors. This means that this system is [[09— Basic Linear Algebra Concepts#Linear Independence|Linearly Independent]]. 

If a system is purely composed of linearly independent vectors, then all combinations of column vectors fill $\mathbb{R}^3$. 
