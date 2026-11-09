---
updated_at: 2026-11-09T12:38:27.502-05:00
edited_seconds: 870
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 15
Lecture Date: 2026-11-03
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[14 — Gaussian Elimination]]
Next: [[16 — Solving the Least Squares Problem]]

--- 
# Lecture Notes
## Applying Gaussian
Consider now the following expression: 
$$
\begin{align}
3x+2y+3x = 20 \\
4x+4y+2z=30 \\
2x+3y+z=19
\end{align}
$$
Performing gaussian Elimination: 
$$
\begin{align}
\left[\begin{array}{ccc|c}
3 & 2 & 3 & 20 \\
4 & 4 & 2 & 30 \\
2 & 3 & 1 & 19 
\end{array} \right] & : r_{2}-2r_{3} \\
\left[\begin{array}{ccc|c}
3 & 2 & 3 & 20 \\
0 & -2 & 0 & -8 \\
2 & 3 & 1 & 19
\end{array} \right]  & : \frac{1}{3}r_{1} \\
\left[\begin{array}{ccc|c}
 1 & \frac{2}{3} & 1 & \frac{20}{3} \\
 0 & -2 & 0 & -8 \\
 2 & 3 & 1 & 19
\end{array} \right] & : -\frac{1}{2}r_{2} \\
\begin{array}{ccc|c}
1 & \frac{2}{3} & 1 & \frac{20}{3} \\
0 & 1 & 0 & 4 \\
2 & 3 & 1 & 19
\end{array} 
\end{align}
$$
We know where we would go from here, but this would eventually result in the following matrix $A$, then: 
$$
\left[\begin{array}{ccc|c}
 1 & 0 & 0 & 3 \\
 0 & 1 & 0 & 4 \\
 0 & 0 & 1 & 1
\end{array} \right]
$$
Then we see that: 
$$
\begin{align}
x=3 \\
y=4 \\
z=1
\end{align}
$$
This implies that: 
* From the row picture, $(3,4,1)$ is the only point that lies on **all three planes**. 
* From the column picture, this solution set corresponds to the required scalar coefficients required in a linear combination of our equation terms. 
However, consider that we could perform other rows to both sides; as we maintain the equality in both sides; we thus need to simply find another plane which fits the same solutions. 

Consider now the following system: 
$$
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
4 & 4 & 2 & 30 \\
2 & 3 & 1 & 19 
\end{array} \right]
$$
Then, Using GE: 
$$
\begin{align}
\left[\begin{array}{ccc|c} 
4 & 1 & 2 & 18 \\
4 & 4 & 2 & 30 \\
2 & 3 & 1 & 19
\end{array} \right] & :r_{2}-r_{1} \\
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
0 & 3 & 0 & 12 \\
2 & 3 & 1 & 19 
\end{array} \right] & : r_{3}- \frac{1}{2}r_{1} \\
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
0 & 3 & 0 & 12 \\
0 & 2.5 & 0 & 10 
\end{array} \right] & : \frac{1}{3}r_{2} \\
\left[\begin{array}{ccc|c}
 4 & 1 & 2 & 18 \\
 0 & 1 & 0 & 4 \\
 0 & 2.5 & 0 & 10
\end{array} \right] & : r_{3}-2.5r_{2} \\
\left[\begin{array}{ccc|c} 
4 & 1 & 2 & 18 \\
0 & 1 & 0 & 4 \\
0 & 0 & 0 & 0
\end{array} \right] \\
\left[\begin{array}{ccc|c} 
4 & 0 & 2 & 14 \\
0 & 1 & 0 & 4 \\
0 & 0 & 0 & 0
\end{array} \right] & : \frac{1}{4}r_{1} \\
\left[\begin{array}{ccc|c}
1 & 0 & \frac{1}{2} & \frac{14}{4}=\frac{7}{2} \\
0 & 1 & 0 & 4 \\
0 & 0 & 0 & 0 
\end{array} \right]
\end{align}
$$
Then we find that: 
$$
\begin{align}
1x + \frac{1}{2}z = \frac{7}{2} \\
y=4
\end{align}
$$
Then, setting $z$ as a free variable; then: 
$$
\begin{align}
x  & =\frac{7}{2}-\frac{1}{2}z \\
y & =4 \\
z & =z
\end{align}
$$
Thus: 
$$
\begin{bmatrix}
x\\y\\z
\end{bmatrix} = \begin{bmatrix}
\frac{7}{2\\4\\0}
\end{bmatrix} + \begin{bmatrix}
-\frac{1}{2}\\0\\1
\end{bmatrix}z
$$
The *row* picture represents a line in $\mathbb{R}^{3}$ space. How about the column picture? Taking it up: 
$$
\begin{bmatrix}
4\\4\\2
\end{bmatrix}\left( \frac{7}{2}-\frac{1}{2}l \right) + \begin{bmatrix}
1\\4\\2
\end{bmatrix}4 + \begin{bmatrix}
2\\2\\1
\end{bmatrix}l = \begin{bmatrix}
18\\30\\19
\end{bmatrix}
$$
Where this equation works for any value of $l$. Expanding this, then: 
$$
\begin{bmatrix}
4\\4\\2
\end{bmatrix} \frac{7}{2} - \begin{bmatrix}
2\\2\\1
\end{bmatrix}z + \begin{bmatrix}
1\\4\\2
\end{bmatrix}4 + \begin{bmatrix}
2\\2\\1
\end{bmatrix}l = \begin{bmatrix}
18\\30\\19
\end{bmatrix}
$$
Note that the terms cancel out, thus: 
$$
\begin{bmatrix}
4\\4\\2
\end{bmatrix} \frac{7}{2} + \begin{bmatrix}
1\\4\\2
\end{bmatrix}4 = \begin{bmatrix}
18\\30\\19
\end{bmatrix}
$$
Where this satisfies any values; then note that this therefore also works for any value of $l$ (or $z$), then the set of solutions is infinite. 

