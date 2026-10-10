---
updated_at: 2026-10-10T13:48:35.636-04:00
edited_seconds: 1230
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 15
Lecture Date: 2026-10-15
Week: 6
---
Hub: [[PHY180 Hub]]
Previous: [[14 — Momentum and Impulse]]
Next:
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
v_{1}+v_{1,f}&= v_{2} + v_{2,f}  \\
\implies v_{1}-v_{2} &= v_{2,f}-v_{1,f}
\end{align}
$$
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
> That is: $$\boxed{\begin{aligned} v_{1,f} = \frac{2m_{2}v_{2}}{m_{1}+m_{2}} - v_{1} \frac{m_{2}-m_{1}}{m_{1}+m_{2}} \\[1em]v_{2,f} = \frac{2m_{1}v_{1}}{m_{1}+m_{2}} - v_{1} \frac{m_{1}-m_{2}}{m_{1}+m_{2}}\end{aligned}}$$
> Note that the equations above are symmetric with each other, the subscripts are simply swapped in the numerators. 
