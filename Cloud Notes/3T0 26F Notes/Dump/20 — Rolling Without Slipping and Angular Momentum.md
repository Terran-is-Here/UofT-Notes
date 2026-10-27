---
updated_at: 2026-10-26T21:33:35.062-04:00
edited_seconds: 520
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
* We also have $f_{f}=f_{n}\mu_{s} = \mu_{s}mg\cos\theta$, acting on a distance $r$ directly opposite the direction of movement. Fir t
For our $y$ forces: 
* We have our normal force and force downwards from gravity, defined as $mg\cos\theta=F_{n}$. 

Solving for the $x$ equilibrium, then: 
$$
\begin{align}
\sum F_{x} & =mg\sin\theta - f_{f}= ma \\
 & =g\sin\theta - \frac{f_{f}}{m} = a
\end{align}
$$
Solving for the torque/moment equilibrium, then: 
$$
\begin{align}
\sum \tau = f_{f}r= I\alpha
\end{align}
$$
Since $\alpha r = a_{t}$, then: 
$$
\begin{align}
f_{f}r^{2}  & = Ia_{t} \\
f_{f} & =\frac{Ia_{t}}{r^2}
\end{align}
$$
We can plug this back in to our earlier equation, then: 
$$
\begin{align}
g\sin\theta - \frac{Ia_{t}}{mr^2}  & = a_{t} \\
g\sin\theta & =a_{t} + \frac{Ia_{t}}{mr^2} = \left( 1 + \frac{I}{mr^2} \right)a_{t} \\
 \frac{g\sin\theta}{1 + \frac{I}{mr^2}}& =a_{t}  & I=\frac{mr^2}{2} \\
  a_{t} & =\frac{g\sin\theta}{1 + \frac{mr^2}{2mr^2}} = \frac{g\sin\theta}{1.5} =\frac{2}{3}g\sin\theta
\end{align}
$$
Then: 
$$
\alpha = \frac{2}{3r}g\sin\theta
$$
Solving for the condition where the wheel does *not* slip, then we have to see that $f_{f}\leq \mu _s N$, retaking our earlier force of friction term: 
$$
\begin{align}
f_{f}  & =\frac{I}{r^{2}}a_{t} \\
 & =\frac{I}{r^{2}}\left( \frac{g\sin\theta}{1 + \frac{I}{mr^{2}}} \right)  & I=\frac{mr^{2}}{2} \\
 & =\frac{I}{r^{2}}\left( \frac{g\sin\theta}{1.5} \right) = \frac{I}{r^{2}}\left( \frac{2}{3}g\sin\theta \right)
\end{align}
$$
Plugging this into $f_{f}\leq \mu_{s}N$, then: 
$$
\begin{align}
\frac{I}{r^{2}}\left( \frac{2}{3}g\sin\theta \right) & \leq \mu_{s}mg\cos\theta \\
\frac{I}{r^{2}mg\cos\theta}\left( \frac{2}{3}g\sin\theta \right) & \leq \mu_{s} \\[1.5em]  I=\frac{mr^{2}}{2} \implies \frac{1}{2I}=\frac{1}{mr^{2}}\\[1.5em]
\frac{I}{2Ig\cos\theta}* \frac{2}{3}g\sin\theta =\frac{1}{3}\tan\theta & \leq \mu_{s}

\end{align}
$$

