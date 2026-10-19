---
updated_at: 2026-10-19T12:55:26.714-04:00
edited_seconds: 1600
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 11
Lecture Date: 2026-10-09
Week: 6
---
Hub: [[ESC103 Hub]]
Previous: [[10 — Matrix Multiplication]]
Next: [[12 — Elementary Row Operations]]

> [!quote] Learning Objectives 
> * Construct a matrix $\mathbf{C}$ from matrix $\mathbf{A}$ using the definition of independent vectors. 
> * Construct a matrix $\mathbf{R}$ such that $\mathbf{A}=\mathbf{CR}$
> * Explain the significance of $\mathbf{R,C}$ with respects to $\mathbf{A}$

> [!quote] Recommended Reading 
> [[08 — Matrix Vector Products]], and [[09— Basic Linear Algebra Concepts]] are also useful for this section as they pop up again and again. 

> [!ila] Lecture Summary
> $\mathbf{A=CR}$
> * $\mathbf{C}$ contains $r$ independent columns of $\mathbf{A}$. 
> * $r$ is the rank of matrix $\mathbf{A}$. 
> * $\mathbf{R}$ tells us how we should modify $\mathbf{C}$ to obtain $\mathbf{A}$
--- 
 
# Lecture Notes
## Matrix Decomposition
The general concept of Matrix Decomposition, is that given some matrix $\mathbf{A}$, we should be able to express this as a product of two matrices $\mathbf{C,R}$; that is: 
$$
\mathbf{A}= \mathbf{C}\mathbf{R}
$$
The concept is that we can break up some $\mathbf{A}$ (which could be complex) into two simpler matrices $\mathbf{C,R}$. We do this to try and make some matrices much easier to compute. 

> [!theorem] Constructing $\mathbf{C}$ from $\mathbf{A}$ (where $A$ is a $m\times n$ matrix) 
> We want to construct our matrix $\mathbf{C}$ with solely the linearly independent columns of $\mathbf{A}$, or in other words, the basis column vectors of a matrix $\mathbf{A}$. 
> For instance: 
> $$\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix}$$Factoring this above requires us to note which columns are linearly independent. 
> 1. If column 1 of $\mathbf{A}$ is not $\vec{0}$, put the first column in $\mathbf{C}$. 
> 2. If column $n$ of $\mathbf{A}$ is not some multiple / scalar combination of the currently present columns, put column two into $\mathbf{C}$. Otherwise, skip. 
> 	1. In lecture, this was written as "if column two of A is not some multiple of column 1, then put column 2 in c, otherwise skip."
> 3. Repeat step 2 until all $\mathbf{A}$ have been iterated over. 
> 
> Thus, for our matrix above; then $\mathbf{C}$ per step is: 
> $$\begin{bmatrix}2\\4\\1\end{bmatrix} \to \begin{bmatrix}2\\4\\1\end{bmatrix} \to \begin{bmatrix}2 & 4 \\4 & 8 \\1 & 5\end{bmatrix}$$
> > Note then, that $\mathbf{C}$ should have $r$ columns; where $r\leq n$, and all column vectors inside are linearly independent. 
> > > In this case, the column space of $\mathbf{A}$ is equal to the column space of $\mathbf{C}$; that is the column vectors of $\mathbf{C}$ are the basis vectors of the column space of $\mathbf{A}$
> > > And $r$ represents the rank of $\mathbf{C}$, which represents the rank of $\mathbf{A}$. 
> 
> Note that for a big matrix $\mathbf{A}$, checking the linear independence of all of it's corresponding column vectors may be computationally intensive. 

