---
updated_at: 2026-11-23T10:43:48.258-05:00
edited_seconds: 500
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 31
Lecture Date: 2026-11-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[30 — Simple Harmonic Motion]]
Next: [[32 — Damped and Forced Oscillations]]
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
> Where $\omega = \frac{2\pi}{T}$  or $\omega=\pm\sqrt{ C }$ where $\omega$ represents the **angular frequency** of our system.
> $$\begin{align}\frac{dx}{dt}  & =  -A\omega \sin(\omega t+\phi) \\\frac{d^{2}x}{dt^{2}}  & = -A\omega^{2}\cos(\omega t+\phi)\\a_{max}  & = A\omega^{2} \\v_{max} & =A\omega\end{align}$$

Note that in these equations, if we plug in our expression, we find that $\omega$ will always be related to $C$ in some way (not inherently, but after getting algebraic manipulations into role, this is normally the case). As such, we can actually generalize this concept for a wider range of oscillatory systems.

> [!caution] Note
> The following equations are all that one requires pertaining to SHM which is undampened, we simply need to change the corresponding terms present, and or rearrange our conventional force equations into this form in order to plug in our expressions derived. 

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
Note as well as since $\omega=\sqrt{ \frac{g}{L} } = \frac{2\pi}{T}$, then: 
$$
\begin{align}
\sqrt{ \frac{g}{L} }  & =  \frac{2\pi}{T} \\
T  & =2\pi \sqrt{ \frac{L}{g} }
\end{align}
$$
## Physical Pendulums 
Consider the case in which we do not have a point mass system, but rather some distributed mass of non-negligible magnitude present within our expression. We thus find that: 
$$
\tau = -Lmg\sin\theta = I\alpha
$$
Using the same concepts as before, then using a small angle approximation where $\theta \approx \sin\theta$, then: 
$$
\begin{align}
I\alpha & =-Lmg\sin\theta  & \sin\theta \to \theta\\
I \frac{d^{2}\theta}{dt^{2}} & = -Lmg\theta \\
\frac{d^{2}\theta}{dt^{2}} & = -\left( \frac{Lmg}{I} \right)\theta
\end{align}
$$
This implies that $C = \frac{Lmg}{I}$, thus we are inclined to choose $\omega = \sqrt{ \frac{Lmg}{I} }$, and thus: 
$$
\begin{align}
\omega & = \sqrt{ \frac{Lmg}{I} } = \frac{2\pi}{T} \\
 T & = 2\pi \sqrt{ \frac{I}{Lmg} }
\end{align}
$$
Note that $L$ in this context corresponds to the distance from the center of mass (where forces of gravity act on) to the pivot point present. Note that if $I$ is corresponding to a point mass, then $I=mL^{2}$, thus we get our expression from previously back. 
## Torsional Pendulums 
Consider now the case in which a mass / object is suspended from a wire which has already been twisted. For these systems, the wire will have some torsion constant pertaining to it's resistance to being twisted. These wires inherently want to stop being twisted with respects to an angular displacement, thus: 
$$
\tau = -\kappa\Theta 
$$
Where this torque is equivalent to our wire trying to unwind itself, thus recalling that $\tau = I\alpha$, then: 
$$
\begin{align}
\tau =I\alpha & = -\kappa\Theta  \\
I \frac{d^{2}\Theta }{dt^{2}} & =-\kappa\Theta \\
\frac{d^{2}\Theta}{dt^{2}} & = -\left( \frac{\kappa}{I} \right)\Theta
\end{align}
$$
Then, recalling our differential from earlier, we are inclined to choose: 
$$
\begin{align}
\omega= \sqrt{ \frac{\kappa}{I} } & =\frac{2\pi}{T} \\
T & = 2\pi \sqrt{ \frac{I}{\kappa} }
\end{align}
$$
