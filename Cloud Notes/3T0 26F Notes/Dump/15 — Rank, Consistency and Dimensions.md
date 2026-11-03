---
updated_at: 2026-11-03T17:46:53.696-05:00
edited_seconds: 610
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 15
Lecture Date: 2026-11-03
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[14 — Gaussian Elimination]]
Next: N/A

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
Which is what we define as the Rank-Nullity Theorem as Desired.)