---
updated_at: 2026-10-26T18:33:58.509-04:00
edited_seconds: 250
course:
tags:
"Lecture #": 20
Lecture Date: 2026-10-25
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[19 —Newton's Second Law for Rotation, Rotational Energy]]
Next:

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Rolling Without Slipping
Consider a rotating body, such as a wheel, rolling on a surface. If, such a wheel is not *slipping* while rolling, then it's relative velocity in comparison to the ground is actually 0, then the actual applied force of friction is equivalent to $\mu_{s}$. 

Recall that we can relate the tangential velocity to the angular velocity of an object by $v_{t}=\omega r$. Note that by sign conventions (assuming that our object is moving towards the right), this actually has a negative term attached onto it. 

Consider now that our center of mass of the wheel (i.e. from it's axle) could also have some of it's own velocity; some $v_{cm}$. Thus we can describe the velocity of a *point* on the direct bottom of the wheel as the sum of both of these components: 
$$
v_{p} = -\omega r + v_{cm}
$$
If our wheel is not *slipping*, then $v_{p}=0$, and thus $v_{cm}=\omega r$. 

Note that we can both differentiate and integrate this: 
* Integrating with respects to time gives us $\Delta d = r\Delta\theta$, or $d=r\theta$, where $d$ is the distance travelled, $\theta$ is the angle revolved. In other words, the linear translation of a center of mass of a rotating wheel-like object is directly linked to the arc length contained by some angle $\theta$ on a circle with radius $r$. 
* Differentiating with respects to time gives us $a=r\alpha$, that is the acceleration of the rotating body is equivalent to the radius times the angular acceleration of our rotating object. 

### Rolling Down Without Slipping
Consider now an inclined plane, with an angle $\theta$ and a coefficient of static friction of $\mu_{s}$. Given a perfectly cylindrical roller with mass $m$, radius $r$, and thus a moment of inertia of $I=\frac{mr^2}{2}$. 
![[20 — Rolling Without Slipping and Angular Momentum-1793054075124.png|410]]

Setting our $x$ and $y$ axis to be inline with the surface then: 
For our $x$ forces: 
* We have $mg\sin\theta$ (force of gravity) in the direction of movement, directly on the center of mass
* We also have $f_{f}=f_{n}\mu_{s} = \mu_{s}mg\cos\theta$, acting on a distance $r$ directly opposite the direction of movement. 
For our $y$ forces: 
* We have our normal force and force downwards from gravity, defined as $mg\cos\theta=F_{n}$. 

Solving for the $x$ equilibrium, then: 
$$
\begin{align}
\sum F_{x} & =mg\sin\theta - \mu_{s}mg\cos\theta = ma
\end{align}
$$