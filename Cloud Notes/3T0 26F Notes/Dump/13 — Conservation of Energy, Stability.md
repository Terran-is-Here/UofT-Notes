---
updated_at: 2026-10-08T16:50:17.852-04:00
edited_seconds: 510
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 13
Lecture Date: 2026-10-08
Week: 5
Created: October 5th 2026, 5:32:52 pm
---
Hub: [[PHY180 Hub]]
Previous: [[12 — Potential Energy, Conservative and Non-Conservative Forces]], [[12.1 — Multivariable Calculus (PHY180)]]
Next: [[14 — Momentum and Impulse]]
> [!quote] Recommended Reading 
> University Physics 8.3, 8.4, 8.5 
--- 
# Lecture Notes
## Spring Potential Energy
Note that we discussed this already previously in [[12 — Potential Energy, Conservative and Non-Conservative Forces]], but spring potential energy is defined as: 
$$
U_{e}=\frac{1}{2}kx^2
$$

## Potential Energy Graphs
For generating potential energy graphs; recall the integration-based definition of Potential Energy: 
$$
U = -\int _{A}^BF\cdot dr
$$
Where $dr$ is often some term of displacement, or more often $x$, then: 
$$
U = -\int_{A}^BF(r)dr
$$
### Relationship with Force 
The concept of a force can be applied in a potential; that is it is actually equivalent to the *negative gradient of potential* (or in other words, the derivative of a potential energy graph with respects to distance gives you force): 
$$
\vec{F} = -\vec{\nabla} U
$$
Where: 
$$
F_{x}=-\frac{\partial U}{\partial x}, F_{y}=- \frac{\partial U}{\partial y}, F_{z}=- \frac{\partial U}{\partial z}
$$
Note that if we do the following: 
$$
\begin{align}
\frac{F_{x}}{dy} = -\frac{\partial U}{\partial x\partial y} && \frac{F_{y}}{dx} = -\frac{\partial U}{\partial x\partial y} \\
\frac{F_{x}}{dy}=\frac{F_{y}}{dy}\end{align}$$
Which gets us the potential energy result for conservative forces that we got in [[12 — Potential Energy, Conservative and Non-Conservative Forces#Proving Conservativity|Proving Conservativity (PHY180-12)]]; that is it results from differentiating the partial results of some gradient of potential. 

## Sources of Energy 

---
# Pre-Lecture Notes
## Conservation of Energy
The concept of the conservation of energy of a system is defined by the term below: 
$$K+U=E$$
Where $E$ is the *mechanical energy* of the system. If we define $K$ and $U$ in terms of their differences; then: 
$$\Delta (K+U) = E$$
**If** a non-conservative / dissipative force exists; then the difference in the mechanical energy grants us the energy dissipated by this non-conservative force: 
$$\Delta E_{\text{path AB}} =\Delta (K+U)_{\text{path AB}} = W_{\text{non-conservative force on path AB}}$$
Since $K,U$ are conserved quantities, if these quantities change, the resulting difference is the amount of energy dissipated out of the system. 

Note that if and only if a non-conservative force is *absent* from a system, then for any $K,U$, then: $$K_{0}+U_{0}=K_{t}+U_{t}=E$$
That is, any change in some $K$ will be directly equal to some change in $U$, as $E$ must remain some constant. Note that for a system; $E\geq0$ always. 
## Potential Energy Diagrams & Stability
Given a function of $U(x)$ where this returns the Potential Energy of a certain particle; we can rewrite our above term as some: 
$$
K + U = E \to K+U(x) = E
$$
Since $E \geq0$ always; then: $$K + U(x) = E \geq 0$$
From here, we can show and solve for a set of values for $x$ for which our particle can take from it's initial energy states; which graphically also restrict the number of energy values which our particle may take (or in other words, the set of possible potential energy values that our particle can take). 

Think about this as showing which range of potential energy values / wells that our particle can passively escape. 

> [!ila] In Lecture Addendum 1
> We can think of the range of values; as the range under some line $y=E_{T_{0}}$, or in other words the amount of energy initially within the system is the maximum it can ever reach, and the function under this is the only valid positions possible. 

> [!ila] In Lecture Addendum 2
> There exists two general types Equilibrium points: 
> * Stable: Where our particle will oscillate between two points (a local minima) 
> * Unstable: Where our particle, if disturbed, would fall into another potential well (a local minima). 

