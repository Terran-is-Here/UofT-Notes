---
updated_at: 2026-10-27T12:27:46.801-04:00
edited_seconds: 160
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[21 — Conservation of Angular Momentum, Gyroscopic Precession]]
Next:
> [!quote] Recommended Reading 
> Section 12.1, 12.2 of the University Physics Textbook.
> Your CIV102 Notes. 
 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Static Equilibrium
Static Equilibrium arises from Newton's Second Law. Recall that the net force is equivalent to the net change in momentum: 
$$
\sum F=\frac{dp}{dt} = ma
$$
In the case of static equilibrium, we set $a=0$, thus: 
$$
\sum F = 0
$$
Conversely, we also define the same for rotational systems, i.e. the net change in the angular momentum of a system must be equal to 0, where: 
$$
\sum \tau = \frac{dI}{dt} = I\alpha
$$
Where $\alpha=0$, then $\sum \tau = 0$, thus giving us our two equilibrium expressions: 
> [!theorem] Equilibrium Expressions
> The following are true if and only if a system is in equilibrium. 
> $$\begin{align}\sum F_{x,y,z}  & = 0  & \text{translational equilibrium} \\\sum \tau  & =0  & \text{rotational equilibrium}\end{align}$$

Note that for both cases, we can break it up into it's corresponding vectors (e.g. $F_{x},F_{y},F_{z},\tau_{x},\tau_{y},\tau_{z}$), or in other words the six degrees of freedom available to an object in some $\mathbb{R}^{3}$. Note that an equilibrium in a system holds true, regardless of which origin you pick for a point of analysis. Do note that distances update accordingly, however force directly pointing inwards/  acting inline with a CoM have their $d$ set to 0 if and only if that point is the point of analysis. 

$$