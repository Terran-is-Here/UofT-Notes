---
updated_at: 2026-09-14T12:40:55.308-04:00
edited_seconds: 740
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 1
Date: 2026-09-10
Week: 0
Created: September 8th 2026, 2:57:08 pm
---
Hub: [[ESC103 Hub]]
Next: [[02 —Vector Dot Product]]
See also: [[2 — Vectors (Physics)]]

--- 

## Vectors & Scalars
> We only have the unit definition; as we *are* in engineering; and any physical quantity should have dimensions/units. 

Recall that Scalars are defined as a value with magnitude; a **sign** and units—whilst vectors are defined as values with magnitude, **direction** and units. 

* Scalars can be represented as simple values such as $2$.
* Vectors can comparatively be represented in a wider variety of methods; such as component, polar, or the linear combination of two other vectors. 

A vector's dimensions can be expressed as the number of values they take within it's component form; for instance, let $\vec{CD}$ and $\vec{AB}$ be vectors; we can define them as: 
$$
\vec{AB} = \begin{pmatrix}
1\\2
\end{pmatrix}
$$
$$
\vec{CD} = \begin{pmatrix}
1&2&3
\end{pmatrix}
$$
In this case; $\vec{AB}$ is a 2d vector; while as $\vec{CD}$ is a 3d vector. Note that $\vec{AB}$ is a ***column vector*** and $\vec{CD}$ is a ***row vector***. **These are distinct with each other** (more accurately being the Transpose of each other.) **Column Vectors and Row Vectors are fundamentally different**. 
> Let $\vec{AB}$ be a row vector; $$\vec{AB} = \begin{pmatrix}a_{1}&a_{2}\end{pmatrix}$$
> We can find it's corresponding Column vector by taking it's transpose (swapping all rows with columns): $$\vec{AB}^T = \begin{pmatrix}a_{1} & a_{2}\end{pmatrix}^T=\begin{pmatrix}a_{1}\\a_{2}\end{pmatrix}$$
### Special Vectors
> [!theorem] $\vec{0}$
> The Zero Vector (denoted as $\vec{0}$) is defined as having all of it's components be equal to 0: 
> $$\vec{a} = \vec{v} - \vec{v} = \begin{pmatrix}0\\0\end{pmatrix}$$

> [!theorem] Unit Vectors
> A unit vector (defined as $\hat{a}$; generally a letter with a "hat" is a unit vector) is defined as a vector with it's magnitude set to 1. Recall how we can find this. 
> Let $\vec{a}$ be a vector in $\mathbb{R}$; then $$\hat{a} = \frac{\vec{a}}{||\vec{a}||}$$

## Linear Combinations
A Linear Combination is defined as the well; linear combinations of two vectors which can describe another vector; generally of the form of: 
$$
c\vec{a} + d\vec{b} = \vec{R}
$$
Where $\vec{a}$ and $\vec{b}$ are vectors, and $c,d\in \mathbb{R}$. 

> [!theorem] Vector Spaces
> A Vector Space is defined as the set of **all possible linear combinations of a set of vectors.** 
> Essentially; all vectors that could be *expressed* as *any* linear combinations of *these* vectors.
> 
> Note that not all vector spaces can map to any vector; these are defined per every vector. This mainly applies to if both $\vec{a}$ and $\vec{b}$ can be expressed as a term of each other (e.g. $\vec{a} = 2\vec{b}$); in which case your vector space would be a line. 
> 

Note that a Linear Combination can be fully extended to any number of vectors; simply by adding another vector term and a corresponding scalar term. 
### Vector Properties
Vectors follow the same three main principles present with the [[02 — The Real Number System|field axioms of the real number system]], that being Commutativity, Associativity, and (Scalar) Distributivity:

> [!theorem] Commutativity
> $$\vec{a}+\vec{b} = \vec{b} + \vec{a}$$
> Geometrically follows from the parallelogram interpretation of vector addition. 

> [!theorem] Associativity
> $$(\vec{a} + \vec{b}) + \vec{c} = \vec{a} + (\vec{b} + \vec{c})$$
> 

> [!theorem] Scalar Distribution*
> $$a_{1}\vec{C} = a_{2}\vec{C} = (a_{1}+a_{2})\vec{C}$$

## Simple Vector Operations
Vector operations are generally defined under the following concepts below: 

### Addition & Subtraction
> Given $\vec{a}=\begin{pmatrix}a_{1}\\a_{2}\end{pmatrix}$ and $\vec{b} = \begin{pmatrix}b_{1}\\b_{2}\end{pmatrix}$, Addition and subtraction are algebraically defined as the following lines below: 
>  $$\vec{a} + \vec{b} = \begin{pmatrix}a_{1}+b_{1}\\a_{2}+b_{2}\end{pmatrix}$$
>   $$\vec{a} - \vec{b}=\vec{a} + (-\vec{b}) = \begin{pmatrix}a_{1}-b_{1}\\a_{2}-b_{2}\end{pmatrix}$$
>   Geometrically; these are defined by the Parallelogram Model (or whatever; you should remember this). **Vector Addition and Subtraction is always Tail to Head**. 
> > Subtraction for this case would be us equivalently flipping $-\vec{b}$; then adding it as normal.

### Scalar Multiplication & Division
> Given $\vec{a} = \begin{pmatrix}a_{1}\\a_{2}\end{pmatrix}$, and $b$ is a scalar value; then Scalar Multiplication is defined as the following: 
> $$\vec{a}*c = \begin{pmatrix}a_{1}*c\\a_{2}*c\end{pmatrix}$$
> Division is also similarly defined: 
> $$\frac{\vec{a}}{c} = \vec{a}* \frac{1}{c}=\begin{pmatrix} \frac{a_{1}}{c}\\ \frac{a_{2}}{c}\end{pmatrix}$$

### Vector Magnitude 
> Recall that a vector's magnitude can be calculated through the Pythagorean Theorem. Let $\vec{a} \in\mathbb{R}^3$, $\vec{a} = \begin{pmatrix}a_{1}&a_{2}&a_{3}\end{pmatrix}$, then $||\vec{a}|$ is represented as: 
> $$||\vec{a}|| = \sqrt{  a_{1}^2+a_{2}^2+a_{3}^3}$$
> In general for any $n$ dimensional vector in R; that is $\vec{b} \in \mathbb{R}^n$; and $\vec{a} = \begin{pmatrix}a_{1}&a_{2}&\dots&a_{n}\end{pmatrix}$: 
> $$||\vec{a}|| = \sqrt{ \sum^n_{{i=1}}a_{i}^2 }$$
