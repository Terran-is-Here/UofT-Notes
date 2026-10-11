---
updated_at: 2026-10-11T00:19:39.267-04:00
edited_seconds: 490
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
## Extending Newtonian Mechanics
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
### Center of Mass
Consider now that if our object has some total momentum represented by the points; some $P_{t}$; then: 
$$
F = \frac{dP_{t}}{dt}
$$
If we consider this situation; recall that we can define $P_{t}$ as $\sum p_{j}$; then take the following; note that $M$ represents the **total mass of the body**. 
$$
F = \sum^N_{j=1} \frac{d \vec{p_{j}}}{dt} = M\vec{a}
$$
Rewriting this; then: 
$$
\begin{align}
M\vec{a} &  = \sum_{j=1}^N \frac{d\vec{p_{j}}}{dt} \\
 & = \frac{d}{dt}\sum_{j=1}^N \vec{p_{j}}  & \text{Note, }\vec{p_{j}} = m_{j} \vec{v_{j}} = \frac{m_{j}\vec{x_{j}}}{dt}\\
 & = \frac{d}{dt}\sum_{j=1}^N m_{j} \frac{d\vec{x_{j}}}{dt} \\
 M\vec{a}&  = \frac{d^2}{dt^2}\sum_{j=1}^N m_{j}\vec{x_{j}}
\end{align}
$$
Then, dividing by the *total* mass of the body: 
$$
\vec{a} =  \frac{d^2}{dt^2}\left( \frac{1}{M}\sum_{j=1}^N m_{j} \vec{x_{j}} \right)
$$
Note that the term in the parenthesis *actually gives us the center of mass*. Or in other words; Center of Mass is the *mean* of the system as a weighed average as a function of distance and weight. 

$$
\vec{x_{\text{CoM}}} =  \frac{1}{M}\sum_{j=1}^N m_{j} \vec{x_{j}}
$$
Note that this is in terms of a vector; we can break this up into it's dimensional components; then performing the traditional resultant vector math to get the equivalent center of mass. 
