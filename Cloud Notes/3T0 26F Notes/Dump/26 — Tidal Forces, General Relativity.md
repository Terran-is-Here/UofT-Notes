---
updated_at: 2026-11-16T16:40:30.260-05:00
edited_seconds: 240
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 26
Lecture Date: 2026-11-16
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[25 — Orbital and Keplerian Mechanics]]
Next: [[27 — Fluids, Density, Pressure, Pascal's Principle]]
> [!quote] Recommended Reading 
> University Physics Sections 13.6, 13.7

--- 
# Lecture Notes
## Tidal Forces and the Inverse Cube Law 
Consider a gravitational field; for a point mass $m$, this is given by the following: 
$$
g = \frac{GM}{r^{2}}
$$
Consider a small displacement $\Delta r$ towards the attracting body; then: 
$$
\begin{align}
\Delta g  & = \left| \frac{dg}{dr}\right|\Delta r \\
 & =\left| \frac{d}{dr}GMr^{-2}\right|\Delta r  \\
 & = \left| \frac{-2GM}{r^{3}}\right|\Delta r
\end{align}
$$
This equation is the equivalent *tide* equation for our object, thus: 
$$
\boxed{\Delta g= \left| \frac{-2GM}{r^{3}}\right|\Delta r}
$$
### Application
For instance, what is the $\Delta g$  between the centre of the earth and it' sedge in comparison to the sun? 

Using the data in the slideshow, we see that: 
$$
\Delta g = \left| -\frac{2GM}{r^{3}}\right|\Delta r = \frac{2*6.67*10^{-11}*2*10^{30}}{(1.5\times 10^{11})^{3}}6400\times 10^{3} = 5\times 10^{-7} \text{ m/s}
$$
For the moon however: 
$$
\Delta g = \left| -\frac{2GM}{r^{3}}\right| = \frac{2\times 6.67\times 10^{-11}\times 7.3\times 10^{22}}{(3.8\times 10^{8})^{3}}\times 6400\times 10^{-3} = 1.1\times 10^{-6} \text{m/s}
$$

## Einstein's Gravity
Recall Newton's Second Law: 
$$
a = \frac{F_{net}}{m_{i}}
$$
Where $m_{i}$ is the inertial mass of the object; to resist acceleration when subject to an external force. 

Consider now the force of gravity: 
$$
F_{g} = m_{g}g
$$
Where $m_{g}$ is equivalent to the gravitational mass, where this represents the scaling factor for **how much gravity affects us**. In free fall, we often set $F_{g} = m_{a}$, and terms cancel out. In other words, we set $m_{i} = m_{g}$

### Rockets
Consider a rocket going upwards at some acceleration of $a=9.8 \frac{m}{s}$. From an observer within this non-inertial reference frame, this "fictional force" appears like the force of gravity. In other words, you cannot tell locally i

---
# Pre-Lecture Notes
## Tidal Forces
The concept of a Tidal Force arises from the radius term that we have in our law of universal gravitation; recall that we defined the force experienced by an object as the following: 
$$
F_{g}=\frac{Gm_{1}m_{2}}{r^{2}}
$$
Given that we are *solely* measuring the gravitational force of an object on a planet $p$'s surface with respects to another body $o$, then we note that $r_{p}$ represents the radius of the planet we are resting on, and $r_{O}$ as the radius of rotation. We also note that $M_{o}$ is the mass of the planet orbiting us, and $m$ being the mass of the respective object; then: 
$$
F_{g} = \frac{GM_{0}m}{(r_{O}\pm r_{p})^{2}}
$$
Note that $\pm$ term on the denominator basically asks us to solve on either the far side, or on the close side of the moon, the corresponding gravitational pull felt. 
> [!ila] In Lecture Addendum
> Note that the interpretation for this is that the tides are caused by an effective difference in the acceleration from gravity from another body. 

## General Relativity
Please refer to lecture notes pertaining to this section in the future. 