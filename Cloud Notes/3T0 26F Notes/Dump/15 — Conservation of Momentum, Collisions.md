---
updated_at: 2026-10-10T21:56:50.877-04:00
edited_seconds: 1590
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 15
Lecture Date: 2026-10-15
Week: 6
Created: October 9th 2026, 10:47:01 pm
---
Hub: [[PHY180 Hub]]
Previous: [[14 — Momentum and Impulse]]
Next: [[16 — Center of Mass and Rockets]]
> [!quote] Recommended Reading 
> Sections 9.4, 9.5 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Collision Types
The core principle of analyzing collisions within Momentum is that the principle of conservation of momentum *always* holds true. That is the initial and final momentum of the system is *always* held true: 
$$
m_{1}v_{1} + m_{2}v_{2} = m_{1}v_{1,f} + m_{2}v_{2,f}
$$
Using the notation of some $v_{n,f}$ to indicate the final velocity of an object. From this, we can derive equations for the types of collisions. 
### Perfectly Elastic
Perfectly Elastic collisions have conservation of momentum, as well as conservation of energy, that is the following two systems of equations *are* true.
$$
\begin{align}
m_{1}v_{1} + m_{2}v_{2} &= m_{1}v_{1,f} + m_{2}v_{2,f} \tag{1}\\
\frac{1}{2}m_{1}v_{1}^2 + \frac{1}{2}m_{1}v_{2}^2 &= \frac{1}{2}m_{1}v_{1, f}^2 +\frac{1}{2}m_{1}v_{2,f}^2 \tag{2}
\end{align}
$$
We want to derive equations to solve for $v_{1,f}$ and $v_{2,f}$. First, lets rearrange equation $(1)$ atop to get terms of $m_{2},m_{1}$ all to one side; 
$$
\begin{align}
m_{1}v_{1}-m_{1}v_{1,f} &= m_{2}v_{2,f} - m_{2}v_{2} \\
m_{1}(v_{1}-v_{1,f}) &= m_{2}(v_{2,f}-v_{2}) \tag{1.1}
\end{align}
$$


Rearranging $(2)$:
$$
\begin{align}
m_{1}v_{1}^2 +m_{2}v_{2}^2 &= m_{1}v_{1,f}^2 + m_{2}v_{2,f}^2 \\
m_{1}(v_{1}^2 - v_{1,f}^2) &= m_{2}(v_{2,f}^2 - v_{2}^2) \\
m_{1}(v_{1}-v_{1,f})(v_{1}+v_{1,f}) &= m_{2}(v_{2,f} - v_{2})(v_{2,f}+v_{2}) \tag{2.1}
\end{align}
$$
Dividing $(2.1)$ by $(1.1)$: 
$$
\begin{align}
\frac{m_{1}(v_{1}-v_{1,f})(v_{1}+v_{1,f}) = m_{2}(v_{2,f} - v_{2})(v_{2,f}+v_{2})}{m_{1}(v_{1}-v_{1,f}) = m_{2}(v_{2,f}-v_{2})} \\
&\boxed{v_{1}+v_{1,f}= v_{2} + v_{2,f}} \tag{3}
\end{align}
$$
Take a note of $(3)$ and $(1)$: 
$$
\begin{align}
m_{1}v_{1} + m_{2}v_{2} &= m_{1}v_{1,f} + m_{2}v_{2,f} \\
v_{1}+v_{1,f}&= v_{2} + v_{2,f} \tag{for derivation 2}  \\
\implies v_{1}-v_{2} &= v_{2,f}-v_{1,f} \tag{for derivation 1}
\end{align}
$$
The equation $v_{1} + v_{1,f} = v_{2}+v_{2,f}$ is actually quite significant; particularly when we write it as the form below. It essentially states that the velocity of our objects on approach relative to each other, is equal to the velocity of our objects after separation. 
> [!axiom] Coefficient of Restitution (External)
> The following equation: 
> $$v_{1}-v_{2}=v_{2,f}-v_{1,f}$$
> Is actually related to a concept known as Restitution. Restitution is a measure of how "elastic" a system is. More generally, it's a proportionality term pertaining to the "springiness" of a collision between two surfaces. This equation above was derived with the assumption that the collision is *perfectly* elastic; that is: 
> $$\frac{v_{2,f}-v_{1,f}}{v_{1}-v_{2}} = e = 1$$
> Where $e$ in this context is the coefficient of restitution. This is *only* $1$ if and only if our collision is perfectly elastic. 
> 
> Note that if our collision is now *perfectly inelastic*, this implies that $v_{2,f}=v_{1,f}$, meaning that $e=0$. This is the term for a perfectly inelastic collision. $e$ will always be some value $0\leq e\leq1$; where $0$ implies a perfectly inelastic collision and $1$ implies a perfectly elastic collision.
> 

