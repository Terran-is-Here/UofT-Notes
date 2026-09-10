---
updated_at: 2026-09-09T21:31:12.809-04:00
edited_seconds: 320
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 2
Date: 2026-09-10
Week: 1
---
Hub: [[PHY180 Hub]]
Previous: 
Next:
> [!note] Recommended Reading: 
> [[Vector Review| Vector Review (ESC103H1)]] (has more of a formal definition of the concept of vectors overall)
> **This note will be more focused on the physics-focused elements of Vectors**

--- 

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

## Coordinate Systems 
In general; we have used a rectangular (cartesian) $xy$ ($\mathbb{R}^2$) system. Points can be defined using two values $(x,y)$. 

Vectors can also use the Cartesian system in order to define their own magnitude; with each value in the respective pair representing one of their dimensional components. We can also represent them as a vector *sum* of their components. 
$$
\vec{A} = \vec{A}_{x}+ \vec{A}_{y}
$$
Where $\vec{A}_{}x$ and $\vec{A}_{y}$ are the vector's orthogonal projections onto their respective axis. We can notate these using the unit vectors of the axises 