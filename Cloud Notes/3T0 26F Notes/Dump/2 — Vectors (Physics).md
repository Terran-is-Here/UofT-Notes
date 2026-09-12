---
updated_at: 2026-09-11T21:56:05.361-04:00
edited_seconds: 800
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 2
Date: 2026-09-10
Week: 1
---
Hub: [[PHY180 Hub]]
Previous: [[1 — Units and Measurement]]
Next: [[3 — Position, Velocity, Acceleration]]
> [!note] Recommended Reading: 
> [[Vector Review| Vector Review (ESC103H1)]] (has more of a formal definition of the concept of vectors overall)
> [[Vector Dot Product| Dot Product (ESC103H1)]] (has more formal definitions of the concept of Dot Products)
 > **This note will be more focused on the physics-focused elements of Vectors**

--- 
> [!Quote] Textbook Chapters Discussed
> Chapters 2.1-2.4
> (p53-96) 
## Scalars & Vectors 
* A Scalar is generally defined as a quantity with units, magnitude (and a sign).
* A Vector is generally defined as a quantity with units, magnitude, **and a direction**. 

Vectors are generally notated with an arrow atop; e.g. $\vec{a}$. Note that you cannot intrinsically add vectors and scalars together (though you can multiply them). In terms of terminology: 
* A vector is **parallel** if they have the same direction unit vector as each-other; or in other words being directly **parallel**. 
* A vector is **orthogonal** if they have direction vectors perpendicular with each other.
	* Or in other words; their dot product is 0 ($\vec{a}\cdot \vec{b}=|\vec{a}||\vec{b}|\cos(\theta)=0$)
* A vector is **antiparallel** is they have the opposite direction vector as each other; that is their angles are $180\degree$ of each other.

## Displacement
Displacement is generally defined as $\Delta p$; and is notated as a vector (often $\vec{D}$). A vector's magnitude can be notated by inputting the absolute value notation around a vector: 
$$
|\vec{D}| = D
$$
## 1D Vector Algebra
Define two vectors as $\vec{a}$ and $\vec{b}$; whose magnitudes are defined by $A$ and $B$ respectively: 
$$
A = |\vec{a}|
$$
$$
B = |\vec{b}|
$$
Vectors can be scaled off each other via scalars; for instance: $\vec{a} = 0.75\vec{b}$. This equation is considered a *vector equation*; as both sides of the equation are vectors. Note that $\vec{a}$ would be parallel to $\vec{b}$ in this case; with their magnitude appropriately scaled: 
$$
A = |b|B
$$
The sum of a series of vectors is normally notated as the Resultant (normally notated by $\vec{r}$ and $R=|\vec{r}|$). 

Note that for $n$ dimensional vectors; it may be more apt to define a *direction* with a magnitude rather than a pure vector. Recall that unit vectors are vectors with a magnitude of $1$; and are notated with a little hat symbol (e.g. $\hat{l}$). 

## Components
In general; we have used a rectangular (cartesian) $xy$ ($\mathbb{R}^2$) system. Points can be defined using two values $(x,y)$. 

Vectors can also use the Cartesian system in order to define their own magnitude; with each value in the respective pair representing one of their dimensional components. We can also represent them as a vector *sum* of their components. 
$$
\vec{A} = \vec{A}_{x}+ \vec{A}_{y}
$$
Where $\vec{A}_{}x$ and $\vec{A}_{y}$ are the vector's orthogonal projections onto their respective axis. We can notate these using the unit vectors of the axes: 
* x = $\hat{i}$
* y = $\hat{j}$
* z = $\hat{k}$

Thus we can define the equation above as: 
> [!axiom] Vector Equation (Component) 
> $$\vec{A} = A_{x}\hat{i}+ A_{y}\hat{j}$$
Where $A_{x}$ and $A_{y}$ are the scalar components of $\vec{A}$. 

