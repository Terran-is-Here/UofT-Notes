---
updated_at: 2026-09-27T12:40:02.149-04:00
edited_seconds: 1370
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 6
Lecture Date: 2026-09-28
Week: 4
created:
Created: September 21st 2026, 9:13:07 pm
---
Hub: [[ESC103 Hub]]
Previous: [[05 — Equations of Lines and Planes]]
Next: N/A 
Tutorial: 

--- 
# Lecture Notes
# Pre-Lecture Notes
For the purposes of this note, consider the problem where we are trying to solve for a solution for a system of 3 equations with 3 unknowns ($x,y,z)$, that is the intersection points of 3 planes if they exist: 
$$a_{11}x + a_{12}y + a_{13}z = b_{1}$$
$$a_{21} x+a_{22}y+a_{23}z = b_{2}$$
$$a_{31}x + a_{32}y + a_{33}z = b_{3}$$
Or, in augmented matrix form, they can be expressed as: 
$$
\left[\begin{array}{ccc|c}
a_{11} & a_{12} & a_{13} & b_{1} \\
a_{21} & a_{22} &a_{23}&b_{2} \\
a_{31} & a_{32} & a_{33} & b_{3}
\end{array}
\right]
$$
## Row Picture
The row pictures deal with considering our equations above as a series of $3$ planes, and simply solving for the solution of $x,y,z$ that satisfies all the values; where the resultant intersection gives you the point at which all three planes intersect. In other words, we want to return that augmented matrix above us into a row-echelon / row-reduced matrix. 

## Column Picture
The Column Picture of solving for the solution of a system of 3 equations deals with solving for a linear combination that solves for our solution set of $x,y,z$. 

Note that we can define 3 vectors from the equations above based on if they're in terms of $x$, $y$, or $z$: 
$$
\vec{v_{x}} = \begin{bmatrix}a_{11} \\a_{21} \\a_{31}\end{bmatrix},
\vec{v}_{y} = \begin{bmatrix}a_{12} \\a_{22} \\a_{32}\end{bmatrix}, 
\vec{v}_{z} = \begin{bmatrix}a_{13} \\a_{23} \\a_{33}\end{bmatrix}
$$
Our solutions / $b$ values can also be defined by their own vector: 
$$
\vec{b} = \begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix}
$$

Therefore, we can define the following as an alternate means of viewing how to solve our expression above: 
$$
x\vec{v}_{x} + y\vec{v}_{y} + z\vec{v}_{z} = \vec{b}$$
Subbing in our values: 

$$x\begin{bmatrix}a_{11} \\a_{21} \\a_{31}\end{bmatrix} + y\begin{bmatrix}a_{12} \\a_{22} \\a_{32}\end{bmatrix}+z\begin{bmatrix}a_{13} \\a_{23} \\a_{33}\end{bmatrix} =\begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix}$$
Where our goal now is to solve for a set of solutions of $x,y,z$ to solve for a linear combination of the vectors $\vec{v}_x,\vec{v}_{y}, \vec{v}_{z}$ that equals $\vec{b}$. 
## General Expression
Recall how we defined the concept of a [[02 —Vector Dot Product#Dot Product / Scalar Product|Dot Product]], we generally defined it as the sum of the respective products of two matrices. 

That is, given matrices $A$, and $B$, where $A$ is a row vector of $m\times {1}$ and $B$ is a column vector of $1 \times n$ where $m=n$
$$
A\cdot B = C
$$
The term at  $C_{xy}$ is defined by the sum of: 
$$
C_{xy} = \sum^n_{i=1} A_{xi} B_{iy}
$$
That is: 
$$
\begin{bmatrix}a_{1} \\a_{2} \\\vdots \\a_{m}\end{bmatrix} 
\begin{bmatrix}b_{1} & b_{2} & \dots b_{n}\end{bmatrix} = \left[\sum^n_{i=1} A_{xi} B_{iy}\right]
$$


## AX=B Matrix
> [!quote] Relevant Textbook Section: 
> [[Nicholson-OpenLAWA-2018B.pdf#page=69&offset=54,733,0|2.2 - Equations, Matrices and Transformations]]

We now introduce the notation of an $Ax=B$ Matrix.
* Let $A$ be equal to some matrix $m\times n$ composed of coefficients: 
	* $m$ represents the number of equations (rows).
	* $n$ represents the number of variables present (columns). 
* let $x$ be equal to some matrix $n \times 1$ of variables, 
	* That is, our variable vector has a number of rows equal to the columns of coefficients present. 
* Let $b$ be equal to some matrix $m\times {1}$ of constants.
	* That is, our output / constant vector has a number of rows equal to the rows of *equations* present. 

$$\vec{A} =\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix},
\vec{x} = \begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix},\vec{b} = \begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}$$

We define $A\mathbf{x}=\mathbf{b}$ as: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix} = \begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}
$$
Note that this is equivalent to our equation earlier; that for the $i$-th row, the corresponding value from the left is defined as the following. For the purposes of this, we will introduce the notation $\vec{r_{i}} = \begin{bmatrix}a_{i1} & a_{i 2} &\dots a_{i n} \end{bmatrix}$, that is $\vec{r_{i}}$ is a row vector representing the $i$-th row of $\vec{A}$, therefore: 
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} & \dots & a_{1n}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n}\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn}
\end{bmatrix}\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix} = 
\begin{bmatrix}
\vec{r_{1}} \cdot x \\
\vec{r_{2}} \cdot x \\
\vdots \\
\vec{r_{n}} \cdot x
\end{bmatrix}=\begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}$$
Note that we define $\vec{r_{i}} \cdot x$ as the following: 
$$
\vec{r_{i}} \cdot x = a_{i1} x_{1} + a_{i2}x_{2} + \dots+a_{in}x_{n} = b_{i}
$$

