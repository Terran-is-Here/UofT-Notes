---
updated_at: 2026-10-01T16:40:17.610-04:00
edited_seconds: 480
course: PHY180H1
tags:
  - PHY180H1
  - TBF
"Lecture #": 10
Lecture Date: 2026-10-01
Week: 4
Created: September 23rd 2026, 9:40:33 pm
---
Hub: [[PHY180 Hub]]
Previous: [[9 — Friction and Centripetal Force]]
Next: [[11 — Work and Kinetic Energy]]

--- 
# Lecture Notes
## Hooke's Law 
Hooke's Law was mentioned in this lecture, but a pre-written section was already written in depth in the following note: [[11 — Work and Kinetic Energy#Hooke's Law & Elastic Energy|PHY180 (11) - Hooke's Law]]. 
## Reaction Forces
Note that Normal Forces and Friction forces (static friction) are only to what is needed. 
## Rolling Friction
Note that for rotational objects, we say that their corresponding coefficient of friction is equivalent to their static friction (as for a rotational member, the bottom of the thing should be static) 
# Pre-Lecture Notes
## Drag Force
Drag Force is the fluid equivalent to the concept of a contact frictional force between two surfaces, albeit in fluids. Akin to the concept of $F_{F}$, it also acts directly opposite in the direction of motion, albeit unlike $F_{F}$, it is also proportional to the velocity of the object. 

> [!theorem] Drag Force
> $$F_{D} = \frac{1}{2}C\rho Av^2$$
> Where $\rho$ is equivalent to the density of our fluid ($[M^1L^{-3}]$), 
> $C$ is some constant related to the shape of our object (empirically defined)
> $A$ is the cross-section of our object

Note that since $\frac{1}{2}C\rho A$ is often some constant, that is it (will normally) not change during the movement of an object, it is often denoted as some constant $b$; i.e.
$$
b = \frac{1}{2}C\rho A \implies F_{D} = bv^2
$$
Note however that the equation for Drag Force above is not entirely universal, for cases such as: 
* A very *small* object
* A very *slow* object
* $\rho > \rho_{\text{Air}}$
The relationship for the force of drag is instead represented by Stokes' Law. 
## Terminal Velocity
Note that since $F_{D}$ scales with $v$, we can solve directly for a term of *terminal velocity* by equating this with the *weight* of an object: 
$$
W_{M} = F_{D}
$$
$$
mg = \frac{1}{2}C\rho Av^2
$$
In this context, we define $v$ as $v_{T}$, notating this as the *terminal velocity*, from here we can solve for $v_{T}$: 
$$
\sqrt{ \frac{2mg}{C\rho A} } = \sqrt{ \frac{mg}{b} } = v
$$
## Stokes' Law 
Stokes Law is a special case(?) of Drag Force which mainly operates under the following regimens: 
1. Our object is a very small object—specifically something that we can define as having some *radius*. 
2. Our object has a low velocity, 
3. $\rho > \rho_{\text{Air}}$
If any of these are true, then the following equation is more accurate for modelling the force of drag experienced by an object:

> $$F_{s} = 6\pi r\eta v$$
> Where: 
> * $\eta$ is the Viscosity of our Fluid (under some condition) 
> * $r$ is the Radius of our object
> * $v$ is the velocity of our object. 