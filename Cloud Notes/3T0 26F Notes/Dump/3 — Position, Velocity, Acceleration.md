---
updated_at: 2026-09-11T22:49:09.482-04:00
edited_seconds: 500
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 3
Date: 2026-09-11
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[2 — Vectors (Physics)]]
Next: [[4 — 1D Kinematics]]

> [!Quote] Textbook Chapters Discussed
> Chapters 3.1-3.3
> 


--- 
# Lecture Notes
# Pre-Lecture Notes
## Distance and Displacement
A key thing to note about acceleration, and motion in general—is that it is always based on a fixed(\*) point of reference. Displacement is generally defined as the change in position of an object: 
$$\Delta x = x_{t}- x_{0}$$
Where total displacement is equivalent to the sum of all individual displacements as expected. 
## Velocity & Speed

> [!theorem] Average Velocity
> The velocity of an object can be defined as the following: Let $t_{t},t_{0}$ be the values of time for when our object is at $x_{t}$ and $x_{0}$ respectively; then: 
> $$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{x_{t}-x_{0}}{t_{t}-t_{0}} \tag{1}$$
> Note that $\bar{v}$ **is** a vector and can be negative dependent on the positions of $\Delta x$. 

> [!theorem] Instantaneous Velocity
> Instantaneous Velocity (or Velocity) tells how how quickly an object is moving at a point on it's path; where the time between the two points on the above relation approaches 0. Redefine $x_{t}$ and $x_{0}$ as a function of $s(x)$ at $s(t_{t})$ and $s(t_{0})$ respectively.
> 
> We can define $t_{t}$ as some value $t_{0}$ with the different of $\Delta t$; that is $t_{t} - t_{0}=\Delta t$; therefore: 
> $$\bar{v} = \frac{\Delta x}{\Delta t} = \frac{s(t_{0} + \Delta t)-s(t)}{\Delta t}$$ 
> We now take the limit of $\Delta t$ as it approaches 0; granting us the definition of Instantaneous Velocity: 
> $$v(t) = \lim_{ \Delta t \to 0 } \frac{s(t_{0} + \Delta t)-s(t)}{\Delta t} = \frac{d}{dt}s(t)$$

>[!theorem] Speed and Instantaneous Speed
>Speed is a scalar value; and is calculated by dividing the total distance by the total time elapsed to travel that distance: 
>$$\bar{\text{Average Speed}} = \frac{\text{Total Distance}}{\Delta t}$$
>The instantaneous speed is defined by taking the magnitude of our instantaneous velocity: 
>$$\text{Instantaneous Speed } = |v(t)|$$
## Acceleration
> [!theorem] Average Acceleration
> Average Velocity is defined by the rate of change of velocity: take $v_{t}, v_{0}, t_{t}, t_{0}$ where the corresponding subscripts represent the term that they are related to; then the average acceleration of an object is defined by: 
> $$\bar{a} = \frac{\Delta v}{\Delta t} = \frac{v_{t}-v_{0}}{t_{t}-t_{0}}$$

> [!theorem] Instantaneous Acceleration
> Instantaneous Acceleration is also defined similarly to how we found Instantaneous Velocity: 
> $$\Delta t > 0, \bar{a} = \frac{\Delta v}{\Delta t} = \frac{v(t_{t} + \Delta t) - v(t)}{\Delta t}$$
> $$a(t) = \lim_{ \Delta t \to 0 } \frac{v(t_{t} + \Delta t) - v(t)}{\Delta t} = \frac{d}{dt}v(t)$$

Note that acceleration is also a vector; however it must not share a direction with velocity. It may not also change the magnitude of the velocity of an object; and could also simply be inducing a turning motion on our object. 