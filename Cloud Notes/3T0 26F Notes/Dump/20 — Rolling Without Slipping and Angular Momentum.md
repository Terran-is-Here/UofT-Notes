---
updated_at: 2026-11-07T12:25:17.530-05:00
edited_seconds: 1340
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
Next: [[21 — Conservation of Angular Momentum, Gyroscopic Precession]]
> [!quote] Recommended Reading 
> Section 11.1 - 11.2 of University Physics
> [[14 — Momentum and Impulse]], [[15 — Conservation of (Translational) Momentum, Collisions]]

--- 
# Lecture Notes
Lecture started up with a question: 

> A 0.50kg basketball rolls around the ground at 1m/s. What is the total kinetic energy?

Recall that $I=\frac{2}{3}MR^{2}$; (hollow sphere), then the total kinetic energy is given to us by the following: 
$$
\frac{1}{2}mv^{2} + \frac{1}{2}I\omega^{2}
$$
Recall, $v_{t} = \omega r \to \omega = \frac{v_{t}}{r}$, then: 
$$
\begin{align}
 & =\frac{1}{2}mv^{2} + \frac{1}{2}\left( \frac{2}{3}Mr^{2} \right)\left( \frac{v^{2}}{r^{2}} \right) \\
 & =\frac{1}{2}mv^{2} + \frac{1}{3}mv^{2} = \frac{5}{6}mv^{2} \\
 & =\frac{5}{6}mv^{2} = \frac{5}{6}(0.5)(1) = \frac{5}{12}\approx 0.42\text{J}
\end{align}

$$


## Rolling Without Slipping (LEC) 
Now we want to derive an expression for the acceleration due to rolling without slipping. 

> What is $a$ of a sliding object down a ramp with an angle $\theta$ without friction? 

We can trivially see that the acceleration would be some term $g\sin\theta$ (from inclined plane questions that we have done before). 

> What is the acceleration of a *rolling* object down a ramp with an an angle $\theta$ with friction? 

Consider the forces in the x-direction aligned with the corresponding plane of the incline, then we see that: 
$$
mg\sin\theta -f_{f} = ma
$$

Consider now the Torque. Let $I=[X]mr^{2}$, where $[X]$ is some dimensionless constant applied in terms of the Moment of Area; then considering the torque: 
$$
f_{f}r = I\alpha
$$
Let $\alpha = -\frac{a}{r}$ (in terms of our sign conventions, then) $r\alpha = -a$, then: 
$$
f_{f}r^{2} = -Ia
$$
Note that $f_{f} = \mu_s mg\cos\theta$, then solving for acceleration, then substituting for force of friction, then: 
$$
f_{f} = -\frac{Ia}{r^{2}}
$$
Then: 
$$
\begin{align}
mg\sin\theta -\frac{Ia}{r^{2}}  & = ma \\
mg\sin\theta- \frac{[X]mr^{2}a}{r^{2}}  & =ma \\
g\sin\theta - [X]a & =a \\
g\sin\theta  & =(1+[X])a \\
\frac{g\sin\theta}{(1+[X])}  & =a
\end{align}
$$
Then, to solve for the angular acceleration, recall that $\alpha=-\frac{a}{r}$, then: 
$$
-\frac{g\sin\theta}{r(1+[X])} = \alpha
$$
> [!ila] In Lecture Addendum
> By generalizing $I$ to any set of $[X]mr^{2}$ (as we know this is what normally arises dimensionally for it, where we obtain some value of $mr^{2}$ and some corresponding dimensionless constant $[X]$), then we see that this actually applies to significantly more equations than what we solved in the pre lecture notes. 
> 
> Note that in our notes, we have the Moment of Inertia for a solid  disk as $I=\frac{mr^{2}}{2}$, then we see $[X]=\frac{1}{2}$, then following the equation above, we arise at the same equation that we did previously: 
> $$\frac{g\sin\theta}{1.5} = \frac{2g\sin\theta}{3}=a$$
### Extension
Since we now know $a$; we can back substitute to solve for $\mu$: 
$$
\begin{align}
\mu mg\cos\theta  & = \frac{Ia}{r^{2}}  \\
\mu mg\cos\theta  & =\frac{[X]mr^{2}}{r^{2}}\left( \frac{g\sin\theta}{(1+[x])} \right) \\
 \mu \cos\theta & =\frac{[X]\sin\theta}{1+[x]} \\
 \mu & =\frac{[X]\tan\theta}{1+[X]}
\end{align}

