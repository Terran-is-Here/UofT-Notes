---
updated_at: 2026-09-14T21:15:55.789-04:00
edited_seconds: 260
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 0
Lecture Date: 2026-09-14
Week:
Created: September 14th 2026, 11:08:55 am
---
Hub: [[ESC103 Hub]]
Previous: [[02 —Vector Dot Product]]
Next: [[04 — Vector Cross Product]]

--- 
# Lecture Notes
# Pre-Lecture Notes
For the purposes of this note; let $\vec{a}$ and $\vec{b}$ be two vectors; with the angle between them in tail-to-tail being notated as $\theta$
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
