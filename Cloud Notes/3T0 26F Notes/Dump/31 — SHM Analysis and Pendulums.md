---
updated_at: 2026-11-27T16:31:10.943-05:00
edited_seconds: 680
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
## Notation
We will refer to the corresponding time derivatives of position with dots (using Newton's Notation): 
$$
\begin{align}
\dot{x} = \frac{dx}{dt} \\
\ddot{x} = \frac{d^{2}x}{dt^{2}}
\end{align}
$$
The idea is that we want to rearrange an expression to: 
$$
\ddot{x} = -Cx \implies \omega=\sqrt{ C }
$$
(Which is what we had previously). 
## Vertical Spring (LEC) 
Consider a vertical spring, with a force constant $k$ hanging from the ceiling. A mass $m$ is attached to the bottom of the spring, what is the equation of motion of the mass? 

Let $y=0$ be equivalent to the equilibrium position. Let there be a mass $m$ applied, where this moves the spring some distance $y_{d}$, thus taking the force in terms of this system being in equilibrium, letting downwards be positive, then: 

$$
\begin{align}
m\ddot{y} = -ky + mg 
\end{align}
$$
Note we can't easily solve this, let $u= y - \frac{mg}{k}$, then: $y=u+ \frac{mg}{k}$ Note that with this substitution, $\dot{u} = \dot{y}, \ddot{u} = \ddot{y}$, thus: 

$$
\begin{align}
m\ddot{u}   & = -k\left( u + \frac{mg}{k} \right) + mg  \\
m\ddot{u}  & = -\frac{k}{m}u \\
\implies  u & =A\cos(\omega t + \phi) \\
\implies \omega & = \sqrt{ \frac{k}{m} } \\
y & = \frac{mg}{k} + A\cos(\omega t +\phi)
\end{align}
$$
Note that in this case, this means that our system oscillates around some value $\frac{mg}{k}$ in  terms of initial displacement. 

## Pendulum (LEC)
Consider a Pendulum with a point mass present, assuming that the string is of a length $L$, and the mass has some value $m$, with some force of $g$, then the torque applied by gravity is offered by the tangential component to the piece of rope applied; inline with the direction of pendulum. 

Thus, noting that this is provided to us by some value $mg\sin\theta$, then this applies some torque at some distance $L$. Note that if $\theta \approx$ small, then $\sin\theta \to \theta$ , thus: 

$$
\begin{align}
mg\theta L  & = I\alpha \\
I \ddot{\theta} & = mg\theta L & I = mL^{2} \\
\ddot{\theta} & = \frac{mg\theta L}{mL^{2}} \\
\ddot{\theta} & = \frac{g}{L}\theta \\
\implies  \omega  & = \sqrt{ \frac{g}{L} } \\
\implies \theta & = A\cos(\omega t+\phi)
\end{align}
$$
## Cork in Water 
Consider a Cylindrical Cork of mass $m$, density $\rho$, cross-sectional area $A$, and height $h$. If you displace it some initial distance and release it, it will bob up and down. What is the equation of motion of the cork? 

Recall that the Buoyancy force is given by some volume displaced: 
$$
Ad=V_{disp}
$$
And the entire cork's volume is given by 
$$
V_{total} = VH
$$
Noting that the forces applied are given by the Buoyant Force and the Force of Gravity. Noting that in equilibrium: 
$$
F_{b} = mg
$$
And for our cork, $m= \rho V_{total}$, and thus: 
$$
\begin{align}
\rho_{w}\cancel{ A }d\cancel{ g }  & = \rho \cancel{ A }h\cancel{ g } \\
d & =\frac{h\rho}{\rho_{w}}
\end{align}
$$
If ew have some vertical displacement downwards, this will be represented by :
$$
V_{displaced} = A(d+y)
$$
And thus the $$

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
