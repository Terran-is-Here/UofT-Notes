---
updated_at: 2026-09-23T22:20:20.380-04:00
edited_seconds: 740
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 5
Lecture Date: 2026-09-22
Week: 3
created:
Created: September 18th 2026, 12:16:18 pm
---
Hub: [[ESC103 Hub]]
Previous: [[04 — Vector Cross Product]]
Next: [[06 — Solving Linear Equations]]
Tutorial: [[T2 - ESC103 Tutorial 2]]

--- 

# Lecture Notes
The general goal of this segment is to be able to define geometric shapes *as* equations, such as a line in $\mathbb{R}^2$ being defined as a scalar equation. Or more specifically, we seek to define the relationships of a value of $x$ to $y$ to describe a geometric object. 

Generally, for two lines / planes intersect, we want to figure out where they geometrically meet (duh) 
## Equation of a Line 
Recall the simplest *scalar* equation that we had for a line in $R^2$: 
$$y=mx+b$$
For the vector equation of this line, refer to the definition we defined below ([[05 — Equations of Lines and Planes#^R3VectorEquation|Linked Here]]). What this equation generally means is that *all the points on the line* can be described by it's following relation. 

For lines in $\mathbb{R}^2$, this can be be defined by simply removing our $z_{0}$ term: 
$$\begin{bmatrix}x \\y\end{bmatrix} = \begin{bmatrix}x_{0} \\y_{0}\end{bmatrix}+a\begin{bmatrix}d_{1} \\d_{2}\end{bmatrix}$$
Note our direction vector can be defined in terms of the slope of our line, and we can define our initial point in terms of some vertical translation from the origin; that is: 
$$\begin{bmatrix}x \\y\end{bmatrix} = \begin{bmatrix}0 \\b\end{bmatrix}+a\begin{bmatrix}1 \\m\end{bmatrix}$$
This resolves down to the familiar scalar equation of the line that we know. 
### Hyperplanes
We can extend our concepts of lines and planes and vectors into $\mathbb{R}^m$ dimensional space: 
$$
\vec{n} = \begin{bmatrix}n_{1} \\n_{2} \\\vdots \\n_{m}\end{bmatrix}
$$
We can define the concept of a "hyperplane", that is $\vec{x}\cdot \vec{n}=0$ as a vector equation holds true. This means that $\forall \vec{x}\perp \vec{n}$. We can reuse the definition that we had in the prenotes, ergo: 
$$
n_{1}x_{1} + n_{2}x_{2} + \dots + n_{m}x_{m} = 0
$$
Where this is the scalar equation of the plane, equivalent to: 
$$
\vec{n} \cdot \vec{x} = \begin{bmatrix}n_{1} \\n_{2} \\\vdots \\n_{m}\end{bmatrix} * \begin{bmatrix}x_{1} \\x_{2} \\\vdots \\x_{m}\end{bmatrix} = \begin{bmatrix}
0\\0\\\vdots\\0
\end{bmatrix}
$$
Note that a hyperplane in $\mathbb{R}^m$ will have a dimension of $m-1$. For instance, $m=2\to \mathbb{R}^2$, which means our hyperplane takes the dimension of a line. 

In general, we can visualize this as the Hyperplane being a subspace of $\mathbb{R}^m$; where the normal vector gives the orthogonal remnant dimension. 

### Plane Equations
Note that we can convert an equation of a plane in a parametric form, into a set of vectors in a vector equation. 
# Pre-Lecture Notes
## Equation of a Line 
Recall the definitions that we had for a general vector in $\mathbb{R}^3$: 

> [!theorem] Equation for a Vector
> $$\begin{bmatrix}x\\ y\\ z\end{bmatrix}= \vec{p} + a\vec{r} = \begin{bmatrix}p_{1}\\ p_{2} \\ p_{3}\end{bmatrix}+ \begin{bmatrix}ar_{1}\\ar_{2} \\ar_{3}\end{bmatrix}$$
> Note that if $\vec{p}=\vec{0}$, we say that the vector runs through the origin. Note that $\vec{p}$ is defined from the origin *onto our line*. 
> Generally, $\vec{p}$ is a *point* on the line defined by $\vec{r}$, and $\vec{r}$ is parallel to the direction of the line.  
> We often notate $\vec{r}$ as some direction vector. 
> Alternatively, we can define it as a set of 3 equations: 
> $$\begin{bmatrix}x=p_{1} + ar_{1}\\y=p_{2} + ar_{2}\\z=p_{3}+ar_{3}\end{bmatrix}$$
> Where $a$ is some scalar multiple of $\vec{r}$. 
^R3VectorEquation

> [!axiom] Lecture Addendum
> Note that we can redefine the equation above to find any equation on the line as well: 
> $$\begin{bmatrix}x-p_{1}\\y-p_{2}\\z-p_{3}\end{bmatrix} = a\vec{r}$$
## Plane Equations
> [!theorem] Equation for a Plane 
> $$\begin{bmatrix}x \\y\\z\end{bmatrix} = \vec{p} + A\vec{r} + B\vec{t} = \begin{bmatrix}p_{1}\\p_{2}\\p_{3}\end{bmatrix} + A\begin{bmatrix}r_{1}\\r_{2}\\r_{3}\end{bmatrix} + B \begin{bmatrix}t_{1}\\t_{2}\\t_{3}\end{bmatrix}$$
> Where $\vec{r},\vec{t}$ are two vectors on the plane that are non-parallel / non-scalar multiples, and $A,B\in \mathbb{R}$, and $\vec{p}$ is a point on the plane from the origin. 
> > Note that if $\vec{p}=\vec{0}$, then our plane runs through the origin. 
> 
> 

Note than an alternate definition exists in terms of *scalars*: A plane can also be defined as the following: 
$$
ax +by+cz = d
$$
Where $d=ax_{0}+by_{0}+cz_{0}$, where $x_{0},y_{0},z_{0}$ is the location of the point $\vec{p}$. 
$$\vec{n} = \begin{bmatrix}a \\b \\c\end{bmatrix}$$
Where $\vec{n}$ is a vector *normal* to the surface of the plane. 

> [!theorem] Lecture Addendum
> Given any vector $\vec{a}$, and we say that $\vec{n}$ is the normal of the plane that contains $\vec{a}$, then: 
> $$\vec{a} \cdot \vec{n} = \vec{0}$$$$\begin{bmatrix}x\\y\\z\end{bmatrix}\cdot \begin{bmatrix}a\\b\\c\end{bmatrix}=\vec{0} \implies ax+by+cz = 0$$
> If our vector doesn't start at the origin, then
> $$\vec{a} \cdot \vec{n} = \vec{0}$$$$\begin{bmatrix}x-x_{0}\\y-y_{0}\\z-z_{0}\end{bmatrix}\cdot \begin{bmatrix}a\\b\\c\end{bmatrix}=\vec{0} \implies ax+by+cz = ax_{0}+by_{0}+cz_{0} = d$$


