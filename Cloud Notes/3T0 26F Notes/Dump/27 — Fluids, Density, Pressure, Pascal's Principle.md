---
updated_at: 2026-10-29T20:25:40.368-04:00
edited_seconds: 320
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
Note that this has implication when combined with our earlier definition of density. Consider the case that we have a container of liquid, what is the pressure applied at the bottom of that container? 

We know that it will experience some pressure from the atmosphere (some $p_{0}$), but we also know that it will experience a force normal to the surface by the weight of the liquid, some $mg$. Note however that we can relate $mg$ to the property of density, thus: 
$$
F_{w} = mg = \rho Vg = \rho Ahg
$$
Note how we expanded $V=Ah$, which is true generally for any *cylindrical* container (see [[23 — Volumes|ESC194 (23) - Volumes]]); then we find that the pre