$$

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
\alpha = -\frac{2}{3r}g\sin\theta
$$
Solving for the condition where the wheel does *not* slip, then we have to see that $f_{f}\leq \mu _s N$, retaking our earlier force of friction term way above from our torque expression, we see that: 
$$
\begin{align}
f_{f}  & =\frac{I}{r^{2}}a_{t}  & a_{t} = \frac{2}{3}g\sin\theta\\
 & =\frac{I}{r^{2}}\left( \frac{g\sin\theta}{1 + \frac{I}{mr^{2}}} \right)  & I=\frac{mr^{2}}{2} \\
 & =\frac{I}{r^{2}}\left( \frac{g\sin\theta}{1.5} \right) = \frac{I}{r^{2}}\left( \frac{2}{3}g\sin\theta \right)
\end{align}
$$
Plugging this into $f_{f}\leq \mu_{s}N$, then: 
$$
\begin{align}
\frac{I}{r^{2}}\left( \frac{2}{3}g\sin\theta \right) & \leq \mu_{s}mg\cos\theta \\
\frac{I}{r^{2}mg\cos\theta}\left( \frac{2}{3}g\sin\theta \right) & \leq \mu_{s} \\[1.5em]\text{ note that }  I=\frac{mr^{2}}{2} \implies \frac{1}{2I}=\frac{1}{mr^{2}}\\[1.5em]
\frac{I}{2Ig\cos\theta}* \frac{2}{3}g\sin\theta =\frac{1}{3}\tan\theta & \leq \mu_{s}

\end{align}
$$

That is; the higher the angle, the higher the corresponding required $\mu_{s}$ needed to stop an object from rolling without slipping. 
### Rolling Down with Slipping 
If in the case that our object *is* slipping, we can't use the equations that require $v_{p}=0$, as $v_{p}\neq0$ (meaning that we can't directly relate the two terms above) Taking the diagram from above once again: 
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
> [!caution] Note
> Since $I=rp \sin\theta$, note that $p=mv_{t}$, and $v_{t}=\omega r$, then
> $$I=rp=rm\omega r = \omega mr^2 = \omega I$$



Note that $p=r\omega$. Note that we can relate the change in angular momentum to a term of force: 
$$
\begin{align}
\frac{d\vec{I}}{dt}  & = \vec{r} \times \frac{d\vec{p}}{dt} \\
 & =\vec{r}\times \vec{F}  & \frac{d\vec{p}}{dt} = \vec{F} \text{ (from NSL)} \\
\frac{d\vec{I}}{dt} & =\sum \vec{\tau}
\end{align}
$$
That is, the net change in angular momentum over time, is equivalent to the net torque applied onto an object. For a system composed of multiple particles, the total angular momentum is equivalent to the total angular momentum of all particles present: 
$$
\begin{align}
L = I_{1} + I_{2} + \dots + I_{n} = \sum_{i=1}^{N} I_{i}
\end{align}
$$
If each particle is subject to a net torque, then: 
$$
\begin{align}
\frac{d\vec{L}}{dt}  & = \sum \frac{d\vec{I}}{dt}  \\
\frac{d\vec{L}}{dt} & =\sum_{i=1}^{N} \vec{\tau_{i}}
\end{align}
$$
### Rigid-Body Angular Momentum
Consider now a rigid body composed of a set of mass segments, some $\Delta m_{i}$. These mass segments would be some distance $R_{i}$ from the rotational center; as well as having a position vector $\vec{r_{i}}$ from the origin of an arbitrary coordinate system. 

Let us state that our object is rotating across the $z$ axis, that is it has some $+\omega$ around the $z$ axis, then we note that from our above definition, that given the velocity of the mass segment $\Delta m_{i}v_{i}$, then the following is it's corresponding rotational momentum: 
$$
I = r_{i}\Delta m_{i}v_{i}\sin\theta
$$
Note that by definition, the velocity of a particle is inherently (well, in this case, inherently) perpendicular with the axis of rotation, then $\theta=90\degree$ and thus $\sin\theta= 1$: 
$$
I = r_{i}\Delta m_{i}v_{i}
$$
Consider now that, for all mass segments present on a rotating rigid body, all mass segments that *do not inherently lie* on the axis of rotation, will have a corresponding mass-segment pair travelling in the opposite direction, which cancels out their corresponding angular momentum. This only applies if cylindrical symmetry applies. 

Thus, we consider now the sum of all the angular momenta along the axis of rotation, then: 
$$
\begin{align}
L  & = \sum_{i=1}^{N} r_{i}\Delta m_{i}v_{i} \\
 & =\sum_{i=1}^{N} r_{i}\Delta m_{i}\omega r = \omega\sum_{i=1}^{N} \Delta m_{i}r_{i}^2 \\
 & =\omega I
\end{align}
$$
Since $\sum mr^2 =I$. 