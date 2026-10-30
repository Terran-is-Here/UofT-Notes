---
updated_at: 2026-10-29T20:07:29.451-04:00
edited_seconds: 580
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 22
Lecture Date: 2026-10-27
Week: 8
---
Hub: [[PHY180 Hub]]
Previous: [[21 — Conservation of Angular Momentum, Gyroscopic Precession]]
Next: [[24 — Gravitation]]
> [!quote] Recommended Reading 
> Chapter 12 of the University Physics Textbook.
> Your CIV102 Notes. 

> [!caution] Note
> This note is the combination of the entire chapter, since most of this is concepts discussed from CIV102 anyways. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Static Equilibrium
Static Equilibrium arises from Newton's Second Law. Recall that the net force is equivalent to the net change in momentum: 
$$
\sum F=\frac{dp}{dt} = ma
$$
In the case of static equilibrium, we set $a=0$, thus: 
$$
\sum F = 0
$$
Conversely, we also define the same for rotational systems, i.e. the net change in the angular momentum of a system must be equal to 0, where: 
$$
\sum \tau = \frac{dI}{dt} = I\alpha
$$
Where $\alpha=0$, then $\sum \tau = 0$, thus giving us our two equilibrium expressions: 
> [!theorem] Equilibrium Expressions
> The following are true if and only if a system is in equilibrium. 
> $$\begin{align}\sum F_{x,y,z}  & = 0  & \text{translational equilibrium} \\\sum \tau  & =0  & \text{rotational equilibrium}\end{align}$$

Note that for both cases, we can break it up into it's corresponding vectors (e.g. $F_{x},F_{y},F_{z},\tau_{x},\tau_{y},\tau_{z}$), or in other words the six degrees of freedom available to an object in some $\mathbb{R}^{3}$. Note that an equilibrium in a system holds true, regardless of which origin you pick for a point of analysis. Do note that distances update accordingly, however force directly pointing inwards / acting inline with a CoM have their $d$ set to 0 if and only if that point is the point of analysis. 

In terms of actually applying this in problems, use the equilibrium conditions above, solve for reactions and or distances if necessary, and always try to find the point of analysis that would most simplify the computation required for solving such a problem. 

## Tensile Stress and Strain
We now define the concept of Stress and Strain. 

> Stress: 
> A force applied over an area, that is some $\frac{F}{A}$, or $\frac{F}{D^{2}}$. Defined in SI units of Pascals $\left( \frac{N}{m} \right)$, (or in CIV102, MPa, $\frac{N}{mm^{2}}$). 
> $$\sigma = \frac{F_{a}}{A}$$
> Describes a force which induces deformation on an object. 

> Strain
> The change in length a material undergoes when deformed, or in other words, $\frac{\Delta L}{L_{0}}$: 
> $$\epsilon = \frac{\Delta L}{L_{0}}$$
> Note that Strain is a dimensionless constant, though it is often notated in CIV102 as $\frac{mm}{mm}$ or $\frac{mm}{m}$; millimeters of elongation per meter. 

Recall that Stress and Strain are defined by the following relation: 
$$
\sigma = E\epsilon
$$
Where $E$ is the Young's Modulus of the material, a material characteristic signifying it's degree of stiffness. Defined in terms of $MPa$, as $\epsilon$ is a dimensionless value. Note that this relation only holds true if and only if $\epsilon>\epsilon_{y}$, as past this point there exist other effects such as yielding, stress hardening, and eventually rupture.

(This often leads to this function being defined more as some piecewise expression, if it were actually mathematically modelled. ): 
$$\sigma(\epsilon) = \begin{cases}\dots \\\dots \\\dots\end{cases}$$
### Bulk Stress and Strain
Consider now the case that for a 3d object, a uniform pressure $\Delta p$ is applied across all surfaces present across the body, such as when being submerged in water. This would induce a change in the volume of that object, thus we can define the concept of Bulk Strain similarly to Tensile / Axial Strain: 
$$\epsilon_{b} = \frac{\Delta V}{V_{0}}$$
Similarly with a uniform applied pressure $\Delta P$ , we can now define the Bulk Modulus as the following: 
$$
B = \frac{\sigma_{B}}{\epsilon_{B}} = -\frac{\Delta P}{\frac{\Delta V}{V_{0}}} = -\Delta P\frac{V_{0}}{\Delta V}
$$
Note that the negative sign present there originates as a means to ensure that $B$ is always constant: If $\Delta P$ increases, $\Delta V$ will become a negative value. This essentially asks if the volume changes by a certain amount, how much does the pressure applied change in response? This is essentially analogous to $\sigma=\epsilon E$ earlier for Tensile/Compressive members. 

The reciprocal of this is defined as the Compressibility of an object: 
$$
k=\frac{1}{B} = -\frac{\Delta V}{\Delta P*V_{0}}
$$
Where the units of this are in terms of a change in volume, with respects to a change in pressure. Compressibility is a measure of how much the volume of an object change, if the pressure applied on it changes. 

### Shear Stress and Strain
Consider now the case of Shear Deformation. Shear Deformation occurs when two *antiparallel* forces of **equal magnitude** are applied tangentially to opposite surfaces of a solid object (this means to transverse deformation, but shear deformation instead). 

Shear deformation is defined by some gradual change of $\Delta x$ of the layers in the direction **tangent** to acting forces present; being applied over some original distance $L_{0}$. Thus we can define shear strain as the following: 
$$
\epsilon_{S} = \frac{\Delta x}{L_{0}}
$$
Similarly to our previous expressions, this is also related with Shear Stress. Stress is due to forces that act parallel to the surface, thus: 
$$
\sigma_{S}= \frac{F_{||}}{A}
$$
Where $F_{||}$ indicates forces that act parallel to our surface. These are also related in some proportionality constant in terms of the shear modulus: 
$$
S = \frac{\sigma_{S}}{\epsilon_{S}} = \frac{L_{0}F_{||}}{\Delta xA}
$$
![[22 and 23 — Static Equilibrium and Elasticity-1793120813452.webp|457]]
Though really, it's kind of weird when you think about it, since this is heavily linked to the concept of a couple.
> [!caution] Note
> Apparently the concept of *complimentary shear stress* exists, to balance out and ensure that rotational equilibrium holds true? I have no idea how that goes into our calculations though, and will thus leave it for the In-Lecture Addendums to more properly explain. \[Aries\]

> [!caution] Note
> Solids are also the sole state of matter able to withstand Shear Stress; other forms of matter simply yield and displace with regards to shear forces. 