Consider now the following system of equations (now written in an augmented matrix): 
$$
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
4 & 4 & 2 & 30 \\
2 & 3 & 1 & 15
\end{array} \right]
$$
Then, performing GE: 
$$
\begin{align}
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
2 & 2 & 1 & 15 \\
2 & 3 & 1 & 15 
\end{array} \right] & :r_{3}-r_{1} \\
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
2 & 2 & 1 & 15 \\
0 & 1 & 0 & 0 
\end{array} \right] & : 2r_{2}-r_{1} \\
\left[\begin{array}{ccc|c}
 4 & 1 & 2 & 18 \\
 0 & 3 & 0 & 12 \\
 0 & 1 & 0 & 0
\end{array} \right]  & :r_{3}-\frac{1}{3}r_{2} \\
\left[\begin{array}{ccc|c}
4 & 1 & 2 & 18 \\
0 & 3 & 0 & 12 \\
0 & 0 & 0 & -4 
\end{array} \right]
\end{align}
$$
We can stop here, as we see that $0=-4$, which is impossible; thus we state that this system is inconsistent.
* For the row picture, these three planes do not have one common point (or system of intersection). 
* For the column picture, this represents that for some $\vec{b}$, this does not lie within the column space of some matrix $A$. 

### Implications
Thus, we find that when we use Gaussian Elimination to solve some $A\vec{x}=\vec{b}$, we have three possible outcomes: 
1. A unique solution exists: There exists only one solution to our system (thus, no free variables exist, thus every variable is a leading variable). 
	1. In row picture, a singular point serves as the solution. 
2. Infinitely many solutions exist: There exists infinite solutions to our system (at least one free variable exists) 
	1. In row picture, some line or hyperplane expresses the possible set of solutions. 
3. No solutions: There exists an inconsistency, such as $0=C$, where $C$ is some number; in which case then there exists no solution.
	1. In row picture, this means that our planes do not inherently ever collide with each other. 
In this case, we often consider $1,2$ as consistent systems, whilst the third case is termed as an inconsistent system. In this case, how do we inherently know the system that we have? We realize this by performing RREF, and noting the $\text{rank}(A)$. 

In this case, note that if we factor our matrix to some $CR$, then $\text{rank}(R)$ represents the following with respects to some $A$ as $m\times n$ matrix: 
* $m$ represents the number of rows, and the number of equations. 
* $n$ represents the number of columns, or the number of variables. 

Then comparing with our values, then: 
1. $\text{rank}(R)=n$
   This implies that there exists the same number of pivot variables as the number of variables present. Then we see that there exists only **one unique** consistent system.
   Or in other words, all column vectors are linearly independent. 
