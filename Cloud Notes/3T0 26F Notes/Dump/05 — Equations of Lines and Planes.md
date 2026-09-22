---
updated_at: 2026-09-21T21:13:03.035-04:00
edited_seconds: 560
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
Where: 
$$\vec{n} = \begin{bmatrix}a \\b \\c\end{bmatrix}$$
Where $\vec{n}$ is a vector *normal* to the surface of the plane. 