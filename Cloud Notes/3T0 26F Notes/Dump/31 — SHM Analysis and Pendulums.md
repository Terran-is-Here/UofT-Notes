---
updated_at: 2026-11-22T21:17:57.429-05:00
edited_seconds: 290
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 31
Lecture Date: 2026-11-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[30 — Simple Harmonic Motion]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics Sections 15.3 to 15.4
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Other Systems
Retaking our general system of equations for SHM, this time without any of the other explanatory text,
> [!theorem] Equations of SHM
> $$\frac{d^{2}x}{dt^{2}}=-Cx$$
> $$x=A\cos(\omega t+\phi)$$
> Where $\omega = \frac{2\pi}{T}$ where $\omega$ represents the **angular frequency** of our system.
> $$\begin{align}\frac{dx}{dt}  & =  -A\omega \sin(\omega t+\phi) \\\frac{d^{2}x}{dt^{2}}  & = -A\omega^{2}\cos(\omega t+\phi)\\a_{max}  & = A\omega^{2} \\v_{max} & =A\omega\end{align}$$

Note that in these equations, if we plug in our expression, we find that $\omega$ will always be related to $C$ in some way (not inherently, but after getting algebraic manipulations into role, this is normally the case). As such, we can actually generalize this concept for a wider range of oscillatory systems.

## Simple Pendulums
A Simple Pendulum is a system defined to have a *point mass* (or a pendulum bob) suspended from a string of length $L$ with negligible mass. Considering the torque on that pendulum, being the force of gravity acting on the arclength of that pendulum, we find that: 
$$
\tau = -Lmg\sin\theta
$$
Noting that the negative sign implies that it is acting in the opposite direction to the angular displacement, as is defined for SHM systems. Recalling that $\tau= I\alpha =I \frac{d^{2}\theta}{dt^{2}}$, then: 
$$
I\frac{d^{2}\theta}{dt^{2}}  = -Lmg\sin\theta
$$
Solving this differential is outside the bounds of this course, but if we let $\theta$ be a small number, then $\sin\theta \approx\theta$, thus: 
$$
\begin{align} 
I\frac{d^{2}\theta}{dt^{2}}  & = -Lmg\theta & I=mL^{2} \\
\cancel{ m }L^{2} \frac{d^{2}\theta}{dt^{2}}  & =-L\cancel{ m }g\theta \\
\frac{d^{2}\theta}{dt^{2}}  & =-\frac{g}{L}\theta
\end{align}
$$
This then implies that we choose $\omega=\sqrt{ \frac{g}{L} }$ into our system of equations above. Note that since this differential is now in terms of an **angular** derivative, not a translational derivative, then: 
$$
\begin{align}
\frac{d\theta}{dt} & = -A\omega \sin(\omega t+\phi) = \omega_{angular,t} \\
 & \implies \omega_{angular,max} = A\omega \\
\frac{d^{2}\theta}{dt^{2}} & = -A\omega^{2}\cos(\omega t+\phi) = \alpha \\
 & \implies\alpha_{max} = A\omega^{2}
\end{align}
$$

