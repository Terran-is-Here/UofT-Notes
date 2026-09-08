---
updated_at: 2026-09-08T15:24:58.217-04:00
edited_seconds: 360
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 1
Date: 2026-09-10
Week: 0
---
Previous: N/A
Next: N/A 

--- 

## Vectors & Scalars
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
In this case; $\vec{AB}$ is a 2d vector; while as $\vec{CD}$ is a 3d vector. Note that $\vec{AB}$ is a *column vector* and $\vec{CD}$ is a row vector.
### Special Vectors
* The Zero Vector (denoted as $\vec{0}$) is defined as having all of it's components be equal to 0. 
* A unit vector (defined as $\hat{a}$; generally a letter with a "hat" is a unit vector) is defined as a vector with it's magnitude set to 1. Recall how we can find this. 
	* Let $\vec{a}$ be a vector in $\mathbb{R}$; then $$\hat{a} = \frac{\vec{a}}{||\vec{a}||}$$

## Linear Combinations
A Linear Combination is defined as the well; linear combinations of two vectors which can describe another vector; generally of the form of: 
$$
c\vec{a} + d\vec{b} = \vec{R}
$$
Where $\vec{a}$ and $\vec{b}$ are vectors. 
> [!info] Definition
> A Vector Space is defined as the set of all possible linear combinations of a set of vectors. 
## Simple Vector Operations
Vector operations are generally defined under the following concepts below: 

### Addition & Subtraction
> Given $\vec{a}=\begin{pmatrix}a_{1}\\a_{2}\end{pmatrix}$ and $\vec{b} = \begin{pmatrix}b_{1}\\b_{2}\end{pmatrix}$, Addition and subtraction are defined as the following lines below: 
>  $$\vec{a} + \vec{b} = \begin{pmatrix}a_{1}+b_{1}\\a_{2}+b_{2}\end{pmatrix}$$
>   $$\vec{a} - \vec{b} = \begin{pmatrix}a_{1}-b_{1}\\a_{2}-b_{2}\end{pmatrix}$$

### Scalar Multiplication & Division
> Given $\vec{a} = \begin{pmatrix}a_{1}\\a_{2}\end{pmatrix}$, and $b$ is a scalar value; then Scalar Multiplication is defined as the following: 
> $$\vec{a}*c = \begin{pmatrix}a_{1}*c\\a_{2}*c\end{pmatrix}$$
> Division is also similarly defined: 
> $$\frac{\vec{a}}{c} = \vec{a}* \frac{1}{c}=\begin{pmatrix} \frac{a_{1}}{c}\\ \frac{a_{2}}{c}\end{pmatrix}$$

### Vector Magnitude 
> Recall that a vector's magnitude can be calculated through the Pythagorean Theorem. Let $\vec{a} \in\mathbb{R}^3$, $\vec{a} = \begin{pmatrix}a_{1}&a_{2}&a_{3}\end{pmatrix}$, then $||\vec{a}|$ is represented as: 
> $$||\vec{a}|| = \sqrt{  a_{1}^2+a_{2}^2+a_{3}^3}$$
> In general for any $n$ dimensional vector in R; that is $\vec{b} \in \mathbb{R}^n$; and $\vec{a} = \begin{pmatrix}a_{1}&a_{2}&\dots&a_{n}\end{pmatrix}$: 
> $$||\vec{a}|| = \sqrt{ \sum^n_{{i=0}}a_{i}^2 }$$
