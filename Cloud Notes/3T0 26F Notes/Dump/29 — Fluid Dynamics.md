---
updated_at: 2026-11-22T18:24:01.979-05:00
edited_seconds: 220
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
Next:
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
dK  & = \frac{1}{2}mv_{2}^{2} - \frac{1}{2}mv_{1}^{2}  & \text{from conservation of mass flow}\\
 & =
\end{align}
$$
