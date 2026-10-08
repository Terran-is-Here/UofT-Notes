---
updated_at: 2026-10-08T17:28:13.140-04:00
edited_seconds: 810
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 6
Lecture Date: 2026-09-21
Week: 3
created:
Created: September 17th 2026, 2:52:05 pm
---
Hub: [[PHY180 Hub]]
Previous: [[5 —2D Kinematics]]
Next: [[7 — 1st and 2nd Laws of Newton]]

> [!quote] Relevant Textbook Sections 
> 4.4 — 4.5
> 
--- 

# Lecture Notes

# Pre-Lecture Notes
## Uniform Circular Motion
Uniform Circular Motion deals with the concept of objects rotating around some center with a constant velocity. Note that while the *magnitude* of the velocity vector may remain constant, *its direction* is changing constantly. 
### Tangential Velocity
Note that with Circular Motion, we can also define the Tangential Velocity of a point as some function if it's angular velocity and the radius of rotation. Recall the definition of Arc Length: 
$$
a = \theta r
$$
Where $\theta$ is defined in Radians; then it comes to follow that we can define velocity as some value of $\frac{\Delta\theta}{\Delta t}$, or in other words $\omega$: 
$$
v_{t} = \omega r
$$
Where $\omega$ is in terms of *radians* per second (or some other time unit). 

### Centripetal Acceleration
Take a circle with a point some distance $\vec{r}$ away from the origin pointing towards some point on the circumference, then: 
$$
|\vec{r}(t)| =|\vec{r}(t+h) | 
$$
Note as well, that the velocity of some point at the circumference is also given as: 
$$
|\vec{v}(t)| = |\vec{v}(t+h)| 
$$
Then: 
$$
\Delta \vec{r} = \vec{r}(t+h ) - \vec{r}(t)
$$
$$
\Delta \vec{v} = \vec{v}(t+h) - \vec{v}(t)
$$
Based on $\vec{v}\perp \vec{r}$, this implies that the triangle $\vec{v}(t), \vec{v}(t+h), \Delta \vec{v}$ and $\vec{r}(t), \vec{r}(t+h), \Delta \vec{r}$ are similar if $\Delta \theta$ is some really small value, that is the below statements hold true if $\Delta \theta \to 0$, that is: 
$$
\frac{\Delta v}{\vec{v}} = \frac{\Delta r}{\vec{r}} \implies \Delta v = \frac{\vec{v}\Delta r}{\vec{r}}
$$
Or, without vector notation, then 
$$
\Delta v = \frac{v\Delta r}{r}$$
![[6 — Rotational Kinematics-1789768786583.webp|557x326]]

To solve for a term of *centripetal acceleration*, we can take the derivative of our term: 
$$
a = \frac{\Delta v}{\Delta t} = \frac{1}{\Delta t}\left( \frac{v\Delta r}{r} \right) = \frac{v}{r}\left( \frac{\Delta r}{\Delta t} \right) = \frac{v^2}{r}
$$
That is: 
> [!theorem] Centripetal Acceleration
> $$a_{c} = \frac{v^2}{r}$$
> Where $a_{c}$ always points to the center of the circle of rotation, that is it points radially inwards **always**. It can also be termed as a form of **Radial** acceleration.
### Equations of Motion
To describe the equations of motion of our particle, we can describe it through $\vec{r}$, and is defined below: 

> [!theorem] Equation of Motion of Circular Motion
> $$\vec{r} = \hat{i} A\sin(\omega t)+\hat{j}A\cos(\omega t)$$
> Where $\omega$ is angular velocity, in terms of $\frac{rad}{s}$ (or some rotation over time value), and $A=r=|\vec{r}|$. 

Note that this is an equation for a term of *displacement*, then we can differentiate it once for velocity, and twice for acceleration respectively. Differentiate with respects to *time*. 

> [!theorem] Velocity Equation (from above) 
> $$\vec{v}(t) = \frac{\Delta \vec{r}}{\Delta t} = \hat{i}\omega A\cos(\omega t) - \hat{j}\omega A \cos(\omega t)$$

> [!theorem] Acceleration Equation (from above) 
> $$\vec{a}(t) = \frac{\Delta \vec{v}(t)}{\Delta t} = -\hat{i}\omega^2A\sin(\omega t) - \hat{j}\omega^2 A\cos(\omega t)$$

Note that our earlier definition still holds; $\vec{v}(t)$ is tangent to the circle; and $\vec{a}$ is equivalent to our centripetal acceleration. 
## Non-Uniform Circular Motion
If our *tangential* velocity is non-constant, then this implies that we have some *acceleration* also tangent to the circle that affects our rotating object, that is: 
$$
a_{t} = \frac{d|\vec{v}|}{dt}
$$
Note that if $a\neq 0$, then $v$ will change. If $a_{c}$ is constant; then:
$$
a_{c} = \frac{v^2}{r}
$$

For this to remain true, $r$ must scale to balance out the change in $\vec{v}$, meaning that our object's radius will proportionally increase or decrease respectively. Note that if tangential acceleration is present, then the overall acceleration of our point (assuming solely $a_{c}$ and $a_{t}$) is defined by the following: 
$$
\vec{a}=\vec{a}_{c}+\vec{a}_{t}
$$
Note that $a_{c} \perp a_t$; ergo $|\vec{a}| = \sqrt{ a_{c}^2 + a_{t}^2 }$. With $a_{t}\neq0$, $a$ will no longer be directly pointing towards the center. 
## Relative Motion
The rule of thumb for relative motion is to sum up the vector subscripts to get it to a term that results in the reference frame basis that we are looking for: recall that $\vec{AB} = -\vec{BA}$. 

Relative Motion can be generally defined by the Galilean Transformation of Velocity: 
$$
\vec{v}_{CB} = \vec{v}_{CA} + \vec{v}_{AB}
$$
i.e. Combine vector subscripts. Note that the Galilean Transformation does not hold under Relativistic speeds, instead the Lorentz Transform is the value which holds. 