> [!theorem] Constructing $\mathbf{R}$ from $\mathbf{C}$
> Retaking our example matrix: $$\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix}$$
> Note from the above step; that $\mathbf{C} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}$
> We now need to solve this:$$\mathbf{A} = \begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}\mathbf{R} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}\begin{bmatrix}a & d & f\\b & e & g\end{bmatrix}$$
> Note that since $\mathbf{A}=3\times 3$, $\mathbf{C}=3 \times 2$, then $\mathbf{R}$ must have dimensions of $2 \times 3$; since $3\times 2 * 2 \times 3 \implies 3 \times 3$. The question then arises; what are the values of $\mathbf{R}$? 
> Let's solve this piece by piece: Note that $\begin{bmatrix}a\ \\  b\end{bmatrix}$ is a vector in $\mathbf{R}$; then note that : 
> $$\begin{bmatrix}2 & 4 \\4 & 8  \\1 & 5\end{bmatrix} \begin{bmatrix}a\\b\end{bmatrix} = \begin{bmatrix}2\\4\\1\end{bmatrix}$$
> Then: $$\begin{align}2a+4b  & = 2 \to a=1\\4a + 8b  & = 4 \to b=0 \\1a + 5b  & = 1\end{align}$$
> But, recall; that matrix vector products are also linear combinations in column view: $$\begin{bmatrix}2\\4\\1\end{bmatrix}a  + \begin{bmatrix}4\\8\\5\end{bmatrix}b = \begin{bmatrix}2\\4\\1\end{bmatrix} \implies a=1,b=0$$
> Repeating this process for $\begin{bmatrix}f\\ g\end{bmatrix}$, this must be $\begin{bmatrix}0\\1\end{bmatrix}$.
> Now for $\begin{bmatrix}d\\ e\end{bmatrix}$, then: $$\begin{bmatrix}2\\4\\1\end{bmatrix}d  + \begin{bmatrix}4\\8\\5\end{bmatrix}e = \begin{bmatrix}6\\12\\3\end{bmatrix} \implies d=3,b=0$$
> Thus $\mathbf{R} = \begin{bmatrix}1 & 3 & 0 \\  0 & 0 & 1\end{bmatrix}$.

From the steps above, we have factored $\mathbf{A}$ to the following: 
$$\mathbf{A} = \mathbf{CR} = \begin{bmatrix}2 & 4 \\4 & 8  \\1 & 5\end{bmatrix}\begin{bmatrix}1 & 3 & 0 \\0 & 0 & 1\end{bmatrix}$$
> [!caution]
> To find the $i$-th column of $\mathbf{R}$, take the $i$th column of $\mathbf{A}$, and express it as a linear combination of the column vectors present within $\mathbf{C}$. 

> [!ila] Important Idea
> In other words, $\mathbf{C}$ give us the tools, and $\mathbf{R}$ give us the instructions that we need to construct the corresponding matrix of $\mathbf{A}$. 

## Solving Homogenous Vectors 
Take the following: 
$$
\begin{align}
\mathbf{A}\vec{x}  & = \vec{0} \\
\mathbf{CR}\vec{x}  & = \vec{0}  & \text{Using associative property: } (\mathbf{AB})\mathbf{C} = \mathbf{A}(\mathbf{BC}) \\
\mathbf{C}(\mathbf{R})\vec{x} & =\vec{0}
\end{align}
$$
Note that $\vec{x}=\vec{0}$ is always a solution to this system; however the question is now "does there exist any other $\vec{x}$ where this results in $\vec{0}$"? 

To start, let's take the example where $\mathbf{A}$ has linearly independent column vectors; such as: 
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & -2 & 7 \\
0 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix}=
\begin{bmatrix}
0\\0\\0
\end{bmatrix}
$$
Note that since $\mathbf{A}$'s column space are linearly independent; then the only linear combination of the column vectors are when the scalars are 0. Note that since the column vectors for $\mathbf{A}$ is linearly independent, then in $\mathbf{CR}$: 
$$
\begin{bmatrix}1 & 0 & 0 \\0 & -2 & 7 \\0 & 1 & 5\end{bmatrix}\begin{bmatrix}1 & 0 & 0 \\0 & 1 & 0 \\0 & 0 & 1\end{bmatrix}\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}
\end{bmatrix} = \vec{0} \iff \vec{x}=0
$$

