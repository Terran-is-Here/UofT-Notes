---
updated_at: 2026-10-29T22:46:52.211-04:00
edited_seconds: 560
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 28
Lecture Date: 2026-11-20
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[27 — Fluids, Density, Pressure, Pascal's Principle]]
Next: N/A
> [!quote] Recommended Reading 
> Sections 14.3 - 14.5 of the University Physics Textbook. 

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Pascal's Principle
> [!theorem] Pascal's Law
> Pascal's Law generally states that, given an applied change in pressure, some $\Delta P$, to a fluid that is **fully enclosed**; that pressure is transmitted undiminished **to all sections  of the fluid including the walls of the container**. In other words, $\Delta P$ is constant throughout the entire fluid and corresponding containers. 
> In terms of an equation then $\Delta P$ is constant regardless of point of analysis. 

This has applications when we consider that this allows us to effectively multiply a given amount of input force. 

Consider an applied force through a piston, i.e. $F_{1}$ on some surface $A_{1}$; then we know the pressure is the following: 
$$
p_{1} = \frac{F_{1}}{A_{1}}
$$
As per the definition of pressure. We know that from Pascal's law that this will be transmitted perfectly across the fluid. Consider now that if our fluid is interfacing with another piston with an area $A_{2}$, we know that the pressure on that piston will be the following: 
$$
p_{2} = \frac{F_{2}}{A_{2}}
$$
We know $p_{2}=p_{1}$ as per Pascal's Principle, thus: 
$$
\boxed{\frac{F_{1}}{A_{1}} =\frac{F_{2}}{A_{2}}}
$$
This is true for any hydraulic system, as long as it is perfectly enclosed. Note that if we notate $F_{1},A_{1}$ as some input piston (replacing the subscript with $i$), and $F_{2},A_{2}$ as the output piston, we see that: 
$$
\frac{F_{i}}{A_{i}} = \frac{F_{o}}{A_o} \implies F_{o} = \frac{F_{i}A_{o}}{A_{i}}
$$
Or in other words: 
$$
F_\text{out}=F_\text{in} \times \frac{A_\text{Out}}{A_\text{In}}
$$
Our force is multiplied by the ratio between the output and input area respectively. We see now that if $A_\text{out}>A_\text{In}, F_\text{out}>F_\text{in}$; that is we effectively increase the corresponding output force. 

For instance, if our output piston is 5 times larger than our input cylinder, then for any applied force in our input cylinder; the corresponding output will be multiplied by 5. The inverse also holds true if we go in the opposite direction. 
## Archimedes' Principle 
Archimedes' Principle essentially deals with the concept of *buoyancy* within fluids; specifically it defines the concept of a Buoyant Force of a fluid. 

To understand where Archimedes' Principle originates from, consider a mass member submerged in water *at rest*. This means that this object is supported by the liquid around it. Consider now if that object is removed; now the liquid that was originally displayed now takes up that spot; and too experiences this force to ensure $y$-equilibrium; thus we find that: 
$$
F_\text{B}=w_\text{fl}
$$
> [!theorem] Archimedes' Principle
> The *buoyant force* on an object is equivalent to the weight of fluid it displaces; that is:
> $$F_\text{B}=w_\text{fl}$$
> Where $F_\text{B}$ represents the buoyant force, and $w_\text{fl}$ represents the weight of water it displaces. 

Note that $w_\text{fl}$ can be expressed as some term of volume of water displaced by an object, times the density of the fluid: $w_\text{fl}=\rho V_\text{displaced}$. 
### Floating
* For something to float, we know that $F_{B}$ must at minimum exceed the weight of the object; that is $\rho _\text{f}V_\text{d}\geq\rho _\text{obj}V_\text{obj}g$. 

We can now consider the concept of *defining* the fraction an object is submerged with respects to a fluid. Consider the following ratio: 
$$
\frac{V_\text{sub}}{V_\text{obj}}
$$
This intuitively gives us the ratio for how much an object is submerged over the volume of the object itself. Note that $V_\text{sub}=V_\text{fl}$, where this represents the volume of fluid we displace. Consider now that with volumes, we can now also compare the densities by $\rho=\frac{m}{V} \implies V=\frac{m}{\rho}$; then: 
$$
\text{Fraction Submerged}=\frac{V_\text{fl}}{V_\text{obj}} = \frac{\frac{m_\text{fl}}{\rho _\text{fl}}}{\frac{m_\text{obj}}{\rho _\text{obj}}} \implies \frac{V_\text{fl}}{V_\text{obj}} =\frac{\rho _\text{obj}}{\rho _\text{fl}} 
$$
Note that since our object is floating; we know that $m_\text{fl}=m_\text{obj}$ (as $y$ in equilibrium); thus we can take the last step in that equality chain. Note that this implies that as $\rho _\text{obj}$ increases, the amount submerged increases (which makes sense). 

## Fluid Dynamics
The scope of this course does not fully tackle the nuances of fluid mechanics, however we note the concept of Flow Rate (and the concepts that immediately follow from it). 

We define the concept of flow rate as the *volume of fluid* that passes through an area during a period of time; that is: 
$$
Q = \frac{dV}{dt}
$$
Note that for a pipe cross-section, we can define this in terms of $V=Ax$, where $x$ is inline the direction of flow, then: 
$$
Q = A \frac{dx}{dt} = Av
$$
Or in other words, the Flow Rate is proportional to the cross-sectional area the fluid is flowing through, times the flow velocity. Note that flow velocity does not necessarily imply a large flow rate. This equation can be applied across several regions of pipe if and only if continuity of flow is held. 

> [!caution] Continuity of Flow
> The same amount of fluid **must** flow past any point in the tube if and only if no other sources or sinks exist between two points in a pipe that would add or remove mass. 
> 
> In other words, the mass flow rate, and flow rate going in; must equal the mass flow rate / flow rate going out. 

For our case; then: 
$$
\begin{align}
Q_{1} & =Q_{2} \\
A_{1}v_{1} &  =A_{2}v_{2}
\end{align}
$$
* Consider the implications of this; we can see that if we have some constriction; some $A_{2}<A_{1}$; then we see that $1< \frac{A_{1}}{A_{2}}$; then $v_{2}>v_{1}$: 
* We can trivially solve for the flow velocity at a certain point by simply comparing the ratio of the cross sections of flow, that is $v_{2}=v_{1} \left( \frac{A_{1}}{A_{2}} \right)$.  


Note that Continuity of Flow also requires the mass flow rate to be constant across both ends of a pipe; assuming that it is a closed system. Recall that we can define mass as a term of density; then: 
$$
m = \rho V = \rho Ax
$$
Then the mass flow rate is given by: 
$$
\frac{dm}{dt} = \rho A \frac{dx}{dt} = \rho Av
$$
Then, following from continuity of flow, we see that: 
$$
\begin{align}
\left( \frac{dm}{dt} \right)_{1}  & = \left( \frac{dm}{dt} \right)_{2} \\
\rho_{1}A_{1}v_{1} & =\rho_{2}A_{2}v_{2}
\end{align}
$$
Note that if $\rho_{1}=\rho_{2}$; then we see that this simplified back into our earlier expression in terms of flow rate. 