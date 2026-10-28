---
updated_at: 2026-10-28T19:24:44.067-04:00
edited_seconds: 320
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 25
Lecture Date: 2026-10-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[24 — Gravitation]]
Next: [[26 — Tidal Forces, General Relativity]]
> [!quote] Recommended Reading 
> Sections 13.4, 13.5 of University Physics


--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Circular Orbits
Consider now the concept of a perfectly circular object. Recall that for a circular body, a centripetal force is applied onto it as it's net force: 
$$
F_{c}=ma_{c}=\frac{mv^{2}}{r}
$$
Consider now that if an object is orbiting a planetary body, this force is solely provided by $F_{g}$, that is the force of gravity. Taking Newton's Law of Universal Gravitation, we find that: 
$$
\frac{GMm}{r^{2}} = \frac{mv^{2}}{r}
$$
Where $v$ represents the orbital velocity. Note that $m$ cancels out in this expression, and thus we can solve for $v$: 
$$
\begin{align}
\frac{GMm}{r^{2}} & =\frac{mv^{2}}{r} \\
\frac{GM}{r} & =v^{2} \\
v & =\sqrt{ \frac{GM}{r} }
\end{align}
$$
> [!theorem] Orbital Velocity (perfectly circular orbits) 
> The orbital velocity of an object in a perfectly circular orbit is defined as the following expression: 
> $$v=\sqrt{ \frac{GM}{r} }$$
> Where $r$ is the radius of the orbit, with respects to the center of mass of the object being orbited. 

Recall that $v=\omega r$, as this is a rotating body, and recall that $\omega$ can be resolved as some $\frac{d\theta}{dt}$, or in terms of revolutions per second, $\frac{2\pi}{T}$, where $T$ represents the period, substituting this in, then: 
$$
\begin{align}
r\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r} } \\
\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r^{3}} } \\
T  & = 2\pi \sqrt{ \frac{r^{3}}{GM} }
\end{align}
$$
Where $T$ represents the rotational period of our body. or in other words: how long it takes to orbit. 
### Boundness
Recall that in our previous note, where we discussed how an object would be gravitationally bound if the total energy is *negative* (see [[24 — Gravitation#Boundness| PHY180(24) - Boundness]]): 
$$
E_{T} < 0
$$
Consider now the case when $v=\sqrt{ \frac{GM}{r} }$ as some term of orbital velocity, then we have: 
$$
\begin{align}
E_{t}  & = K + U_{g}  &\text{ Let }U_{g}=-\frac{GMm}{r},\, K=\frac{1}{2}mv^{2} \\
 & =\frac{1}{2}mv^{2} - \frac{GMm}{r} &\text{Recall, } v=\sqrt{ \frac{GM}{r} } \\
 & =\frac{1}{2}m\left( \frac{GM}{r} \right)-\frac{GMm}{r} \\
 & =\frac{GMm}{2r}-\frac{GMm}{r}= -\frac{GMm}{2r}
\end{align}
$$
Thus, we can see that the energy within a rotating system's total is equal to some negative value, thus an orbiting body in a perfectly circular orbit is gravitationally bound to the object in which it is orbiting with respects to. 

> This result also apparently applies to any two masses in circular orbits around their common center of mass, at a distance $r$ from each other, proof will be provided here when I get to doing this exercise. 


