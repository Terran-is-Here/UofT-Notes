---
updated_at: 2026-11-02T12:37:04.082-05:00
edited_seconds: 320
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 13
Lecture Date: 2026-11-02
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[12 — Elementary Row Operations]]
Next: [[14 — Gaussian Elimination]]

--- 
# Lecture Notes
## Solving Systems
Recall that we can solve a system of equations as a matrix, and that we can apply elementary row operations to solve such a system. Consider the following system of equations then: 
$$
\begin{align}
x_{1} + 2x_{2} + x_{3}  & =0 \\
2x_{1} + 4x_{2} + 5x_{3} & =0  \\
3x_{1} + 6x_{2} + 4x_{3} & =0
\end{align}
$$
Or, as a matrix: 
$$
\begin{bmatrix}
1 & 2 & 1 \\
2 & 4 & 5 \\
3 & 6 & 4
\end{bmatrix}
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix}
= \begin{bmatrix}
0\\0\\0
\end{bmatrix}
$$
Recall, we can solve this in terms of $A=CR$, then from here we can solve $R\vec{x}=0$ as previously: 
$$
\begin{bmatrix}1 & 2 & 1 \\2 & 4 & 5 \\3 & 6 & 4\end{bmatrix} = \begin{bmatrix}
1 & 1 \\
2 & 5 \\
3 & 4
\end{bmatrix} \begin{bmatrix}
1 & 2 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

We can actually instead use elementary row operations to solve such a system instead. We intend to use EROs to get to $R_{0}$ (something very similar to $R$), we can do this trivially: 
$$
\begin{align}
\begin{bmatrix}
1 & 2 & 1 \\
2 & 4 & 5 \\
3 & 6 & 9
\end{bmatrix}  &  & R_{2}-2R_{1} \\
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 3 \\
3 & 6 & 9
\end{bmatrix} &  & R_{3}-3R_{1} \\
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 3 \\
0 & 0 & 6
\end{bmatrix}  &  & R_{3} - 2R_{2} \\
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 3 \\
0 & 0 & 0 
\end{bmatrix} &  & \frac{1}{3}R_{2} \\
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{bmatrix} &  & R_{1}-R_{2} \\
R_{0}=\begin{bmatrix}
1 & 2 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0 
\end{bmatrix}
\end{align}
$$

The matrix here is termed as the RREF form of $R$, as this is equivalent to $R$ with an extra row of 0 at the bottom. 
## RREF Matrices 
RREF (Reduced-Row Echelon Form) Matrices follow the properties below: 
1. The first non-zero entry in a row is a $1$ (leading ones).
2. All entries within a column with a leading one must be 0. 
3. All leading ones are to the right of the one above them. 
4. Any and all rows fully compromised of 0s are collected at the bottom of the matrix. 

Then with our above matrix, note that since we are solving for it equals to $0$, then we find that: 
$$
\begin{bmatrix}
1 & 2 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{bmatrix}\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix}=\begin{bmatrix}
0\\0\\0
\end{bmatrix}
$$
Then this is equivalent to: 
$$
x_{1}+2x_{2} = 0\\
x_{3}=0
$$
Then setting $x_{2}$ as the free variable, then: 
$$
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix} = \begin{bmatrix}
-2\\1\\0
\end{bmatrix}x_{2}
$$
Where this like represents the null space of $A$; or in other words, $\text{nullity}(A)=1$
> Generally, we can see that the column *whithout a leading one* represents a free variable (as they aren't fully fixed to a certain desired value). 
---
# Pre-Lecture Notes

## Forward Elimination
Forward Elimination *refers* to **the series** of elementary row matrices $E_{u}=E_{i}E_{i-1}\dots E_{1}$ multiplied to turn a matrix $A$ into an upper-triangular matrix $U$, that is $E_{u}A=U$; Recall that an upper triangular matrix refers to where all the entries **below** the diagonal entries equals zero. 

Note that with $A\vec{x}=0$, we know that for any matrix $E_{u}$, or even $M$, that $M 0 = 0$; thus $A\vec{x}=0$'s solution set for $\vec{x}$ is equivalent to $U\vec{x}=0$. Note that the position we multiply things with respect to matters; though at this point you should have enough ERO practice in order to perform this seamlessly. 

## Backwards Substitution
After obtaining some upper-triangular matrix $U$, we can perform *backwards substitution* in order to obtain some $R_{0}$ (otherwise known as the Row-Reduced Echelon Form) of $A$. A matrix in RREF requires the following characteristics: 
1. The first non-zero entry in each row **must** be one. 
2. Each leading one **must** be to the right of all leading ones above it. 
3. All other entries in the same column as a leading one must be 0. 

To get a matrix $U\to R_{0}$, we perform another set of EROs; note that we often term the leading terms the "pivot points", and the non-leading terms as potential free variables. The number of leading pivot points represents the number of linearly independent vectors within the space (and by extension, the corresponding nullity from the rank-nullity theorem).


