---
updated_at: 2026-10-18T17:54:46.793-04:00
edited_seconds: 730
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 18
Lecture Date: 2026-10-22
Week: 7
---
Hub: [[PHY180 Hub]]
Previous: [[17 — Rotational Kinematics, Rotational Variables]]
Next: [[19 —Newton's Second Law for Rotation, Rotational Energy]]
> [!quote] Recommended Reading 
> University Physics, 10.4-10.5
> [[11 — Work and Kinetic Energy]]
> [[16 — Center of Mass and Rockets]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Rotational Kinetic Energy & Moments of Inertia 
Recall that we defined Kinetic Energy as the following in the previous note: 
$$
K_{T}= \frac{1}{2}mv^2
$$
Note however that this was defined for a sole point mass. Also consider that, in a rotational body; there might exist multiple particles present on the object that's rotating with various radii and masses pertaining to the center of rotation. We can also observe that, for a rotational system; while the tangential velocity may differ with radius; the same angular velocity is shared across the entire rotating object. 

Recall that: 
$$
v_{t} = \omega r
$$
Thus; plugging this into the equation above that we had earlier: 
$$
\begin{align}
K  & = \frac{1}{2}m(\omega r)^2 = \frac{1}{2}mr^2\omega^2
\end{align}
$$
Consider the expression/case that we had earlier; that for an object with multiple particles of varying masses and radii from the axis of rotation, that their corresponding $v_{t}$ term will differ. Since we know that $\omega$ is some constant across the entire rotating body; we simply need to take the sum of all of the kinetic energies present per particle in order to get the rotational kinetic energy of an object: 
$$
K = \frac{1}{2}m_{1}r_{1}^2\omega^2 +  \frac{1}{2}m_{2}r_{2}^2\omega^2 +  \dots +  \frac{1}{2}m_{n}r_{n}^2\omega^2 +  
$$
Note that the $\frac{1}{2}\omega ^2$ term is present in all of these; thus we can express it as the following equation: 
$$
K_{R} = \frac{1}{2}\left[ \sum_{j=1}^Nm_{j}r_{j}^2 \right]\omega^2
$$
Where we define the term inside; $\sum_{j=1}^N m_{j}r_{j}^2$ as the *Moment of Inertia* of our object; a relative measure of the difficulty to rotate; in terms of $kg\cdot m^2$: 

> [!theorem] Moment of Inertia (Descretized)
> The moment of Inertia of a rotating object with discrete particles is defined as the following expression: 
> $$I = \sum_{j=1}^Nm_{j}r_{j}^2$$
> Where $I$ is a measure of the object's rotational inertia; that is to say how hard it is to change it's rotational velocity. 

> [!axiom] Implications
> For instance; take an object with two particles of mass $M$ some distance $r$ from the rotational center of an object. If we analyze the center of our object; then we get the following moment expression: 
> $$I = Mr^2 + Mr^2 = 2Mr^2$$
> Now consider if we analyze it at the end of one of our objects instead; then: 
> $$I = M 0^2 + M(2r)^2 = 4Mr^2$$
> Which implies that our object will actually be *twice as hard* to rotate. 

Then; our above expression for rotational kinetic energy becomes the following: 
$$
K_{R} = \frac{1}{2}I\omega^2
$$
Note that from this, we can now extend our concept of the total kinetic energy of a system to now include both Rotational and Kinetic Energy: 
$$
K = K_{T} + K_{R} = \frac{1}{2}Mv^2 + \frac{1}{2}I\omega^2 = \frac{1}{2}(Mv^2 + I\omega^2)
$$
> [!theorem] Moment of Inertia (Integral) 
> The *moment* of inertia of a continuous object can be found by realizing that; for any infinitesimal segment of an object (i.e. $dm$), the radius will remain the same; thus we can define $I$ by taking smaller and smaller cuts of $m_{j}$ in the expression we defined above; up to some $dm$; then: 
> $$I = \int r^2 dm$$
> Where $dm$ represents some component of the mass distribution of the object (often from the linear mass density; though not always); and $r$ is often some term of distance from the rotational center. 
> > In CIV102; this is known as the Second Mass-Moment of Inertia; since that's the extended name of the term (though physics normally solely uses the term Moment of Inertia) 

## Calculating Moments of Inertia
Retaking our two Moment of Inertia expressions from above: 
$$
\begin{align}
I  & = \sum^N_{j=1}m_{j}r_{j}^2 \\
 & =\int r^2\ dm
\end{align}
$$
We could now begin starting to solve for some expressions for the moments of inertia of some objects. Note that for most objects; we can normally define $dm$ as some differential with respects to $r$. Note that $r$ is some factor with respects to how we define where our axis of rotation for our object is; and thus if we define $dm$ as a term of $r$; then the integration bounds above are now defined with respects to the geometry of an object. 

> Consider now the example of a uniform thin rod with an axis through the center; that is a rod of length $L$ and a linear mass density of $\lambda$. 

Recall that we can find the center of mass of a uniform object by taking the integral of $\frac{1}{M}\int r\ dm$; where $dm=\lambda dr$; then 
$$
\begin{align}
r_{com} &  = \frac{1}{M}\int ^{L}_{0} r\lambda dr = \frac{\lambda}{M} \left( \frac{L^2}{2} \right)   & \lambda L=M\\
 & =\frac{L}{2}
\end{align}
$$
Which implies that the center of mass of an object is at it's center. Consider now us finding the moment of inertia at this center; since we defined $dm$ already; then: 
$$
\begin{align}
I  & = \int r^2 dm = \int\lambda r^2dr = \lambda \int_{-\frac{L}{2}}^{L/2} r^2dr \\
 & =\lambda\left[ \frac{r^3}{3} \right]^{L/2}_{-L/2} = \lambda\left[ \frac{L^3}{24} + \frac{L^3}{24} \right] \\
I & =\frac{\lambda L^3}{12} = \frac{ML^2}{12}
\end{align}
$$

Consider now if we took the rotational axis at the *end* of one of the beams; that is changing the bounds of the integral from $\left[ -\frac{L}{2}, \frac{L}{2} \right]$ to $[0,L]$: 
$$
\begin{align}
I  & = \int r^2dm = \int\lambda r^2dr = \lambda \int ^{L}_{0}r^{2}dr \\
 & =\frac{\lambda L^3}{3}= \frac{ML^2}{3}
\end{align}
$$
This leads to the following theorem arising: 
> [!theorem] Parallel-Axis Theorem
> Let $m$ be the mass of an object, and let $d$ be the distance from an axis through the object's center of mass to a new axis, then we have: 
> $$I_{\text{Parallel Axis}} = I_{\text{CoM}} + md^2$$

For our expressions above; then we have: 
$$
\begin{align}
\frac{1}{3}ML^2  & = \frac{1}{12}ML^2 + M\left( \frac{L}{2} \right)^2  \\
 & =\frac{1}{12}ML^2 + \frac{ML^2}{4} = \frac{1}{3}ML^2
\end{align}
$$
### Other Surfaces
Note that for other surfaces; the context for which we define $dm$ (and consequently, $dr$) may vary. 

> For instance; suppose that we are forced to find the Moment of Inertia of a flat disk. 

For this, since it's a flat disk, we can assume that the density is uniform across the flat surface; that is $\sigma A = M$; then $\sigma dA =dM$; where $\sigma$ is the surface mass density of the object ($\sigma=\frac{M}{A}$)

Now consider the term $dA$; since this is a circle; we know that $A = \pi r^2$; thus $dA = 2\pi r\ dr$; thus plugging this in to our expression above: for $dM = \sigma(2\pi r) dr$ 
$$
\begin{align}
I  & = \int r^2\ dm = \int r^2 (\sigma2\pi r) \ dr  \\
 & =\sigma2\pi\int r^3dr

\end{align}
$$
Consider now the bounds that we are integrating with respects to; we want to integrate from the *center* of the circle, all the way out towards it's full radius, some radius $R$; then: 
$$
\begin{align}
I  & = \sigma2\pi \int_{0}^{R}r^3dr = \sigma2\pi\left[ \frac{R^4}{4} \right] \\
 I& =\frac{\sigma\pi R^4}{2}  & \sigma=\frac{M}{A=\pi R^2} \\
 I & =\frac{M\pi R^4}{2\pi R^2} = \frac{MR^2}{2}
\end{align}
$$
> Note that (probably) an alternative method exists for doing this in terms of some angular measure $\theta$; integrating from $0$ to $2\pi$, as we can subtend the area of a circle as the area inscribed within the arc formed by that corresponding angle. 
> 
> Proof is left as an exercise to the future reader. 
## Compound Objects 
Now that we know how to solve for the Moment of Inertias of continuous objects; now arises the equation as to how we should derive the moment of inertia of multiple objects in a more complex structure. 

In general, if we want to define the total Moment of Inertia of a system, we define it as the summation of the moments with respects to some rotational axis: 
$$
I = \sum ^{N}_{n=1} I_{n}
$$
Note that this means that **when we take the moments** in this context; they need to share the same axis; thus the Parallel Axis theorem may be applied in order to find the corresponding moment with the context of a certain rotational axis being set. 
