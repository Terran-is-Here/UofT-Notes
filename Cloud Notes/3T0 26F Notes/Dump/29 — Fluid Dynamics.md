---
updated_at: 2026-11-22T18:55:15.588-05:00
edited_seconds: 620
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 29
Lecture Date: 2026-10-26
Week:
Created: October 30th 2026, 4:06:52 pm
---
Hub: [[PHY180 Hub]]
Previous: [[28 — Pascal's and Archimedes' Principle and Buoyancy]]
Next: [[30 — Simple Harmonic Motion]]
> [!quote] Recommended Reading 
> University Physics Sections 14.6 - 7
> [[11 — Work and Kinetic Energy]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Bernoulli's Equation
Recall from earlier how we said that, with the concept of continuity of flow: 

$$
Q_{1}=Q_{2}
$$

For some mass flow rate, that is: 

$$
A_{1}v_{1} = A_{2}v_{2}
$$

If $A_{1} \neq A_{2}$, then $v_{1} \neq v_{2}$. Note as well that at the point in which a pipe's cross-sectional area changes, the pressure also changes due to the change in area. 

This change in pressure results in a *net force* being applied onto the fluid; where this force applies work. Recall from our note all the way back that the work is equivalent to the change in kinetic energy, thus: 

$$
W = \frac{1}{2}mv_{2}^{2} - \frac{1}{2}mv_{1}^{2}
$$

Using this principle, applied to a frictionless, laminar flow, we can actually derive the expression for Bernoulli's Equation! 

### Derivation
Consider some pipe, with two sections with cross-sectional areas $A_{1},A_{2}$ present at some height $h_{1},h_{2}$ from the surface. Consider that this pipe is frictionless and incompressible ($\rho$ is constant). Thus, with some initial flow velocity $v_{1}$, the corresponding amount of volume $dV$ it traces out between $A_{1}$ and $v_{1}$ must be the same as the corresponding amount of volume drawn out by $A_{2}$ and $v_{2}$: 
![[29 — Fluid Dynamics-1795389735926.webp|636]]

Noting that $dV$ is equivalent to some $A_{i}dx_{i}$; where subscripts indicate the corresponding area being discussed, we find that the work done on the fluid is represented by the following: 

$$
\begin{align}
dW & =F_{1}dx_{1} - F_{2}dx_{2} \\
 & =p_{1}A_{1}dx_{1} - p_{2}A_{2}dx_{2}  & A_{1}dx_{1} = A_{2}dx_{2} = dV \\
 & =p_{1}dV-p_{2}dV = (p_{1}-p_{2})dV
\end{align}
$$

Consider now as well the change in kinetic energy of the fluid: 

$$
\begin{align}
dK  & = \frac{1}{2}mv_{2}^{2} - \frac{1}{2}mv_{1}^{2}  & \text{from conservation of mass flow, }m_{1}=m_{2}=m\\
 & =\frac{1}{2}\rho dVv_{2}^{2} - \frac{1}{2}\rho dVv_{1}^{2} \\
 & =(v_{2}^{2}-v_{1}^{2}) \frac{1}{2}\rho dV
\end{align}
$$

And the corresponding change in the gravitationalpotential energy of the fluid: 

$$
\begin{align}
dU & =mgh_{2}-mgh_{1} = \rho dVh_{2} - \rho dVh_{1} \\
 & =(h_{2}-h_{1})\rho dV g
\end{align}
$$

Noting that $dW = dK+dU$, then: 

$$
\begin{align}
dW & =dK + dU \\
(p_{1}-p_{2})\cancel{ dV } & =\frac{1}{2} (v_{2}^{2}-v_{1}^{2})\rho \cancel{ dV } + (h_{2}-h_{1})\rho \cancel{ dV }g \\
p_{1}-p_{2} & = \frac{1}{2} \rho v_{2}^{2}-\frac{1}{2} \rho v_{1}^{2 } + \rho gh_{2} -\rho gh_{1} \\
p_{1} + \frac{1}{2}\rho v_{1}^{2} + \rho gh_{1} & = p_{2} + \frac{1}{2}\rho v_{2}^{2} + \rho gh_{2}
\end{align}
$$

Noting that in this system, conservation of energy is preserved, and that our choice for $h_{2}$ (and really, the point of analysis on the left side being arbitrary), then we come to the final derivation of Bernoulli's Equation: 

> [!theorem] Bernoulli's Equation
> For a frictionless, incompressible fluid; the combination of pressure and the sum of kinetic potential energy densities is constant not only over time, but also along a stream line. 
>
> $$p + \frac{1}{2}\rho v^{2} + \rho gh = \text{some constant}$$
>
> Where $p$ corresponds to the pressure at some point, $h$ represents the height above some origin, and $v$ corresponds to the flow velocity of the fluid. 

### Application
We can easily see the ramifications of Bernoulli's Equation in the following cases:

1. What if the velocity is constant? 
Consider the case in which $v_{1}=v_{2}$, thus: 

$$
\begin{align}
p_{1} + \cancel{ \frac{1}{2}\rho v_{1}^{2} } + \rho gh_{1} & = p_{2} + \cancel{ \frac{1}{2}\rho v_{2}^{2} } + \rho gh_{2} \\
p_{1} + \rho gh_{1} & = p_{2} + \rho gh_{2}
\end{align}
$$

Note that we normally define some point to be $h=0$, letting $h_{1}=0$ lets us see that: 

$$
p_{1} = p_{2} + \rho gh_{2}
$$

We see here that, for some change in height in a fluid travelling the same velocity, if $h$ decreases, $p_{2}$ increases, and the inverse is also true. 

2. What if it's depth is constant, but the velocity changes? (Bernoulli's Principle)
Consider the case in which $h_{1}=h_{2}$, thus: 

