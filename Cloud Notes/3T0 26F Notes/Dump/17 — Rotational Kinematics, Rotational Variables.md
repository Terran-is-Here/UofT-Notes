---
updated_at: 2026-10-19T16:32:57.340-04:00
edited_seconds: 1040
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 17
Lecture Date: 2026-10-19
Week: 7
Created: October 14th 2026, 8:36:48 am
---
Hub: [[PHY180 Hub]]
Previous: [[16 — Center of Mass and Rockets]]
Next: [[18 — Moment of Inertia, Torque]]
> [!quote] Recommended Reading 
> University Physics 10.1 - 10.3
> Looking at [[2 — Vectors (Physics)#Polar Coordinates]] may also be useful. 
> [[6 — Uniform Circular Motion]] (for centripetal and constant velocity)
--- 
# Lecture Notes
## Rotational Kinematics (LEC) 
The following is a complete list of terms for Rotational Kinematics for reference. 
* A particle travels on a circular path of some radius $R$. 
* Angular position is defined by $\theta$
* Arc Length is defined by $s=\Delta\theta R$
* Angular velocity is defined by $\omega = \frac{d\theta}{dt}$ .
	* Tangential velocity is defined by $v_{t}=\omega r$
* Angular acceleration is defined by $\alpha=\frac{d\omega}{dt}=\frac{d^2\theta}{dt^2}$
	* Tangential acceleration is defined by $a_{t}=\alpha r$
* Centripetal Acceleration is defined by $a_{c} = \frac{v_{t}^2}{r}$. 
Sign convention wise; we call the counter clockwise direction is positive, and the clockwise direction as negative. In terms of $\alpha$, this would be defined in terms of how $\omega$ is changing (i.e. if $\omega$ is positive and speeding up, $\alpha$ is also positive). 

> [!theorem] Note
> Note that $\omega$ and $\alpha$ can be defined as the right hand rule; i.e. curling your right hight hand and thumb sticking up is the resultant direction of the vector $\omega$ or $\alpha$

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
> [!ila] In Lecture Addendum
> Note that if $\omega$ is in terms of radians per second; we can rewrite this into revolutions per minute as $\omega=\frac{2\pi}{T}$. 

Note however that for a rotational system; $\omega$ is always some constant; whilst the radius can vary. That is to say; a spinning thing will have the same angular velocity across the entire rotating object, but the radius may vary: 

> For instance consider if $r_{1} <r_{2} \implies r_{1}\omega < r_{2}\omega \implies v_{1}<v_{2}$

### Vector Angular Velocity
Note that $\omega$ is represented by some vector quantity; that is perpendicular to the plane formed by $\vec{v},\vec{r}$. Then: $\vec{v} = \vec{\omega}\times\vec{r}$. 

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

> [!ila] In Lecture Addendum
> Note that for any rotating rigid body, all rotational components are constant across the whole rotational body; independent of radii. 

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
\theta _{t}  & =\bar{\omega}t + \theta_{0} \tag{Equation 1.1}

\end{align}
$$

Note additionally that since $\alpha = \frac{d\omega}{dt}$; then: 
$$
\begin{align}
\alpha  & =\frac{d\omega}{dt} \\
\int_{t_{0}}^t\alpha\ dt  & =\int_{\omega_{0}}^{\omega t}d\omega \\
\alpha t & =\omega_{t}-\omega_{0}  \\
\omega_{t}  & = \alpha t + \omega_{0} \tag{Equation 1.2}
\end{align}
$$
Note that since $\omega=\frac{d\theta}{dt}$; integrating with respects once more to time (setting $t_{0}=0$). Note that since $\omega$ varies as a function of time; then we can set it as some $\alpha t+\omega_{0}$; then: 
$$
\begin{align}
\int_{t_{0}}^t\omega dt  & =\int_{\theta_{0}}^{\theta_{t}} d\theta \\
\int_{t_{0}}^t (\alpha t + \omega_{0})\ dt & =\theta_{t}-\theta_{0} \\
\frac{1}{2}\alpha t^2 + \omega_{0}t  +\theta_{0}& =\theta_{t} \tag{Equation 1.3}
\end{align}
$$
> Note that this expression is essentially equivalent to it's linear motion cousin. 

From here, we can solve for a time independent version of Equation 1.2 by solving for time in Equation 1.1: 
$$
\begin{align}
\frac{\omega_{t}-\omega_{0}}{\alpha}  & =t \\
\frac{1}{2}\alpha\left( \frac{\omega_{t}-\omega_{0}}{\alpha} \right)^2 + \omega_{0}\left(\frac{\omega_{t}-\omega_{0}}{\alpha}\right)  +\theta_{0}& =\theta_{t} \tag{Equation 1.3} \\
\frac{1(\omega _{t}^2 -2\omega_{t}\omega_{0}+\omega _{0}^2)}{2\alpha} + \frac{\omega_{0}(\omega_{t})-\omega_{0}}{\alpha}  & =\Delta\theta \\
\omega_{t}^2 -2\omega_{t}\omega_{0} + \omega_{0}^2 + 2\omega_{0}\omega_{t} - 2\omega_{0}^2 & =2a\Delta\theta \\
\omega_{t}^2 - \omega_{0}^2 & =2a\Delta\theta \\
\omega_{t}^2 & =\omega_{0}^2 +2a\Delta \theta \tag { Equation 1.4} 
\end{align}
$$
> [!caution] Note
>  These expressions are essentially the same structurally to their linear kinematics equivalents: 
>  $$\begin{array}{cc|cc}\text{Linear Kinematics} &  & \text{Rotational Kinematics} \\v_{t} =at + v_{0} &  & \omega_{t}=\alpha t + \omega_{0} \\\bar{v} = \frac{v_{0}+v_{t}}{2} &  & \bar{\omega} = \frac{\omega_{t}+\omega_{0}}{2} \\ x= \bar{v}t + x_{0} &  & \theta = \bar{\theta}t + \theta_{0} \\ x = \frac{1}{2}at^2 + v_{0}t + x_{0} &  & \theta = \frac{1}{2}\alpha t^2 + \omega_{0}t + \theta_{0} \\v_{f}^2 = v_{0}^2 + 2a\Delta x &  & \omega_{t}^2 = \omega_{0}^2 + 2\alpha\Delta\theta\end{array}$$
>  Since velocity and acceleration follow the same differential structure in a rotational and linear context. 

Since $\omega_{t}$ is always in terms of some radians/second; they need to be converted into revolutions per minute or vice versa if necessary. 
### Relating Angular and Translational Kinematics
Recall how earlier we defined $\theta=\frac{s}{r}$; that is as the ratio of an arc length $s$ and the radius of rotation $r$. 

Note however that $\vec{v}=\vec{\omega} \times \vec{r}$; then we can describe that: 
$$
\begin{align}
\omega  & = \frac{v_{t}}{r} \\
\alpha & = \frac{a_{t}}{r}
\end{align}
$$
Which makes sense; as both $v_{t}$, and $a_{t}$ are both tangential components of some component around some axis of rotation. Note however that for [[6 — Uniform Circular Motion|UCM]], we still have our own separate $a_{c}$ term defined by $v_{t}$; that is 
$$
a_{c} = \frac{v_{t}^2}{r} = \omega^2r
$$