Consider now a non-linearly independent matrix: take the following matrix: 
$$
\begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix}
$$
Factoring this into $A=CR$, then: 
$$
\begin{bmatrix}2 & 6 & 4 \\4 & 12 & 8 \\1 & 3 & 5\end{bmatrix} = \begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}\begin{bmatrix}
1 & 3 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
Applying this to $\mathbf{A}=CR \implies C(R\vec{x})=0$: 
$$
\begin{bmatrix}2 & 4\\4 & 8\\1 & 5\end{bmatrix}\begin{bmatrix}
1 & 3 & 0 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = \vec{0}
$$
Note that now, recall that for a set of linearly independent vectors $C$, or in our case, the Column vector is linearly independent. Thus, the only way that is $\vec{0}$ is if we can equate $R\vec{x}=0$; then: 
$$\begin{bmatrix}1 & 3 & 0 \\0 & 0 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}=\vec{0}$$
Or in other words, $R\vec{x}=0$ and $A\vec{x}=0$ both share the same set of solutions $\vec{x}$. Thus, taking this from the column picture; this can be trivially solved: 
$$
\begin{bmatrix}1\\0\end{bmatrix}x_{1} + \begin{bmatrix}3\\0\end{bmatrix}x_{2} + \begin{bmatrix}0\\1\end{bmatrix}x_{3} = \begin{bmatrix}0\\0\end{bmatrix}
$$
$x_{1}=-3x_{2}$, $x_{2}=x_{2}=t$, $x_{3}=0$, then we get $\vec{x}=t\begin{bmatrix}-3\\1\\0\end{bmatrix}$; or in other words, the set of solutions is of the form of a line with a span of $\mathbb{R}^1$ (or in other words, our system has a nullity of 1). We can change $x_{2}=t$, as we can define it as our free variable (as it is not natively dependent on any other terms of the expression) We now arise at some other definitions: 

> A free variable is a variable freely defined as any value.
> A leading(pivot) variable is a variable dependent on some free variable (for our case, $x_{1},x_{3}$). 

Note that a free variable can be set well, freely. the pivot variables need only to be defined as some term of the leading variable. 

> [!theorem] Null space (tut) 
> The null space of a matrix $\mathbf{A}$ is the set of solutions of $\vec{x}$ in $\mathbf{A}\vec{x}=\vec{0}$. 
> > The *dimension* of a null space is otherwise notated as nullity. Or in other words, the amount of linearly-independent basis vectors within the null space. 

Note that for our expression of linearly independent basis vectors from above, we define it's nullity() as 0. 

Take now the following example: 
$$
\mathbf{A_{3}}=  \begin{bmatrix}2 & 3 & -4 \\1 & \frac{3}{2} & -2 \\4 & 6 & -8\end{bmatrix}=
\begin{bmatrix}2\\1 \\4\end{bmatrix}\begin{bmatrix}
1 & \frac{3}{2}-2
\end{bmatrix}
$$
Then solving for $R\vec{x}=0$: 
$$
x_{1} + \frac{3}{2}x_{2} + -2x_{3} = 0
$$
Note that for any combination of $x_{1},x_{2},x_{3}$ works for this combination. Thus, this is actually a *plane* in R3 (or, a Hyperplane in $\mathbb{R}^3$ ). For our case, declare $x_{2},x_{3}$ as free variables; then we can solve for an expression of $x_{1}$: 
$$
\begin{align}
x_{1}=-\frac{3}{2}x_{2} + 2x_{3} \\
x_{2}=x_{2} \\
x_{3}=x_{3}
\end{align}
$$
Then, in a vector form: 
$$
\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = \begin{bmatrix}
-\frac{3}{2}\\1\\0
\end{bmatrix}x_{2} + \begin{bmatrix}
2\\0\\1
\end{bmatrix}x_{3}
$$
We denote the two column vectors here as the two special solutions; all other solutions for $x_{1},x_{2},x_{3}$ are linear combinations of these two; or in other words, a vector that lies on the plane defined by these two matrices. 