2. $\text{rank}(R)<n$
   This implies that there exist some *free* variables present (at least one). Then we see that there exists **infinite, consistent** solutions to a potential system. 
   Or in other words, the set of column vectors are linearly dependent.
3. $\text{rank}(R)=m$
   This implies that, for some set of vectors in $\mathbb{R}^{m}$, there exists $\text{rank}(R)$ linearly independent basis vectors present; that is $\text{rank}(R)\implies \mathbb{R}^{r}$ column space. If $\mathbb{R}^{r}=\mathbb{R}^{m}$, then our space fully spans the space that the vectors are present in; thus all solutions are consistent. 
4. $\text{rank}(R)<m$
   This implies that, for some set of vectors in $\mathbb{R}^{m}$ if $\text{rank}(R) \implies \mathbb{R}^{r}$, then $\mathbb{R}^{r} < \mathbb{R}^{m}$, that is, the corresponding column space spanned by our matrix is less than the dimension of the space that our vectors exist in. 
	   In terms of RREF, This implies that, there exists at least *one* zero row. 
   Thus, this implies that there may exist values in $\mathbb{R}^{m}$ which may not be in the space defined by $\mathbb{R}^{r}$, that is there *may* exist inconsistent solutions. 

Then: 

|                                                  | $r=n$ Unique Solution                                | $r<n$ Infinitely Many Solutions                            |
| ------------------------------------------------ | ---------------------------------------------------- | ---------------------------------------------------------- |
| $r =m$<br>Solutions are always consistent        | One unique solution exists.                          | Infinitely many consistent solutions exist.                |
| $r<m$<br>Solutions may not always be consistent. | No solution exists<br>OR one unique solution exists. | No solution exists.<br>OR, infinitely many solution exist. |


## Determining Systems 
We can relate the type of system, with the corresponding properties of some matrix $A$. Note that $\text{rank}(A)$ can be defined as: 
1. The amount of linearly independent column vectors in A. 
	1. The dimension of the column space.
2. The number of pivot / leading variables. 

---
# Pre-Lecture Notes
## Gaussian Elimination Solutions
When Considering the potential cases in Gaussian Elimination, we generally have *three* sets of possibilities pertaining to the resulting solution. 
1. If all columns are defined by a leading one (that is, there exists no free variables / $A$ is linearly independent), then we say that a *unique, consistent* solution exists. 
2. If free variables are present (that is, there exists columns not defined by a leading one), then we say that a *consistent, but infinite* number of solutions exist. 
3. If an inconsistent solution arises (e.g. $0=1$ in one of our rows), then we state that this is inconsistent, and that no solution exists.
	1. Geometrically, this means that for some $A\vec{x}=\vec{b}$ where this is the case, $\vec{b}\not\in A$'s column space. 

Consider that we can also extend this to our previously defined concept of $\text{rank}(A)$. Recall that $A$ represents some $m\times n$ matrix, then: 
* $\text{rank}(A) =m$, then our system is fully consistent, as this states that for any vector in $\mathbb{R}^{m}$, some linear combination of our corresponding column vectors present in our matrix where this resolves to $\vec{b}$ in $\mathbb{R}^{m}$. 
* $\text{rank}(A)<m$, then our system may not be fully consistent, some $\vec{b}$ may not be in the column space of $A$. 
* $\text{rank}(A)=n$, then our system is fully composed of pivot variables (that is, full linear independence), thus **one unique solution exists**. 
* $\text{rank}(A)<n$, then our system may have one or more free variables, then multiple solutions may concurrently exist (i.e. non-existence of unique solution). 

### Rank-Nullity
Consider that for a matrix $A$ of some size $m\times n$, we can see that for some given rank, this corresponds to the number of linearly independent vectors present in $A$, and thus the corresponding amount of pivot variables; that is $\text{rank}(A)=r$. For this system then, the corresponding number of free variables is given to us by the expression of $n-r$; and we note this corresponds to the nullity of a system; thus: 
$$
\begin{align}
r + n - r  & = n  \\
\text{rank}(A)+\text{nullity}(A) & =n
\end{align}
$$
Which is what we define as the Rank-Nullity Theorem as Desired.