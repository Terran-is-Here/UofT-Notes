---
updated_at: 2026-10-17T22:11:45.587-04:00
edited_seconds: 390
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 17
Lecture Date: 2026-10-14
Week: 7
Created: October 14th 2026, 8:36:48 am
---
Hub: [[PHY180 Hub]]
Previous: [[16 — Center of Mass and Rockets]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics 10.1 - 10.3
> Looking at [[2 — Vectors (Physics)#Polar Coordinates]] may also be useful. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Angular Velocity
For objects in a Circle, we can define the distance as some arc length: 
$$
s=\theta r
$$
Where $\theta$ is in Radians; then $s$ is some measure with distance; recall that if we differentiate distance as a function of time; and noting that $r$ is some constant; then: 
$$
\frac{ds}{dt} = r\frac{d\theta}{dt}
$$
We define the concept of *angular velocity* as the instantaneous rate of change of some circular angle; that is: 
$$
\frac{\Delta \theta}{\Delta t}=\frac{d\theta}{dt} = \omega
$$
Where $\omega$ is some value of $rad$/$s$. With this; and noting that $\frac{ds}{dt}=v$; then: 
$$
v = r\omega
$$
Note however that for a rotational system; $\omega$ is always some constant; whilst the radius can vary. That is to say; a spinning thing will have the same angular velocity across the entire rotating object, but the radius may vary: 

> For instance consider if $r_{1} <r_{2} \implies r_{1}\omega < r_{2}\omega \implies v_{1}<v_{2}$

### Vector Angular Velocity
Note that $\omega$ is represented by some vector quantity; that is perpendicular to the plane formed by $\vec{v},\vec{r}$. Then: $\vec{v} = \vec{\omega}-\vec{r}$. 

We define $\omega$ by the right hand rule; where it points upwards in some clockwise rotation; and downwards in a counter clockwise direction. 
### Angular Acceleration
Taking the derivative of $\omega$; we arrive at the Angular Acceleration term $\alpha$: 
$$
\lim_{ \Delta t \to 0 } \frac{\Delta\omega}{\Delta t} = \frac{d\omega}{dt} = \alpha
$$
Note that then; 
$$
\vec{a} = \vec{\alpha}\times \vec{r}
$$
Where $a$ in this case represents the *tangential* acceleration of our system; and is the corresponding cross product of $\alpha$ and $\vec{r}$. Note that this would technically be colinear (or at minimum antiparallel) with some $\vec{v}$; which can be expressed from above. 

## Angular Kinematics Expressions
Similarly to how we derived the kinematics equations for [[4 — 1D Kinematics|1D Kinematics]]; we can derive a *shockingly* similar set of equations in terms of angular velocity. 

Assuming that $\bar{\alpha}=\alpha$; that is Angular Acceleration is some constant; then we can define some constant angular velocity as: 
$$
\bar{\omega} = \frac{\omega _{t} + \omega_{0}}{2} =
$$
Note that since $\bar{\omega}=  \frac{\Delta\theta}{\Delta t}$; then: 
$$
\begin{align}
\bar{\omega}  & = \frac{\Delta\theta}{\Delta t}  \\
\bar{\omega}\Delta t  & = \Delta\theta  & \Delta t = t_{f}-t_{0}, t_{0}=0 \\
\bar{\omega}t  & =\theta_{t}-\theta_{0} \\
\theta _{t}  & =\bar{\omega}t + \theta_{0}

\end{align}
$$

Note additionally that since $\alpha = \frac{d\omega}{dt}$; then: 
$$
\begin{align}
\alpha  & =\frac{d\omega}{dt} \\
\int_{t_{0}}^t\alpha\ dt  & =\int_{\omega_{0}}^{\omega t}d\omega \\
\alpha t & =\omega_{t}-\omega_{0}  \\
\omega_{t}  & = \alpha t + \omega_{0}
\end{align}
$$
From here; then note that $\omega _t = \frac{d\theta}{dt}$, integrating once more then: 
$$
\begin{align}
\omega_{t}  & = \alpha t + \omega_{0} \\
\int_{t_{0}}^t\omega_{t} \ dt & = \int_{t_{0}}^t\alpha t + \omega_{0} \ dt \\

\end{align}
$$