This expression if you notice is actually similar to our expressions earlier for our scalar equations of a plane. Retaking our $3 \times 3$ matrix from earlier, then: 
$$
\begin{bmatrix}a_{11} & a_{12} & a_{13} \\a_{21} & a_{22} & a_{23} \\a_{31} & a_{32} & a_{33}\end{bmatrix}\begin{bmatrix}x \\y \\z\end{bmatrix} = \begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix} \text{ which can be roughly represented like } \left[\begin{array}{ccc|c}
a_{11} & a_{12} & a_{13} & b_{1} \\
a_{21} & a_{22} &a_{23}&b_{2} \\
a_{31} & a_{32} & a_{33} & b_{3}
\end{array}
\right]
$$
Where the solution of the augmented matrix on the right resolves in our $\mathbf{x}$; that is the solution to the following: 
$$
\text{ the solution of }\left[\begin{array}{ccccc|c}
a_{11} & a_{12} & a_{13} & \dots & a_{1n} & b_{1}\\
a_{21} & a_{22} & a_{23} & \dots & a_{2n} & b_{2}\\
\vdots & \vdots & \vdots & \ddots & \vdots & \vdots\\
a_{m 1} & a_{m 2} & a_{m 3} & \dots & a_{mn} & b_{m} \\
\end{array}\right] \text{ gives us }
\begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{n}\end{bmatrix}
$$
This can actually be generalized, as we can extend this to any size of $x,b$ as long as their width remains the same. What this means is we can transform $\mathbf{A}$ into it's RREF to solve for our terms in $x$ based on $b$. 

### Backing Logic 
Retake our original set of 3 equations that we had at the top: 
$$a_{11}x + a_{12}y + a_{13}z = b_{1}$$
$$a_{21} x+a_{22}y+a_{23}z = b_{2}$$
$$a_{31}x + a_{32}y + a_{33}z = b_{3}$$
Note how we can redefine this as a set of 3 column vectors: 
$$
x\begin{bmatrix}a_{11} \\a_{21} \\a_{31}\end{bmatrix} + y\begin{bmatrix}a_{12} \\a_{22} \\a_{32}\end{bmatrix} + z\begin{bmatrix}a_{13} \\a_{23} \\a_{33}\end{bmatrix}  = \begin{bmatrix}b_{1} \\b_{2} \\b_{3}\end{bmatrix}
$$
That is, we can turn our system above into a column picture of vectors, Note that if we define our variables in terms of their own vector, that is: 
$$
\mathbf{x} = \begin{bmatrix}x \\y \\z\end{bmatrix}
$$