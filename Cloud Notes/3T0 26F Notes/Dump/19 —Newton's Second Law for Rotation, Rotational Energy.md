---
updated_at: 2026-10-19T11:18:51.023-04:00
edited_seconds: 380
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 19
Lecture Date: 2026-10-18
Week:
Created: October 18th 2026, 6:01:52 pm
---
Hub: [[PHY180 Hub]]
Previous: [[18 — Moment of Inertia, Torque]]
Next:
> [!quote] Recommended Reading 
> University Physics Sec. 10.6 - 10.8 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Torque 
We define torque as the following description: 
$$\vec{\tau} = \vec{r} \times \vec{F}$$
Note that this is similar in theory to how we defined $\alpha$ as $a_t = \vec{\alpha}\times \vec{r}$ being the cross product of the plane / vector formed from $\vec{a}$ and $\vec{r}$. Recall that we can define the magnitude of the cross product as the following: 
$$
|\vec{\tau}| = |\vec{r}||\vec{F}|\sin\theta
$$
Note that Torque is maximized during the case where $\theta=90\degree$, or in other words our force is perfectly perpendicular to some term of radius. Note that we can also define $|\vec{r}|\sin\theta$ as some perpendicular distance from the force towards the center of rotation; that is $d=r\sin\theta = r_{\perp}$; then we can write this as $\tau = Fd$. 

> [!theorem] Torque
> Torque is defined as the following: 
> $$|\vec{\tau}| = |\vec{F}||\vec{r}|\sin \theta = Fd$$
> Where $d$ represents the perpendicular distance of our force from an axis of rotation. The three-dimensional / orthogonal direction of the cross product vector is defined as usual through the right hand rule (thumb variant). 

Note that in terms of analysis of Torque, always consider that you *can* rearrange vectors in vector space roughly freely, as long as you maintain their corresponding directions. You should know the implications of this by now that you shouldn't have to worry about it. 

## Rotational Newton's Second Law
We now seek to define a rotational equivalent to Newton's Second Law. Recall that we defined Newtons' Second Law as the following: 
$$
\frac{F}{m} = a \implies F=ma
$$
Note that we could define this in terms of the other form; that is $F=\frac{dp}{dt}$, but we have not yet formed the concept of the rotational equivalent to the concept of momentum; thus we will keep to this description. 

Recall that for some tangential acceleration $a_{t}$, we can define it as a term of $\alpha$, that is $a_{t}= \alpha r$; substituting this into the term for force above, then: 
$$
F = m\alpha r
$$
Note that if we now multiply this by some perpendicular distance from a center of rotation $r$, then we know that $rF=\tau$: 
$$
\begin{align}
F  & = m\alpha r \\
rF  & =m\alpha r^2 \\
\tau  & =mr^2\alpha & \text{Recall that}~I=mr^2 \\
\tau & =I\alpha
\end{align}
$$
This then states that the Torque of an object is some function of the geometric property of the second moment of area of a particle; we derived a property like this in CIV102: 

> [!theorem]- CIV102 Derivation
> From CIV102, we define the following terms: 
> $$\begin{align}M = Fd \\F = ma\end{align}$$
> Thus, we can equate the two from relating the same $F$ onto them; then$$\frac{M}{d} = ma$$
> For a rotational system; we are convinced that $a= r \frac{d^2\theta}{dt^2}$; then setting $r=d$ and $\alpha=\frac{d^2\theta}{dt^2}$
> $$\begin{align}\frac{M}{r}=mr\alpha \implies M=mr^2\alpha \implies M=I\alpha\end{align}$$
> 

From here, we derive the full expression for extending Newton's Second Law to Rotational Bodies: 
> [!theorem] Newton's Second Law (rigid bodies) 
> The net torque of an object is equivalent to the sum of all the torques on an object, and is equivalent to the product of the Moment of Inertia and the net Angular Acceleration of an object: $$\tau_{net} = \sum \tau = I\alpha$$

Note that $I$ is always some term of the geometry of the object that we are trying to rotate; which means it often varies as a different set of parameters present. 

## Rotational Energy
Recall that in [[11 — Work and Kinetic Energy]], we defined the concept of $W$ 