---
updated_at: 2026-09-28T16:23:20.217-04:00
edited_seconds: 450
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 7
Lecture Date: 2026-09-24
Week:
created:
Created: September 18th 2026, 10:28:45 pm
---
Hub: [[PHY180 Hub]]
Previous: [[6 — Uniform Circular Motion]]
Next: [[8 — 3rd Law of Newton, FBDs]]

> [!quote] Relevant Textbook Sections: 
> 5.1-5.4


--- 

# Lecture Notes
## Dynamics
Dynamics are generally defined as the study of *why* things move. 
# Pre-Lecture Notes
## Forces
A force is generally defined as a *push* or a *pull* from something *external to the system*[^1]. Forces *are* vectors (i.e. with Magnitude and Direction). Also recall that vectors are defined in terms of Newtons (units of $[M^1L^1T^{-2}]$). 

[^1]: Taken from the lecture.
### Newton's First Law 
Newton's First Law states that: 
> [!theorem] NFL 
> A body at rest remains at rest, or if in motion, remains in motion at constant velocity, unless acted upon by a net external force. 

Mathematically, we can say that $\bar{v}$ remains constant across a timespan if $F_{N}=0$. 

Basically, an object's velocity (both it's direction and magnitude) cannot be changed unless acted upon by an external force. This is generally defined as the Law of Inertia, as Inertia is defined as the integral of force. 

NFL also generally defines the concept of Inertial Reference Frames: 
> [!theorem] Inertial Reference Frames
> A reference frame moving at *constant* velocity relative to an inertial frame of reference is also considered to be inertial. A reference frame *accelerating* with respects to an inertial frame of reference is considered to be non-interial.

> [!caution] Caution
> Newton's Laws only apply to **Inertial Reference Frames**. If a frame has an inherent acceleration, it is considered non-inertial, and cannot be considered as following Newton's Law. 
## Newton's Second Law
Newton's Second law states that: 
> [!theorem] NSL: 
> The acceleration on a system is directly proportional to the force applied and inversely proportional to the mass of the system. That is: $$\vec{a} = \frac{\vec{F_{N}}}{m}$$
> Where $\vec{a}$ is acceleration, $\vec{F_{N}}$ is the force applied, and $m$ is the mass of the system. This is more often written as: $$F_{N} = m \vec{a}$$

Note that since $\vec{F_{N}}$ is some vector, we can also break it down into components. 
### Momentum
Note however that Newton actually defined his second law in terms of Momentum:
> The instantaneous rate at which a body's momentum changes is equal to the net force acting on the body: 

That is; $$F_{N} = \frac{d\vec{p}}{dt}$$
Momentum for now can be generally defined as $$\vec{p} = m\vec{v}$$
Note that with this definition, then our above descriptor for Force via momentum simplifies. Assume that $m$ remains as some constant; then: 
$$
F_{N} = \frac{d(m\vec{v})}{dt} = m \frac{d\vec{v}}{dt} = m\vec{a}
$$
## Weight
Weight is generally defined as the following: 
$$
W_{m} = mg
$$
Where $m$ is the mass of an object, and $g$ is the gravitational pull of the Earth, though more generally defined as the gravitational acceleration derived from some other formula. For instance, assuming Newtonian Mechanics, this evaluates as: 

$$
W_{m} = m *\left[\frac{GM}{r^2}\right]
$$
Where $G$ is the gravitational constant of $\frac{6.67*10^{-11}Nm^2}{kg^2}$ and $M$ is the mass of the main body of gravity within the system, and $r$ is some term representing the distance of the body of analysis from the center of mass of the gravitational body.


