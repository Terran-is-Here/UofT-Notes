---
updated_at: 2026-11-10T17:29:05.997-05:00
edited_seconds: 300
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
Note the inconsistencies at the bottom. This implies that we *cannot directly fit all three points on the line* (which makes sense) The approach we then take, is how to minimize the distances between the points on the line, and a line of best fit.

It is very common to have a dataset of points that we believe follows some kind of curve (a "model"), but due to certain "errors" within our data, the associated system directly may be unsolvable. 

Consider the case where we break up our system above into it's column picture, we see that this simply states that *the value for $b$* is outside the column space of our matrix: 
$$
\begin{bmatrix}
1\\1\\1
\end{bmatrix}a+ \begin{bmatrix}
-1\\2\\3
\end{bmatrix}b = \begin{bmatrix}
6\\0\\2
\end{bmatrix}
$$
Our goal is to find some vector $y_\text{ls}$ (or rather, $Ac_\text{ls}$ such that it is *closest* to our $y$ (or in other words, some $\vec{y_\text{ls}}$ that is closest to $\begin{bmatrix}6\\0\\2\end{bmatrix}$ in our equation above for instance). 

Before solving the Problem of Least Squares, we find that for some vector $\vec{y}$, and the corresponding least-squares $\vec{y_\text{ls}}$, the corresponding residual vector (some error vector, some $\vec{e}$) being the following: 
$$
\vec{e} = \vec{y} - A\vec{c_\text{ls}}
$$

Or in other words, we want to find some $\vec{y_\text{ls}}=A\vec{c_\text{ls}}$, where this is equivalent to the *orthogonal projection* in some way of $\vec{y}$ onto the column space of $\vec{A}$. That is: 

$$
\vec{e} = \vec{y} - \vec{y_\text{ls}} = \begin{bmatrix}
y^{\text{data}}_{1}-y^{\text{model}}_{1} \\
y^{\text{data}}_{2}-y^{\text{model}}_{2} \\
y^{\text{data}}_{3}-y^{\text{model}}_{3}
\end{bmatrix}
$$
Consider now then what would be the magnitude of this error term? Then: 
$$
||\vec{e}||^{2} = (y^{\text{data}}_{1}-y^{\text{model}}_{1})^{2} + (y^{\text{data}}_{2}-y^{\text{model}}_{2})^{2}
$$
Or, alternatively: 
$$
||\vec{e}||^{2} = \sum_{i}(y^{\text{data}}_{i}-y^{\text{model}}_{i})^{2}
$$
And the concept is that, we want to *minimize* this term, thus minimizing the corresponding square. 
## Solving Least Squares
Our goal is therefore: 
> Find some $\vec{c_\text{ls}}$ such that $\vec{e}=\vec{y}-A\vec{c_\text{ls}}$ is orthogonal to the column space to $A$. 

Consider the matrix $A$ as the following: 
$$
A = \begin{bmatrix}
\vdots & \vdots & \vdots & \vdots \\
a_{1} & a_{2} & \dots & a_{i} \\
\vdots & \vdots & \vdots & \vdots
\end{bmatrix}
$$
Taking it's transpose, then: 
$$
A^{T} = \begin{bmatrix}
\dots & a_{1}^{T} & \dots \\
\dots & a_{2}^{T} & \dots \\
\dots & \vdots& \dots \\
\dots & a_{i}^{T} & \dots
\end{bmatrix}
$$
If $\vec{e}$ is orthogonal to $A$'s column space, then for all $c\cdot a_{i}=0$. Then: 
$$
A^{T}e = \vec{0}
$$

Thus, doing some algebra from our earlier definition of $e$, then: 
$$
\begin{align}
A^{T}\vec{e}  & = \vec{0} \\
A^{T}(\vec{y}-A\vec{c_\text{ls}})  & =\vec{0} \\
A^{T}\vec{y} -A^{T}A\vec{c_\text{lls}}
\end{align}
$$