$$
\begin{align}
p_{1} + \frac{1}{2}\rho v_{1}^{2} + \cancel{ \rho gh_{1} } & = p_{2} + \frac{1}{2}\rho v_{2}^{2} + \cancel{ \rho gh_{2} } \\
p_{1} + \frac{1}{2}\rho v_{1}^{2} & = p_{2} + \frac{1}{2}\rho v_{2}^{2}
\end{align}
$$

Note that upon observation, we find that as the velocity increases, the pressure has to correspondingly decrease. 
> Note that we can still relate the volume to the corresponding flow rate, and that flow rate is conserved within a case in which continuity of flow holds. 

## Viscosity
Recall the definition of Laminar Flow, that is to say that the layers within a fluid don't mix, and all layers move with respects to the direction of flow. Recall as well, that when flow is violent; layers *do mix* and have significant velocities other than the desired direction of flow. 

The measure of viscosity is generally defined as the equation below:

$$
F = \eta\frac{ vA}{L} \implies\eta = \frac{FL}{vA}
$$

Where: 
* $F$ is the force required to keep some measuring plate moving at a fixed velocity, 
* $L$ is the distance between two measuring plates, 
* $v$ corresponds to the flow velocity of our fluid
* $A$ corresponds to the cross-sectional area of our plates.
* $\eta$ corresponds to the viscosity of our fluid (eta) 
(you can see this on the image below) 
![[29 — Fluid Dynamics-1795391047059.webp]]

## Laminar Flow
Consider now that we've been discussing about mass flow rate, flow rate, and all of these terms without fundamentally asking the question: what actually causes flow? We find that the cause of flow of a fluid is a pressure difference, where our fluid moves from a higher pressure, to a lower pressure: 

$$
Q = \frac{p_{2}-p_{1}}{R}
$$

Where $p_{2},p_{1}$ represent pressures at the end and start of a section respectively, and $R$ represents some factor of *resistance* to flow. $R$ is defined by Poiseuille's Law for Resistance below: 
> [!theorem] Poiseuille's Law for Resistance
>
> $$R=\frac{8\eta l}{\pi r^{4}}$$
>
> Where: 
> * $\eta$ is the viscosity of our fluid
> * $l$ corresponds to the **length** of a tube. 
> * $r$ corresponds to the radius of the tube.
> > Note that this implies that: 
> > $l,\eta$ increase the resistance of the fluid to flow (which makes sense, more contact area to resist / have drag) 
> > $r$ significantly decreases the resistance of the fluid to flow. 
> > > That is, if $r$ scales by a factor of $2$, our value of $R$ shrinks by a factor of 16.
> > 

Combining all of these pieces of information together, and substituting our term for $r$ into $Q$, we find that: 
$$
\begin{align}
Q  & = \frac{p_{2}-p_{1}}{R} \\
 Q& = \frac{(p_{2}-p_{1})\pi r^{4}}{8\eta l}= \frac{dV}{dt}
\end{align}
$$
Note that this is normally notated as Poiseuille's Law (or, Poiseuille's law for **laminar** flow). 
### Measuring Turbulence
In terms of measuring turbulence as well for a fluid, we have a measure notated as the Reynolds number of the flow: 
$$
N_{R} = \frac{2\rho vr}{\eta}
$$
Where: 
* $\rho$ is fluid density
* $v$ is the speed of the fluid
* $r$ is the radius of the tube
* $\eta$ corresponds to the viscosity.

Normally: 
* If $N_{R}<2000$, a flow is laminar.
* If $N_{R}>3000$, a flow is turbulent. 
* If $2000<N_{R}<3000$, a flow is considered to be **unstable**. That is it *can* be laminar, but small obstructions make it a turbulent flow. 