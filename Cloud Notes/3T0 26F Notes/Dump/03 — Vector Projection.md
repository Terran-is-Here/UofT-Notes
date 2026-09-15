---
updated_at: 2026-09-15T17:32:50.423-04:00
edited_seconds: 310
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 0
Lecture Date: 2026-09-15
Week:
Created: September 14th 2026, 11:08:55 am
---
Hub: [[ESC103 Hub]]
Previous: [[02 —Vector Dot Product]]
Next: [[04 — Vector Cross Product]]

--- 
# Lecture Notes
## Projection
Retake our earlier definition(s) of a vector: 
$$
\vec{a} = \begin{bmatrix}
a_{1} \\
a_{2}
\end{bmatrix} = a_{1}\hat{i} + a_{2}\hat{j}
$$
The left-most term implies that we find our $a_{1}$ term as a projection of $\vec{a}$ onto $\hat{i}$. Projection is essentially resolving some vector $\vec{a}$ into it's projections in $x,y,z$ (or more specifically, $\hat{i},\hat{j},\hat{k}$). 

Note that for $\mathbb{R}^2$, $a_{1}\hat{i}$ and $a_{2}\hat{j}$, these two corresponding projections are orthogonal complements of eachother. 
# Pre-Lecture Notes
For the purposes of this note; let $\vec{a}$ and $\vec{b}$ be two vectors; with the angle between them in **tail-to-tail** being notated as $\theta$. 
## Scalar Projection
The scalar projection of a vector following the assumptions above can be generally defined as the relation below: 
$$\text{proj}_{\vec{b}}\vec{a} =||\vec{a}||\cos \theta$$
This is notated as the projection of $\vec{a}$ on $\vec{b}$. Recall the definition of the Dot Product: 
$$\vec{a} \cdot \vec{b} = ||\vec{a}||*||\vec{b}||\cos \theta$$
Multiplying our earlier equation by $\frac{||\vec{b}||}{||\vec{b}||}$ gives us: 
$$
\text{proj}_{\vec{b}}\vec{a} = \frac{||\vec{a}||*||\vec{b}||\cos\theta}{||\vec{b}||} = \frac{\vec{a}\cdot \vec{b}}{||\vec{b}||}
$$
## Vector Projection
Vector projection is generally defined as: 
$$\text{vector proj}_{\vec{b}}\vec{a} = \text{proj}_{\vec{b}}\vec{a}* \hat{b} = \text{proj}_{\vec{b}}\vec{a} * \frac{\vec{b}}{||\vec{b}||}$$
We can sub in our extended equation to our dot product: 
$$\text{vector proj}_{\vec{b}}\vec{a}= \frac{\vec{a}\cdot \vec{b}}{||\vec{b}||} * \frac{\vec{b}}{||\vec{b}||}$$
We can simplify the denominator into a dot product as well; recall that $||\vec{b}||*||\vec{b}|| =\vec{b}\cdot \vec{b}$
$$
\text{vector proj}_{\vec{b}}\vec{a}=\frac{\vec{a}\cdot \vec{b}}{\vec{b}\cdot \vec{b}}\vec{b}
$$
