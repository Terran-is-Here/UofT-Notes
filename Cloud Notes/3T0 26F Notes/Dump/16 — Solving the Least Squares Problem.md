---
updated_at: 2026-11-09T12:50:48.415-05:00
edited_seconds: 170
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 16
Lecture Date: 2026-11-09
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[15 — Rank, Consistency and Dimensions]]
Next: N/A

> [!ila] Lecture Goals
> Apply Linear Algebra to the simplest statistical model present: Linear Regression. 

--- 
# Lecture Notes
## Matrix Transpose
To take the Transpose of some Matrix, we simply take the transpose of the corresponding column vectors and set them as our corresponding row vectors. 
> In terms of an actual full matrix, consider this as simply flipping the matrix across the main diagonal.

For instance; 
$$
A=\begin{bmatrix}
1 & 2  & -1 \\
0 & 5 & 6
\end{bmatrix}
$$
Then: 
$$
A^{T} = \begin{bmatrix}
1 & 0 \\
2 & 5 \\
-1 & 6
\end{bmatrix}
$$
A Matrix Transpose has the following rules: 
* $(A^{T})^{T} = A$
* $(cA)^{T} = cA^{T}$, where $c$ is a scalar. 
* $(A+B)^{T} = A^{T} + B^{T}$
* $(AB)^{T} = B^{T}A$ (Order is flipped corresponding to matrix, proof is left as an exercise to the reader). 


## Regression
For the case of Linear Regression, we will define the $x$ variable as the *explanatory variable*, and the $y$ axis as the corresponding *response variable*. 

For our lecture example, we wanted to linearly regress a set of data pertaining to the relationship between a heating bill and a temperature, then
* Our temperature is equivalent to our $x$ term, that is our *explanatory variable*. 
* Our power bill is equivalent to our $y$ term, that is our *response* variable. 

That is, we want to relate our $x$ to our $y$ by some function of $x \to y$. Starting out with an example data set of hte following: 
* $(x_{1},y_{1})=(-1,6)$
* $(x_{2},y_{2})=(2,0)$
* $(x_{3},y_{3})=(3,2)$
We want to solve for a function which goes through all *three* of these points. For this case, lets assume that we want to model this in the form of a quadratic function, that is some: 
$$
y=a+bx + cx^{2}
$$
Noting that this now becomes a system of equations if we plug in our points into our quadratic formula, 
$$
\begin{align}
6 & =a -b+c \\
0 & =a+2b+4c \\
2  & =a + 3b + 9c
\end{align}
$$
Then, noting this can be rewritten as the following system, then: 
$$
\begin{bmatrix}
1 & x_{1} & x_{1}^{2} \\
1 & x_{2} & x_{2}^{2} \\
1 & x_{3} & x_{3}^{3}
\end{bmatrix}\begin{bmatrix}
a\\b\\c
\end{bmatrix} = \begin{bmatrix}
y_{1}\\ y_{2}\\y_{3}
\end{bmatrix}
$$
Plugging in our values, then: 
$$
\begin{bmatrix}
1 & -1 & 1 \\
1 & 2 & 4 \\
1 & 3 & 9
\end{bmatrix}\begin{bmatrix}a\\b\\c
\end{bmatrix}=
\begin{bmatrix}
6\\0\\2
\end{bmatrix}
$$
Solving the corresponding system gives us the following: 
$$
\left[\begin{array}{ccc|c}
1 & 0 & 0 & 2 \\
0 & 1 & 0 & -3 \\
0 & 0 & 0 & 1 
\end{array} \right]
$$
Then our function is the following: 
$$
y=2-3x-x^{2}
$$
Where this goes through *all three* points. Note however that when we do this, we directly overfit (as we exactly fit our points), and the corresponding equation does not make resultant sense. 

### Linear Regression
Consider now, what if we want to linearly regress a line through all 3 points? Retaking our equation of a line and plugging it for all three points: 
$$
\begin{bmatrix}
1 & x_{1} \\
1 & x_{2} \\
1 & x_{3}
\end{bmatrix}\begin{bmatrix}
a \\b
\end{bmatrix} = \begin{bmatrix}
y_{1}\\y_{2}\\y_{3}
\end{bmatrix}
$$
Plugging in our values once more: 
$$
\begin{bmatrix}
1 & -1 \\
1 & 2 \\
1 & 3
\end{bmatrix}\begin{bmatrix}
a\\b
\end{bmatrix} = \begin{bmatrix}
6\\0 \\2
\end{bmatrix}
$$
Preforming Gaussian Elimination gives us the following system:
$$
\left[\begin{array}{cc|c}
1 & 0 & 4 \\
0 & 1 & -2 \\
0 & 0 & 1 
\end{array} \right]
$$
Note the inconsistencies at the bottom. This implies that we *cannot directly fit all three points on the line*