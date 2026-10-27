---
updated_at: 2026-10-26T22:52:19.577-04:00
edited_seconds: 300
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-26
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[20 — Rolling Without Slipping and Angular Momentum]]
Next: N/A
> [!quote] Recommended Reading 
> Sections 11.3, 11.4 of the University Physics Textbook. 
> [[15 — Conservation of (Translational) Momentum, Collisions]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Conservation of Angular Momentum
Recall our definitions for Angular Momentum: 
$$
L= rp \sin\theta = I\omega
$$
Note that for the purposes of notation, we will consider the term of Angular Momentum as some variable $L$, and the corresponding moment of inertia as some variable $I$. Recall that we also defined that the net change in the angular momentum of a system is defined in terms of the net torque applied *onto* the system, that is: 
$$
\frac{dL}{dt} = \sum \tau
$$
Recall, since $\tau=I\alpha, \frac{dL}{dt}=I \frac{d\omega}{dt} = I\alpha = \tau$. Thus we define the concept of the Conservation of Angular Momentum as the following: 

> [!theorem] Conservation of Angular Momentum
> If the net torque applied on a system is 0, or in other words, the change in the total angular momentum of the system is 0, then the angular momentum in that system is conserved: 
> $$\frac{dL}{dt}=0 \implies L=\sum_{i=1}^{N} I_{i}=\text{some constant}$$
> Or in other words, (using the same notation as we did during translational momentum), then:
> > $$I\omega=I'\omega'$$
> > Where $'$ signify the "final" and or "terminal" versions of these; i.e. at some point in time $t$: 
> > $$I_{0}\omega_{0} = I_{t}\omega_{t}$$

Recall that $I=\sum mr^2$, or rather $I=\int r^2dm$; if the radius of the rotating object decreases with respect to the masses, then $\omega$ proportionally increases (and vice versa). Consider this implication in the context of angular/rotational kinetic energy; where we have an initial and final rotational kinetic energy (e.g. from pulling weights closer, etc.)
$$
\begin{align}
K_{rot}  & = \frac{1}{2}I\omega^2 \\
K'_{rot} & =\frac{1}{2}I'\omega'^2
\end{align}
$$
Note that if Angular Momentum is conserved, then $I\omega=I'\omega'$ holds, and we can see that $\omega' = \frac{I\omega}{I'}$, then: 
$$
\begin{align}
K'_{rot} & =\frac{1}{2}I'\left( \frac{I\omega}{I'} \right)^2 \\
  & =\frac{1}{2} \frac{I'I^2\omega^2}{I'^2} = \frac{1}{2}I\omega^2 \frac{I}{I'} \\
  K'_{rot}& =K_{rot}\left( \frac{I}{I'} \right)
\end{align}
$$
That is, the corresponding rotational kinetic energy before and after a change in the structure of the rotating body in the case where angular momentum is preserved, can be found by comparing a ratio of the resulting moments of inertia before and after: 
$$
\frac{K'_{rot}}{K_{rot}}=  \left( \frac{I}{I'} \right)
$$