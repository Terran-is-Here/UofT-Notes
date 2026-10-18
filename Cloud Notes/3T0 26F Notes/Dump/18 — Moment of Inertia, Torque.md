---
updated_at: 2026-10-18T17:06:54.405-04:00
edited_seconds: 270
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 18
Lecture Date: 2026-10-22
Week: 7
---
Hub: [[PHY180 Hub]]
Previous: [[17 — Rotational Kinematics, Rotational Variables]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics, 10.4-10.5
> [[11 — Work and Kinetic Energy]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Rotational Kinetic Energy
Recall that we defined Kinetic Energy as the following in the previous note: 
$$
K_{T}= \frac{1}{2}mv^2
$$
Note however that this was defined for a sole point mass. Also consider that, in a rotational body; there might exist multiple particles present on the object that's rotating with various radii and masses pertaining to the center of rotation. We can also observe that, for a rotational system; while the tangential velocity may differ with radius; the same angular velocity is shared across the entire rotating object. 

Recall that: 
$$
v_{t} = \omega r
$$
Thus; plugging this into the equation above that we had earlier: 
$$
\begin{align}
K  & = \frac{1}{2}m(\omega r)^2 = \frac{1}{2}mr^2\omega^2
\end{align}
$$
Consider the expression/case that we had earlier; that for an object with multiple particles of varying masses and radii from the axis of rotation, that their corresponding $v_{t}$ term will differ. Since we know that $\omega$ is some constant across the entire rotating body; we simply need to take the sum of all of the kinetic energies present per particle in order to get the rotational kinetic energy of an object: 
$$
K = \frac{1}{2}m_{1}r_{1}^2\omega^2 +  \frac{1}{2}m_{2}r_{2}^2\omega^2 +  \dots +  \frac{1}{2}m_{n}r_{n}^2\omega^2 +  
$$
Note that the $\frac{1}{2}\omega ^2$ term is present in all of these; thus we can express it as the following equation: 
$$
K_{R} = \frac{1}{2}\left[ \sum_{j=1}^Nm_{j}r_{j}^2 \right]\omega^2
$$
Where we define the term inside; $\sum_{j=1}^N m_{j}r_{j}^2$ as the *Moment of Inertia* of our object; a relative measure of the difficulty to rotate; in terms of $kg\cdot m^2$: 

> [!theorem] Moment of Inertia (Descretized)
> The moment of Inertia of a rotating object with discrete particles is defined as the following expression: 
> $$I = \sum_{j=1}^Nm_{j}r_{j}^2$$
> Where $I$ is a measure of the object's rotational inertia; that is to say how hard it is to change it's rotational velocity. 

Then; our above expression for rotational kinetic energy becomes the following: 
$$
K_{R} = \frac{1}{2}I\omega^2
$$
Note that from this, we can now extend our concept of the total kinetic energy of a system to now include both Rotational and Kinetic Energy: 
$$
K = K_{T} + K_{R} = \frac{1}{2}Mv^2 + \frac{1}{2}I\omega^2 = \frac{1}{2}(Mv^2 + I\omega^2)
$$
> [!theorem] Moment of Inertia (Integral) 
> The *moment* of inertia of a continuous object can be found by realizing that; for any infinitesimal segment of an object (i.e. $dm$), the radius will remain the same; thus we can define $I$ by taking smaller and smaller cuts of $m_{j}$ in the expression we defined above; up to some $dm$; then: 
> $$I = \int r^2 dm$$
> Where $dm$ represents some component of the mass distribution of the ob