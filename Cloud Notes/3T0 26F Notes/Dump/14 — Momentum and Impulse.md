---
updated_at: 2026-10-09T13:58:29.792-04:00
edited_seconds: 300
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 14
Lecture Date: 2026-10-07
Week: 5
---
Hub: [[PHY180 Hub]]
Previous: [[13 — Conservation of Energy, Stability]]
Next:
> [!quote] Recommended Reading 
> 9.1 - 9.3 (University Physics)
--- 
# Lecture Notes

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
$$
\vec{J} = \int _{t_{0}}^{t^1}\vec{F}(t)dt
$$
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

> Relating Back to Newton
> Note that if 
