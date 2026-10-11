---
updated_at: 2026-10-11T00:07:18.330-04:00
edited_seconds: 320
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-10
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[15 — Conservation of Momentum, Collisions]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics 9.6, 9.7
> [[14 — Momentum and Impulse]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Center of Mass
So far, all Newtonian mechanics have been focused on defining the behaviors of point loads: 
$$
F=ma
$$
Consider a particle composed of $N$ masses; where: 
$$
m_{\text{total}}= \sum _{j=1}^Nm_{j}
$$
Where $m_{j}$ represents the mass of the $j$-th particle of our system. Now consider that if we have an applied force $F_{a}^\text{ext}$ over our object, each miniscule particle will have it's own applied force $F_{j}^\text{ext}$ from the external source. Note that $F_{j}$ between particles may not be equivalent; and are often *not* equivalent. 

Consider now that each particle in isolation may *apply* forces to their neighbours. From Newton's Third Law, we know that each particle when a force is applied will feel a reactive force $F_{j}^\text{Int}$ in turn. Note that we say that this force does not inherently cancel out; but rather they are applied on separate bodies. Therefore for some particle $F_{j}$, the sum of the forces it experiences are defined as below: 
$$
F_{j} = F_{j}^\text{Ext} + F_{j}^\text{Int}
$$
Note that $F=\frac{dp}{dt}$; then: 
$$
\frac{dp_{j}}{dt} = F_{j}^\text{Ext} + F_{j}^\text{Int} \tag{1.1}
$$
Note now considering this whole system as a whole as some $F^\text{ext}_{a}$ is applied on our *entire object*. This changes the momentum of the entire system; thus: 
$$
F_{net} = \sum^N_{j=1} \frac{dp_{j}}{dt}
$$
Note that from $(1.1)$ that we can relate the sum the momentums with the sum of some internal forces of our objects; that is: 
$$
\sum_{j=1}^N F_{j}^\text{Ext} +\sum_{j=1}^N F_{j}^\text{Int}  =  \sum^N_{j=1} \frac{dp_{j}}{dt}
$$
Consider the term $\sum_{j=1}^N F_{j}^\text{Int}$, this represents the reaction force pairs within our body. Since these pairs are internal, and our object is *preferably* not tearing itself apart, then this term should equal 0; then: 
$$
\boxed{\sum_{j=1}^N F_{j}^\text{Ext}= F_{j}^\text{ext}  =  \sum^N_{j=1} \frac{dp_{j}}{dt}}

$$
That is, the net external force applied is equivalent to the sum of the corresponding change of momentum over the time period of *all* of the particles present in our object. 