> [!theorem]- Linear Algebra Derivation 
> We can actually relate these together in a linear system of $\mathbf{A}x = b$ (see [[06 — Solving Linear Equations, Intro to Matrices#AX=B Matrix|AX=B Matrices]])
> $$\begin{bmatrix}m_{1} & m_{2} \\1 & -1\end{bmatrix}\begin{bmatrix}v_{1,f} \\v_{2,f}\end{bmatrix} = \begin{bmatrix}m_{1}v_{1} + m_{2}v_{2} \\v_{2}-v_{1}\end{bmatrix}= \begin{bmatrix}m_{1}v_{1,f} + m_{1}v_{2,f} \\v_{1,f}-v_{2,f}\end{bmatrix}$$
> $$\begin{bmatrix}m_{1} & m_{2} \\1 & -1\end{bmatrix}\begin{bmatrix}v_{1,f} \\v_{2,f}\end{bmatrix} = \begin{bmatrix}m_{1}v_{1} + m_{2}v_{2} \\v_{2}-v_{1}\end{bmatrix} \tag{we only care about this}$$
> > [!axiom] Inverse of a Matrix 
> > Note that we now need to *solve* for the inverse of a matrix. We haven't really figured out how to exactly get our selves to some equation (at least at time of writing); but a matrix inverse is generally defined as the following: 
> > $$\begin{align}\mathbf{A} &= \begin{bmatrix}a & b \\c & d\end{bmatrix} \\\mathbf{A}^{-1} &=\frac{1}{\det \mathbf{A}}\text{adj }\mathbf{A} = \frac{1}{ad-bc}\begin{bmatrix}d & -b \\-c & a\end{bmatrix}\end{align}$$
> > We denote $\mathbf{A}^{-1}$ the inverse of matrix $\mathbf{A}$, and has the property that $\mathbf{A}\mathbf{A^{-1}}=\mathbf{I}$:$$\begin{align}\left( \frac{1}{ad-bc} \right)\begin{bmatrix}a & b \\c & d\end{bmatrix}\begin{bmatrix}d & -b \\-c & a\end{bmatrix} &= \begin{bmatrix}ad-bc & -ab+ba \\cd-dc & -cb+da\end{bmatrix}\left( \frac{1}{ad-bc} \right) \\\begin{bmatrix}\frac{ad-bc}{ad-bc} & 0 \\0 & \frac{ad-bc}{ad-bc}\end{bmatrix} & = \begin{bmatrix}1 & 0 \\0 & 1\end{bmatrix} \\\therefore, \mathbf{AA}^{-1} &= \mathbf{I}\end{align}$$
> 
> For our case, we want to solve for some $\mathbf{A^{-1}}$, or in other words the inverse of our matrix $\begin{bmatrix}m_{1} & m_{2}\\1 & -1\end{bmatrix}$. Taking our formula above; then we see that; 
> $$\begin{bmatrix}m_{1} & m_{2} \\1 & -1\end{bmatrix}^{-1} = \frac{1}{-(m_{1}+m_{2})}\begin{bmatrix}-1 & m_{2} \\-1 & m_{1}\end{bmatrix}$$Then: 
> $$\begin{align}\begin{bmatrix}v_{1,f} \\v_{2,f}\end{bmatrix} &= \left( -\frac{1}{m_{1}+m_{2}} \right)\begin{bmatrix}-1 & -m_{2} \\-1 & m_{1}\end{bmatrix}\begin{bmatrix}m_{1}v_{1} + m_{2}v_{2} \\v_{2}-v_{1}\end{bmatrix} \\[1em]&=\left( -\frac{1}{m_{1}+m_{2}} \right)\begin{bmatrix}-m_{1}v_{1}-m_{2}v_{2}  -m_{2}v_{2}+m_2v_{1}  =-2m_{2}v_{2} +v_{1}(m_{2}-m_{1}) \\-m_{1}v_{1}-m_{2}v_{2} + m_{1}v_{2} -m_{1}v_{1} = -2m_{1}v_{1} + v_{2}(m_{1}-m_{2})\end{bmatrix} \\[1em]&=\left( \frac{1}{m_{1}+m_{2}} \right)\begin{bmatrix}2m_{2}v_{2} -v_{1}(m_{2}-m_{1}) \\2m_{1}v_{1} - v_{2}(m_{1}-m_{2})\end{bmatrix} \\[1em]\begin{bmatrix}v_{1,f} \\v_{2,f}\end{bmatrix} &=\begin{bmatrix}\frac{2m_{2}v_{2}}{m_{1}+m_{2}} - \frac{v_{1}(m_{2}-m_{1})}{(m_{1}+m_{2})} \\\frac{2m_{1}v_{1}}{(m_{1}+m_{2})}-\frac{v_{2}(m_{1}-m_{2})}{(m_{1}+m_{2})}\end{bmatrix}\end{align}$$
> That is: $$\boxed{\begin{aligned} v_{1,f} = \frac{2m_{2}v_{2}}{m_{1}+m_{2}} - v_{1} \frac{m_{2}-m_{1}}{m_{1}+m_{2}} \\[1em]v_{2,f} = \frac{2m_{1}v_{1}}{m_{1}+m_{2}} - v_{2} \frac{m_{1}-m_{2}}{m_{1}+m_{2}}\end{aligned}}$$
> Note that the equations above are symmetric with each other, the subscripts are simply swapped in the numerators. 

> [!theorem] Traditional Derivation
> Taking the equation $v_{1}+v_{1,f} = v_{2}+v_{2,f}$, we can rearrange this into something that substitutes out one of our velocities. 
> > Taking the final velocity of object one as something to back-substitute 
> > $v_{1,f}=v_{2}+v_{2,f} - v_{1}$
> > Plugging this into our equations above to the conservation of momentum: $$\begin{align}m_{1}v_{1} - m_{1}(v_{2} + v_{2,f} -v_{1}) &= m_{2}v_{2,f} -m_{2}v_{2} \\m_{1}v_{1} - m_{1}v_{2} - m_{1}v_{2,f} + m_{1}v_{1} &= m_{2}v_{2,f} - m_{2}v_{2} \\2m_{1}v_{1} - m_{1}v_{2}+ m_{2}v_{2}  & = m_{1}v_{2,f} + m_{2}v_{2,f} \\2m_{1}v_{1} -v_{2}(m_{1}-m_{2})  & =v_{2,f}(m_{1}+m_{2}) \\[1.5em]\frac{2m_{1}v_{1}}{m_{1}+m_{2}} - v_{2} \frac{m_{1}-m_{2}}{m_{1}+m_{2}}  & =v_{2,f}\end{align}$$
> > This equation above is equivalent to the equation that we got from the linear algebra derivation above. The other solution is essentially the same, just with all subscripts flipped.
> > 

### Perfectly Inelastic 
Perfectly inelastic collisions have a coefficient of restitution of $0$, meaning that the relative separation velocities of our objects are $0$, or in other words; our objects are stuck together. In this case, our momentum equations actually simplify significantly: 
$$
\begin{align}
m_{1}v_{1} + m_{2}v_{2} &= (m_{1}+m_{2})v_{f} \\
\frac{m_{1}v_{1} + m_{2}v_{2}}{m_{1}+m_{2}} & =v_{f}
\end{align}
$$
## Collisions in Higher Dimensions
Similarly to Kinematics, the underlying principle is that since Momentum is a property of mass *and* velocity, then we can solve it as with any multidimensional kinematics problem by simply solving it as separate one-dimensional momentum problems.

Note that the Conservation of Momentum (and corresponding coefficient of restitution) all remain constant across all dimensions of a problem unless otherwise stated. Simply break up into dimensional components; solve each individually; then solve for the resultant vector of the problem as usual. 