We can also define $A_{x}$ and $A_{y}$ through the difference of the points present at the origin ($x_{0},y_{0}$) and it's endpoint $x_{a}, y_{a}$: 
$$
A_{x} = x_{a} - x_{0}
$$
$$
A_{y} = y_{a} - y_{0}
$$

Adding two vectors together in this format is equivalent to adding up their respective components in the same axis: 

### Generalized Dimensions
For a $3D$ vector; we also have to account for the $z$ axis of the vector. We can define our vector in component form by extending it to our third dimension; letting $\hat{k}$ be the unit vector in the positive $z$ axis: 
$$
\vec{A} = A_{x}\hat{i}+ A_{y}\hat{j} + A_{z}\hat{k}
$$

### Magnitude and Angle 
Note that $A_{x}, A_{y}, A$ all form a right angle triangle; with $A$ as the longest side; therefore: 
$$
A^2 = A_{x}^2 + A_{y}^2 \implies A = \sqrt{ A_{x}^2 + A_{y}^2 }$$
Magnitude is generalized to an $n$-dimensional vector as: 
$$||\vec{a}|| = \sqrt{ \sum^n_{{i=1}}a_{i}^2 }$$
We can also find the angle it makes with the $+x$ axis towards the vector (counter clockwise): 
$$
\tan \theta_{A} = \left(\frac{A_{y}}{A_{x}}\right) \implies \theta_{A} = \cot\left(\frac{A_{y}}{A_{x}}\right)
$$

From viewing our vectors as a right-angle triangle; we can now also define them as a function of a vector's magnitude and angle: 
$$
A_{x} = A\cos \theta_{A}
$$
$$
A_{y} = A\sin\theta_{A}
$$
### Polar Coordinates
Polar Coordinates are an alternate means of describing a vector/point. We normally use the Polar Coordinate System when we are dealing with rotational systems. 

Unlike the cartesian coordinate system; the Polar Coordinate System is defined by two values: $r$ (the distance of a point from the origin) and $\theta$ represents the angle it makes from a certain baseline (normally $+x$). 

> [!axiom] Polar Coordinate representation of a Vector 
> Given a point $P = (x,y)$; we can define it in a polar coordinate system as: 
$$P=\begin{cases}x = r\cos\theta \\y=r\sin \theta\end{cases} = (r,\theta)$$
> The *radial* vector (notated $\hat{r}$) is the unit vector directly pointed to our point; whilst another vector $\hat{t}$ is orthogonal to $\hat{r}$ in the counter-clockwise direction; essentially a positive direction of rotation for the $\theta$ value of our point. 

**Note that for Polar Coordinates, $\theta$ is solely defined in Radians.**
## Vector Operations & Algebra
Recall earlier how we described that we can actually manipulate vectors with scalars; we can extend this towards their vector component representations. For some scalar $S$: 
$$
S\vec{A} = SA_{x}\hat{i}+ SA_{y}\hat{j} + SA_{z}\hat{k}
$$
Note that we can also actually modify this some more; a vector can be mathematically be defined to be antiparallel if it is equivalent to it's negative version (or; it's additive inverse where $\vec{A} + (-\vec{A}) = \vec{0}$): 
$$
-\vec{A} = -A_{x}\hat{i}- A_{y}\hat{j} - A_{z}\hat{k}
$$

> [!axiom] Definition of $\vec{0}$: 
> Given $\vec{a}$ and $-\vec{a}$: 
> $$\vec{a} = a_{x}\hat{i} + a_{y}\hat{j} + a_{z}\hat{k}$$
> $$-\vec{a} = -a_{x}\hat{i} - a_{y}\hat{j} - a_{z}\hat{k}$$
> Summing these together: 
> $$\vec{a}-\vec{a} = -a_{x}\hat{i} - a_{y}\hat{j} - a_{z}\hat{k} + a_{x}\hat{i} + a_{y}\hat{j} + a_{z}\hat{k}$$
> All these terms cancel out, leading us to the definition of the 0 vector. 
> $$ \vec{0} = 0\hat{i} + 0\hat{j} + 0\hat{k}$$

