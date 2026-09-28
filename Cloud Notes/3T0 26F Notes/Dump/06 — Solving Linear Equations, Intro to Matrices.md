---
updated_at: 2026-09-28T12:48:52.789-04:00
edited_seconds: 1880
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
Next: [[07 — Matrix Vector Products]]
Tutorial: 

--- 
# Lecture Notes
Linear Algebra is solving a *set* or *system* of linear equations[^1]. This has a wide variety of applications. 

> Applications
> For instance: Professor (Chen?) is researching particulate matter present in the air (due to their focus as an atmospheric chemist). Particulate Matter present can be described as a histogram with the number of particles present with respects to their relative size.
> 
> We can use linear algebra to back-propagate values from particles measured, to predicted amounts present (as some particulates may be categoized as another size due to uncertainties due to measurements): $$\begin{align}N_{1}^` &= 0.9N_{1} + 0.1 N_{2} + 0.05 N_{3} \\N_{2}^` &= 0.1N_{1} + 0.8 N_{2} + 0.10 N_{3} \\N_{3}^` &= 0.0N_{1} + 0.1 N_{2} + 0.85 N_{3} \end{align}$$
> This is a system of linear equations, which is the focus of linear algebra. 
---

Consider the following two equations: 
$$\begin{align}x-2y &=1 \\ 3x+2y &=11\end{align}$$
The purposes of this Lecture Note is to show two methods to express this linear system: as a row picture, and as a column picture. Note that the goal of this is to solve for a set of $(x,y)$ that satisfy both equations *simultaneously*. 
## Row Picture 
The Row Picture essentially wants us to solve our equation as the solution (for our case above) as the intersection point of our two line equations above. 
$$
\begin{align}x-2y &=1 \\ 3x+2y &=11\end{align}
$$
In this case, the solution is the point $(3,1)$. 
## Column Picture
The Column Picture asks us to solve this in terms of "columns", i.e. vertically. Instead of seeing them as a set of two linear equations that need to be simultaneously satisfied, this can be represented as the following vector equation: 
$$\begin{bmatrix}x-2y\\3x+2y\end{bmatrix} = \begin{bmatrix}1\\11\end{bmatrix}$$
This can be rewritten as: 
$$
x\begin{bmatrix}1\\3\end{bmatrix} + y\begin{bmatrix}-2\\2\end{bmatrix} = \begin{bmatrix}1\\11\end{bmatrix}
$$
That is, we rewrite our linear system into solving for the coefficients for a *linear combination* which leads to our resultant vector. Note that the components of the coordinate space formed by our vectors $\begin{bmatrix}1\\3\end{bmatrix}$ and $\begin{bmatrix}-2\\2\end{bmatrix}$ **are no longer present in** $\mathbb{R}^2$, but rather their own unique coordinate space (as $x,y$ are now linear coefficients for our linear combinations.) This coordinate space is represented by the corresponding components of our column vector (e.g. $r_{1},r_{2}$). 
In this case, $x=3,y=1$ gives us our solution, i.e. $(3,1)$:  
$$3\begin{bmatrix}1\\3\end{bmatrix} + 1\begin{bmatrix}-2\\2\end{bmatrix} = \begin{bmatrix}1\\11\end{bmatrix}$$
## Introduction to Matrices
Matrices are generally described as a means to describe a system of equations. A matrix is represented as a rectangular array of numbers with a size of $m\times n$, where $m$ is the number of rows, and $n$ is the number of columns. For instance: $$A = \begin{bmatrix}4 & 8 & 3 \\2 & 1 & -9\end{bmatrix}$$
The matrix $A$ has a size of $2\times 3$. Generally for a matrix: 
$$
A =\begin{bmatrix}\vec{r}_{1} \\\vec{r}_{2} \\\vdots \\\vec{r}_{n}\end{bmatrix} = \begin{bmatrix}
\vec{c_{1}} & \vec{c_{2}} & \dots &\vec{c_{n}}
\end{bmatrix}$$
Where $\vec{r_{n}}$ is some row vector, and $\vec{c_{n}}$ is some column vector. For Instance: 
$$
\begin{align}
\vec{r}_{1}&=\begin{bmatrix}
4 & 8 & 3
\end{bmatrix} \\
\vec{c_{1}} &=\vec{r_{1}}^T = \begin{bmatrix}4\\8\\3\end{bmatrix}
\end{align}
$$
### AX=B Matrix (Lecture) 
Taking our earlier example: 
$$
\begin{align}x-2y &=1 \\ 3x+2y &=11\end{align}
$$
We can represent this as the following matrix-vector multiplication: 
$$
\begin{align}
\begin{bmatrix}1 & -2 \\3 & 2\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}&=\begin{bmatrix}1 \\11\end{bmatrix} \\
\mathbf{A\vec{v}} &=\vec{b}
\end{align}$$
Where this represents our system above. We often notate our coefficients as some matrix $\mathbf{A}$, our vector of variables $\vec{v}$, and our vector of constants $\vec{b}$. This raises the question though, how *do* we multiply *matrices* with *vectors*? 
#### Row Picture
The multiplication of a matrix by a vector can be described as the following. Taking our earlier example to demonstrate: 
$$
\begin{align}
\begin{bmatrix}1 & -2 \\3 & 2\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}&=\begin{bmatrix}1 \\11\end{bmatrix} =\begin{bmatrix}\vec{r_{1}}^T \cdot \vec{x}\\ \vec{r_{2}}^T \cdot \vec{x}
\end{bmatrix}\\\end{align}$$
Where $\vec{r_{n}}$ is equivalent to the $n$'th row of our vector. This then gives us the following system back: 
$$
\begin{bmatrix}1\\-2\end{bmatrix}\cdot \begin{bmatrix}x\\y\end{bmatrix} = 1x-2y = 1
$$
$$
\begin{bmatrix}3\\2\end{bmatrix}\cdot \begin{bmatrix}x\\y\end{bmatrix} = 3x+2y = 11
$$
This is generally defined in this equation (taken from Pre-Lecture Notes): Note that in this case, a $m\times n$


---
# Pre-Lecture Notes
For the purposes of this note, consider the problem where we are trying to solve for a solution for a system of 3 equations with 3 unknowns ($x,y,z)$, that is the intersection points of 3 planes if they exist: 
$$
\begin{align}
a_{11}x + a_{12}y + a_{13}z &= b_{1} \\
a_{21} x+a_{22}y+a_{23}z &= b_{2} \\
a_{31}x + a_{32}y + a_{33}z &= b_{3}
\end{align}
$$
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
The Column Picture of solving for the solution of a system of 3 equations deals with solving for a **linear combination** that solves for our solution set of $x,y,z$. 

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
\vec{r_{1}}^T \cdot x \\
\vec{r_{2}}^T \cdot x \\
\vdots \\
\vec{r_{m}}^T \cdot x
\end{bmatrix}=\begin{bmatrix}b_{1} \\b_{2} \\\vdots \\b_{m}\end{bmatrix}$$
Note that we define $\vec{r_{i}}^T \cdot x$ as the following: 
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

### Implication
What this implies is that we can find the vector pointing to the possible intersection of the set of $m$ amounts of hyperplanes existing in the $n-1$-th dimension with a vector that points to it in $n-1$ space as the result of a Matrix-Vector multiplication operation. 
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

[^1]: Well, specifically for linear algebra.
