---
updated_at: 2026-10-27T12:16:05.743-04:00
edited_seconds: 570
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 21
Lecture Date: 2026-10-26
Week: 8
---
Hub: [[PHY180 Hub]]
Previous: [[20 — Rolling Without Slipping and Angular Momentum]]
Next: [[22 and 23 — Static Equilibrium and Elasticity]]
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
> Or, more generally: 
> $$L = mv*r\sin\theta$$
> Where $m$ represents the mass member, $v$ represents it's tangential velocity, and $r \sin\theta$ can be rewritten as some perpendicular distance $d$ from the centre of rotation: $$L=mvd$$

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

> [!caution] Note
> Additionally since $I=\sum mr^{2}$, then if another object (e.g. a collision, etc) is added onto an object that is revolving, that too would be added onto the corresponding $I'$ term in the final/initial angular momentum. 

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

## Gyroscopic Precession
Note that the conservation of angular momentum, when given that $I$ is constant, lets us derive a concept of "precession" for a rotating body. Let us assume a rotating body has a constant angular momentum $L=I\omega$. For the purposes of this derivation, we will refer to this graphic (since it is quite helpful for understanding where the derivation originates from): 
![[21 — Conservation of Angular Momentum, Gyroscopic Precession-1793117084485.webp|320]]

Let us now also assume that some applied gravitational torque is applied onto our object from it's center of mass (see [[16 — Center of Mass and Rockets]]), then we know the torque applied is given to us by the following. Let $\theta$ be the value for how "tipped" our object is (i.e. it's inclination), then: 
$$
\tau = rMg\sin\theta 
$$
Recall that $\frac{dL}{dt}=\sum \tau$, then
$$
dL = rMg\sin\theta\,dt
$$
We know that $dL$ will be applied orthogonal to $L$, and therefore will cause a rotation across a horizontal axis. We also affirm that in this context, the magnitude of $L$ is held constant, only it's direction will change. (or in other words, $\omega$ is held constant). 

Therefore, with an applied $dL$, and a constant magnitude of $L$, since $dL\perp L$, then there will exist a form of circular precession for our object. We can note that the radius of precession will be defined by some $L\sin\theta$, and the corresponding tangential value of $L$ will be some value of $dL$, thus: 
$$
\begin{align}
d\phi  & = \frac{dL}{L\sin\theta} = \frac{rMg\sin\theta}{L\sin\theta}\,dt  \\
 d\phi& =\frac{rMg}{L}\,dt  & \text{recall, }d\phi = \omega_{p}\text{ and } L=I\omega, \text{then} \\
 \omega_{p} & =\frac{rMg}{I\omega}
\end{align}
$$
Note that in this context, $\omega$ represents the rotational velocity of our gyroscope as is, and $\omega _p$ represents the rotational velocity of the procession of our rotating body. Note that the implications of this, is that: 
1. $\omega_{p}\propto \frac{1}{\omega}$, that is if $\omega$ increases, $\omega _p$ decreases. If you spin something faster, it processes slower.
2. Same applies for the Moment of Inertia above, if you make something harder to spin, it processes slower. 
	1. Or in other words, $\omega_{p}\propto \frac{1}{L}$, where the increase in angular momentum of the system decreases the rate of procession. 
3. Our term for $\omega_{p}$ is completely independent of what value $\theta$ we give (i.e. the angle of inclination). 
> [!caution] Note
> This derivation assumes $\omega_{p} \ll \omega$.