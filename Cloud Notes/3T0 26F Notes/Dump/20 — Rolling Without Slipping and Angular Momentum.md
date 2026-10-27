---
updated_at: 2026-10-26T21:57:36.278-04:00
edited_seconds: 850
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 20
Lecture Date: 2026-11-02
Week:
Created: October 25th 2026, 2:02:05 pm
---
Hub: [[PHY180 Hub]]
Previous: [[19 —Newton's Second Law for Rotation, Rotational Energy]]
Next:
> [!quote] Recommended Reading 
> Section 11.1 - 11.2 of University Physics
> [[14 — Momentum and Impulse]], [[15 — Conservation of Momentum, Collisions]]

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

That is; the higher the angle, the higher the corresponding required $\mu_{s}$ needed to stop an object from rolling without slipping. 
### Rolling Down with Slipping 
If in the case that our object *is* slipping, we can't use the equations that require $v_{p}=0$, as $v_{p}\neq0$. Taking the diagram from above once again: 
![[20 — Rolling Without Slipping and Angular Momentum-1793054075124.png|410]]

For our $x$ forces: 
* We have $mg\sin\theta$ (force of gravity) in the direction of movement, directly on the center of mass
* We also have $f_{f}=f_{n}\mu_{s} = \mu_{k}mg\cos\theta$, acting on a distance $r$ directly opposite the direction of movement. Fir t
For our $y$ forces: 
* We have our normal force and force downwards from gravity, defined as $mg\cos\theta=F_{n}$. 

Thus for the $x$ equilibrium: 
$$
\begin{align}
\sum F_{x}: mg\sin\theta - \mu_{k}mg\cos\theta  & = ma_{com} \\
a_{com} & =g(\sin\theta-\mu_{k}\cos\theta)
\end{align}
$$

And for the corresponding $\tau$ equilibrium: 
$$
\begin{align}
\sum \tau & : \mu_{k}mg\cos\theta = I\alpha \\
 & :r\mu_{k}mg\cos\theta  = \frac{mr^2}{2}\alpha \\
 & :\frac{2\mu_{k}g\cos\theta}{r^{}} = \alpha
\end{align}
$$
Note that, in contrast to Rolling Without Slipping, Rolling With Slipping has a term of $\mu_{k}$ involved in it's equations. 

## Conservation of Energy
Recall in an earlier note how we defined the total kinetic energy of an object as the sum of the translational kinetic energy and the rotational kinetic energy of an object :
$$
K = \frac{1}{2}mv^{2} + \frac{1}{2}I\omega^{2}
$$
If our object is rolling without slipping, then $v_{CM}=\omega r \to \frac{v_{CM}}{r}=\omega$, subbing it in, then: 
$$
\begin{align}
K  & = \frac{1}{2}mv^{2} + \frac{1}{2}I\left( \frac{v}{r} \right)^2  \\
 & =\frac{1}{2}mv^{2} + \frac{Iv^{2}}{2r^{2}}
\end{align}
$$
And the corresponding mechanical energy formula, assuming that energy is conserved and is solely involved in a potential manner, then: 
$$
E_{T} = \frac{1}{2}mv^{2} + \frac{1}{2} \frac{Iv^{2}}{r^{2}} + mgh
$$
## Angular Momentum 
Before we define Angular Momentum, recall how we defined the concept of momentum in a translational setting: 
$$\vec{p} =m\vec{v}$$The Angular equivalent of Translational Angular Momentum is defined as the following: 
$$
\vec{I} = \vec{r}\times \vec{p}
$$
Therefore: 
$$
|I| = |r||p|\sin\theta
$$
Note that $p=r\omega$. Note that we can relate the change in angular momentum to a term of force: 
$$
\begin{align}
\frac{d\vec{I}}{dt}  & = \vec{r} \times \frac{d\vec{p}}{dt} \\
 & =\vec{r}\times \vec{F}  & \frac{d\vec{p}}{dt} = \vec{F} \text{ (from NSL)} \\
\frac{d\vec{I}}{dt} & =\sum \vec{\tau}
\end{align}
$$
That is, the net change in angular momentum over time, is equivalent to the net torque applied onto an object. 