Note that we can relate the concept of nullity with the rank of the original matrix, consider a matrix with $\text{rank}(\mathbf{A})=3$ (or for above; we know that for a matrix with all linearly independent vectors, the sole solution is the origin), thus $\text{nullity}(\mathbf{A})=0$

Consider now a matrix with 2 linearly independent columns and one dependent column; then we have $\text{rank}(\mathbf{A_{2}})=2$ and $\text{nullity}(A_{2})=1$. 

Conversely, for the one we just did; we have $\text{rank}(A_{3})=1$ and $\text{nullity}(A_{3})=2$. There's a clear pattern in here; this is defined by the Rank Nullity Theorem: 

> Rank Nullity Theorem
> $$\text{rank}(A) + \text{nullity}(A) = n$$
> Where $n$ represents the number of columns within a matrix; or in other words, the number of variables present. Thus, the rank of a variable represents the number of pivot variables, while nullity represents the number of free variables present in solutions to a system. 

We can apply solving systems of linear equations as the result of a chemical reaction; though that is beyond the scope of this note and is thus left as a future thing to read. i guess. 

---
# Pre-Lecture Notes
## CR Matrices 
Given the following matrix: 
$$
\mathbf{A} = \begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix}
$$
A matrix $\mathbf{C}$ can be created from the linearly independent columns of $\mathbf{A}$: 
$$\mathbf{C} = \begin{bmatrix}1 & 4 \\3 & 2 \\0 & 2\end{bmatrix}$$
Note; that $\begin{bmatrix}7\\11\\2\end{bmatrix} = 3\begin{bmatrix}1\\3\\0\end{bmatrix}+ 1\begin{bmatrix}4\\2\\2\end{bmatrix}$, That is to say that this matrix is *linearly* dependent. Then we can express the matrix $\mathbf{R}$ as the following matrix: 
$$
\mathbf{R} = \begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & 1
\end{bmatrix}
$$
Where: 
$$
\begin{bmatrix}1 & 4 & 7 \\3 & 2 & 11 \\0 & 2 & 2\end{bmatrix} = \begin{bmatrix}1 & 4\\3 & 2\\0 & 2\end{bmatrix}\begin{bmatrix}1 & 0 & 3\\0 & 1 & 1 \end{bmatrix}
$$
Recall that matrix multiplication **always** works in a row-column arrangement. That is; we iterate through rows of $\mathbf{A}$ before iterating through columns of some $\mathbf{B}$ in $\mathbf{AB}$. 
> [!ila] Important Idea
> Note that the Column Vectors of $\mathbf{C}$ are the basis vectors of the column space of $\mathbf{A}$, or in other words; they represent the linearly independent vectors in $\mathbf{A}$ (and thus it's corresponding rank and dimensions).
> 

### Significance of R
Note however that the matrix $\mathbf{R}$ is something special: it is the Row-Reduced Echelon Form of $\mathbf{A}$; though it's kind of outside the bounds of this note for now to work on it. 

## Solving Homogenous Systems
> [!caution] Note
> This section is *technically* meant for next lecture, though I wouldn't be surprised if it's not mentioned in this lecture. Will edit in the future if it is moved to a future lecture. 

> [!ila] In Lecture Addendum
> This was previously keyed as solving Ax=0 using A=CR, however this is now termed as solving Homogenous Systems. 
> 
> A homogenous system is any system of the form $\mathbf{A}\vec{x}=\vec{0}$. 


A = CR provides us a useful tool for solving our previous $\mathbf{A}\vec{x} = \vec{b}$ equations that we have tackled in the past in a bit more of an algebraic method. Take the following matrix: 
$$
\mathbf{A}=\begin{bmatrix} 
1 & 3 \\
2 & 3 \\
1 & 3
\end{bmatrix} = \begin{bmatrix}1 & 3\\2 & 3\\1 & 3\end{bmatrix}\begin{bmatrix}
1 & 0\\0 & 1\end{bmatrix}
$$
That is, the corresponding $\mathbf{R}=\mathbf{I}$ and $\mathbf{C}=\mathbf{A}$. We know that the span of $\mathbf{A}$ is entirely composed of linearly independent vectors then: 
$$
\begin{bmatrix}1 & 3\\2 & 3\\ 1 & 3\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\end{bmatrix} = \begin{bmatrix}0\\0\\0\end{bmatrix}
$$
The only solutions to this are if $\vec{x}=\vec{0}$. 

However, now consider the following linearly dependent matrix: 
$$
\begin{bmatrix}1 & 3 & 5 \\2 & 3 & 7 \\1 & 3 & 5\end{bmatrix} = \begin{bmatrix}1 & 3 \\2 & 3\\1 & 3\end{bmatrix}\begin{bmatrix}1 & 0 & 2 \\0 & 1 & 1\end{bmatrix}
$$
Now broken up into some $\mathbf{A=CR}$; then resubstituting this into $\mathbf{A}\vec{x}=\vec{0}$: 
$$
\begin{bmatrix}1 & 3\\2 & 3\\ 1 & 3\end{bmatrix}\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}=\begin{bmatrix}0\\0\\0\end{bmatrix}
$$
Note that $\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix}$ Results in some vector $\begin{bmatrix}b_{1}\\b_{2}\end{bmatrix}$ (we lose a row in $\mathbf{R}$ over $\mathbf{A}$). Since $\begin{bmatrix}1 & 3\\2 & 3\\1 & 3\end{bmatrix}$ is linearly independent; taking our case above; then the only way this equals 0, is if it's multiplied by 0. 
Or in other words: 
$$
\begin{bmatrix}1 & 0 & 2\\0 & 1 & 1\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = \vec{0}
$$
Thus: 
$$
x_{1}\begin{bmatrix}1 \\0\end{bmatrix} + x_{2}\begin{bmatrix}0\\1\end{bmatrix} + x_{3}\begin{bmatrix}2\\1\end{bmatrix} = \begin{bmatrix}0\\0\end{bmatrix}
$$
$$
x_{1}\begin{bmatrix}1 \\0\end{bmatrix} + x_{2}\begin{bmatrix}0\\1\end{bmatrix} = -x_{3}\begin{bmatrix}2\\1\end{bmatrix}
$$
Note that the solution of this now; is: 1
$$
\begin{align}x_{1}=-2x_{3} \\x_{2}=-x_{3}\end{align}
$$
We can *parameterize* $x_{3}$ (or in other words, it is the *free* variable) to some value $t$, and then the corresponding systems of equations pop out: 
$$
\begin{align}
x_{1}&=-2t \\
x_{2}&=-1t \\
x_{3}&=t
\end{align}
$$
Which then implies 
$$\begin{bmatrix}x_{1}\\x_{2}\\x_{3}\end{bmatrix} = t\begin{bmatrix}-2\\-1 \\1\end{bmatrix}$$
As the solution to our above expression of $\mathbf{A}\vec{x}=\vec{0}$. Note that this entire expression leads us to two more core definitions for Linear Algebra: 
> [!theorem] Nullspace/Kernel
> The **nullspace** (otherwise known as the Kernel) of some matrix $\mathbf{A}$ is the vector space for the solution of $\vec{x}$ in $\mathbf{A}\vec{x}=\vec{0}$. 

> [!theorem] Nullity
> **Nullity** is the *Dimension* of the null space; that is it's corresponding amount of basis vectors. 


