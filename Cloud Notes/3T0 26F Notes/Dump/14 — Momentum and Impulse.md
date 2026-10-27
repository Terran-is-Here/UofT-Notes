---
updated_at: 2026-10-10T21:28:45.211-04:00
edited_seconds: 790
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 14
Lecture Date: 2026-10-09
Week: 5
Created: October 7th 2026, 11:22:24 pm
---
Hub: [[PHY180 Hub]]
Previous: [[13 — Conservation of Energy, Stability]]
Next:[[15 — Conservation of (Translational) Momentum, Collisions]]
> [!quote] Recommended Reading 
> 9.1 - 9.3 (University Physics)
--- 
# Lecture Notes
## Momentum (LEC) 
Momentum is a property of *moving* things; that is inertia in motion. It's defined as the velocity of an object multiplied by it's mass: 
$$\vec{p} = m\vec{v}$$
Or, as a scalar, $p=mv$. Note that since $\vec{p}$ is a vector; unlike energy, it is a vector and *has* direction. 
> [!ila] Interesting Realization
> If $p=mv$, $pv = mv^2 \implies pv=2E_{k}$, Seemed interesting. 
> $$\frac{p^2}{2m}=\frac{pv}{2}=E_{k}$$
> > What am I saying; this is literally in [[11 — Work and Kinetic Energy]] (Aries, I mean not exactly but something like it.) 

## Collisions
There's generally two types of momentum situations that we need to consider: Explosion questions ($p_{t}=0$ / starting from rest), and Collision questions (not starting from rest). **Conservation of Momentum** always holds true. 

> Elastic Collisions: 
> Kinetic Energy remains constant across a collision. 

> Inelastic Collision:
> > Perfectly: 
> > Objects stick together (minimizes kinetic energy) 
> 
> > Partially Inelastic: 
> > Objects don not stick together, but kinetic energy is lost. 
> 
> > Explosive Collision: 
> > More kinetic energy is gained after the collision (due to some external source) 

## Impulse-Momentum Theorem 
Impulse is Related to force: Impulse is the integral of Force over *time* (note, work is the integral of force over *distance*): 
$$
\begin{align}
d\vec{J}&=\vec{F}dt \\
\vec{J} &= \int_{t_{0}}^{t_{1}}\vec{F}dt \\
\vec{J} &= \vec{F}_{avg}\Delta t & \text{Where } \vec{F}_{avg} = \frac{1}{\Delta t}\int_{t_{0}}^{t_{1}}F(t)dt
\end{align}
$$
Note that with $F\Delta t=J$, then $J=\Delta p$; which is the equivalent change in Momentum for the system with respects of a timespan. 
> [!ila] In Lecture Idea
> Newton's Second Law can be presented as a change of momentum with respects to time:
> $$F_{net}=\frac{dp}{dt}$$
> Can be derived, though we already did that derivation from below. 

---
# Pre-Lecture Notes
## Momentum
Momentum is generally defined as the product of the mass of a particle and it's corresponding velocity: 
$$
\vec{p} = m\vec{v}
$$
Where the corresponding units are actually in terms of $N*m$. Differentiating this with respects to an infinitesimal time gives us an interesting property: 
$$
\begin{align}
\frac{\vec{p}}{dt}&=  \frac{m\vec{v}}{dt} \\
\frac{\vec{p}}{dt} &=m\vec{a} & \text{since }\frac{\vec{v}}{dt} = \vec{a} \\
\frac{\vec{p}}{dt} = \vec{F}
\end{align}
$$
We define $\frac{\vec{p}}{dt}$ as an interesting quantity: Impulse, notated as $\vec{J}$. 
## Impulse 
Instantaneous impulse is defined as the following: 
$$d\vec{J} = \vec{F(t)}dt$$
Where the force is the force applied on an object over some time interval; integrating this gets us the total impulse over that corresponding interval: 

> [!theorem] Impulse over an Interval
> For a force applied between $t_{0},t_{1}$, the impulse over that entire interval is given by the following relation. 
> $$\boxed{\vec{J} = \int _{t_{0}}^{t^1}\vec{F}(t)dt}$$
> Note that since (later on), $J=\Delta p$, then 
> $$\Delta p = \int _{t_{0}}^{t^1}\vec{F}(t)dt$$

^39f602

Note that we can redefine this in terms of an *average force*. Given some function $f(x)$, it's average can be defined as some integral: 
$$
f_{av}(x) = \frac{1}{\Delta x}\int_{x_{0}}^{x_{1}}f(x) dx
$$
Applying this then: 
$$
\begin{align}
\vec{F_{av}(x)} &= \frac{1}{\Delta t}\int_{t_{1}}^{t_{2}}F(t)dt \\
\Delta t\vec{F}_{av}(x) &= \int_{t_{1}}^{t_{2}}F(t)dt = \vec{J} \\
& \boxed{\vec{J} = \Delta t\vec{F}_{av}(x)}
\end{align}
$$
Note that if $\vec{F}_{av}=\bar{F} \implies \vec{F}=m\vec{a}$, then: 
$$\begin{align}\vec{J} =m\vec{a}\Delta t = m(v_{t}-v_{0}) = m\Delta v\end{align}$$
Where $\Delta v$ is the change in $v$ over $\Delta t$. This actually has another way that we can write Impulse: It is the rate of change of *momentum*: 
$$
\begin{align}
\vec{J} &= m\Delta v \\
\vec{J} &= \Delta p
\end{align}
$$

> [!theorem] Relating Back to Newton
> Take the following relation; then: $$\vec{J}=\Delta p = \Delta t\vec{F}_{av}$$
> $$\frac{\Delta p}{\Delta t}=\vec{F}_{av}$$
> Taking the limit of $\Delta t \to dt$; then $\Delta p \to dp$; then: 
$$ma=\frac{dp}{dt}=F$$
> Or in other words, force is actually the instantaneous rate of change of momentum. 
> > This can be seen from $F=ma$ too, since $a=\frac{dv}{dt}$, then 
> > $$\begin{align}F&=ma \\&=m * \frac{dv}{dt} \\&=\frac{m*dv}{dt} \\F&=\frac{dp}{dt}\end{align}$$
## Conservation of Momentum
Conservation of Momentum is another conservatory principle in physics, however it applies more generally to more states over our current definition of the conservation of Energy. 

> [!Theorem] Conservation of Momentum
> In a closed system where the **net force** is zero (as a force imparts a change in momentum); the total momentum within a system remains constant. $$p_{a 0} + p_{b 0} = p_{a t} + p_{b t}$$
> This applies for any amount of dimensions; where the net momentum in an $n$-dimensional setup can be broken up  $n$ $1d$ linear systems. 
> > If external forces are applied; this increases the net amount of momentum present within the system; we could use the equations that we have above that we defined in the earlier sections of this lecture. 
> 
> > This can be used to derive other equations (in the next note) pertaining to Elastic and Inelastic collisions; since some $p_{a}=m_{a}v_{a}$, and $m_{a}$ normally does not change (unless it's an inelastic collision).
> 
> > [!ila] In Lecture Addendum
> > **Whatever these momentums** add up to is vital. In explosion problems, this is normally $0$, though not always. 

Note that this principle applies *generally for any closed system*; even in cases in which the kinetic energy of a system may decrease, such as cases of Inelastic Collisions. 


