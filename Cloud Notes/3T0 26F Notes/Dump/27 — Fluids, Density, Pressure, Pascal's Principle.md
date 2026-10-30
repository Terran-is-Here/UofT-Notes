---
updated_at: 2026-10-29T21:05:27.111-04:00
edited_seconds: 590
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 27
Lecture Date: 2026-11-19
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[26 — Tidal Forces, General Relativity]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics Section 14.1, 14.2
> [[22 and 23 — Static Equilibrium and Elasticity]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Fluids
Recall that in [[22 and 23 — Static Equilibrium and Elasticity]], solids are the sole state of matter that can properly resist Shear Stresses; where as fluids like Liquids and Gasses immediately yield and displace with subjected to them. Recall from *your long history in Science* that: 

* Liquids do not have a fixed shape and conform to the shape of their container; 
* Gasses do not have a fixed shape and **fill the volume of their container**. 

Recall the degrees of separation present with Liquids and Gasses: Particles between liquids have a small degree of separation (but freedom of movement); whilst gasses have a large degree of separation. What this implies is that, when we compress a liquid; it takes significantly more pressure to compress it by a certain $\Delta V$ over compressing a gas. 

### Density
We can also define the concept of Density; however that should be obvious at this point. Density is a function of mass over volume; that is:
$$
\rho = \frac{m}{V}
$$
Note however that the density of a substance may not be constant across the entire liquid being analyzed; a homogenous substance has some constant $\rho$, whilst a heterogenous substance may not have a constant $\rho$. We can take the local density as the limit of $\frac{dm}{dV}$: 
$$
\rho = \lim_{ \Delta V \to 0 } \frac{\Delta m}{\Delta V}
$$

## Pressure
Recall that we already defined the concept of pressure in [[22 and 23 — Static Equilibrium and Elasticity]], but we can restate it here. Pressure is defined as the *normal force* per unit area; that is:
$$
p = \frac{F}{A}
$$
Where the pressure at a point is taking the differential of this: 
$$
p = \frac{dF}{dA}
$$
Note that this has implication when combined with our earlier definition of density. Consider the case that we have a container of liquid, what is the pressure applied at the bottom of that container?  We know that it will experience some pressure from the atmosphere (some $p_{0}$), but we also know that it will experience a force normal to the surface by the weight of the liquid, some $mg$. Note however that we can relate $mg$ to the property of density, thus: 
$$
F_{w} = mg = \rho Vg = \rho Ahg
$$
Note how we expanded $V=Ah$, which is true generally for any *cylindrical* container (see [[23 — Volumes|ESC194 (23) - Volumes]]); then we find that the pressure applied on the bottom will be: 
$$
\begin{align}
p_{b}  & = p_{0} + \frac{\rho Ahg}{A} \\
 & =p_{0} + \rho hg
\end{align}
$$
This is actually only usable if and only if the fluid has some constant density; that is $\bar{\rho}=\rho$; then this is the pressure at some depth $h$ for a fluid of constant density: 
> [!theorem] Pressure at a Depth for a Fluid of $\bar{\rho}$
> $$p_{h} = p_{0} + \rho hg$$
> Where $p_{0}$ is the atmospheric pressure, $\rho$ is the density of the fluid, $h$ is the depth, and $g$ is gravity. 

Note however that the pressure at some certain height $h$ is applied across uniformly the container at that point; that is given a container; at some height $h$, the pressure experienced by the walls of that container are defined by our equation above, assuming that the density is uniform within the fluid. 

### Generalization
Consider now that our above assumptions rely on the case on if and only if the density of a liquid is held constant with respects to the entire volume. Note that we also however know, that our liquid will be realistically be compressed by the liquid above it; thus gaining a slightly higher density. We should be able to find a generalized equation with respects to this however. 

Consider now a container of liquid; with a density of $\rho$ and a cross-sectional area of $A$. Consider taking a slice of that liquid at some height $y$ below the water, giving us some mass member $\Delta m$. Let $h=y$ and let $y$ be positive going upwards for this instance. 

We know that this slice of water will experience some force proportional to the pressure above the water; some $p(y)A$; and we know that it will experience a corresponding reaction force upwards by some force $p(y+\Delta y)$, where $\Delta y <0$. We also know that it will experience some force of gravity, some $g\Delta m$. We also know that this acceleration should be 0 (or our water is falling); thus in terms of the $\sum F_{y}$; we get the following relation: 
$$
p(y+\Delta y)A - p(y)A - g\Delta m = 0
$$
Note that we can describe $\Delta m$ from the volume of the corresponding mass member; that is $\Delta m = |\rho A\Delta y| =-\rho A\Delta y$ (as $\Delta y <0$); then plugging this in to our expression above, we get: 
$$
\begin{align}
p(y + \Delta y)A - p(y)A +g\rho A\Delta y  & = 0 \\
p(y+\Delta y)A - p(y)A & =-g\rho A\Delta y  & \text{Divide by } A\Delta y\\
\frac{p(y+\Delta y) - p(y)}{\Delta y}  & =-g\rho \\
\lim_{ \Delta y \to 0 } \frac{p(y+\Delta y) - p(y)}{\Delta y} = \frac{dp}{dy} & =-g\rho
\end{align}
$$
That final result is pivotal; that is the rate of change of pressure in the fluid; is proportional to the fluid's density times the gravity experienced by that fluid. 

Consider now if density *is* constant in a fluid. Define the start of the container as the top, that is $y=0$, then we find that integrating from $0 \to -h$, where $h$ is the height of the container, then 
$$
\begin{align}
dp  & = -g\rho \,dy \\
\int_{p_{0}}^{p_{h}} dp & =\int _{0}^{-h}-g\rho \,dy \\
p_{h}-p_{0} & =g\rho h \\
p_{h} & =p_{0} +g\rho h
\end{align}
$$
Which is the same result we derived earlier. 
### Variant Height
We now also need to consider the term $p_{0}$, as this is a factor of the pressure of the air. Recall from Grade 12 chemistry that we can describe pressure as a function of volume, moles of material, temperature, and a constant $R$: 
$$
pV = nRT
$$
This can be rewritten as the following: 
$$
p = \frac{\rho k_{b}T}{m}
$$
Where $k_{b}$ is Boltzmann's Constant, $k_{b}=1.38\times 10^{-23} \frac{J}{K}$. This is an equivalent rewriting of the ideal gas law, however it lets us set it related to some term of $\rho$. 