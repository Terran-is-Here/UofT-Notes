---
updated_at: 2026-10-09T23:37:12.637-04:00
edited_seconds: 430
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
We can actually relate these together in a linear system: 
$$
\begin{bmatrix}m_{1} & m_{2} \\1 & -1\end{bmatrix}\begin{bmatrix}
v_{1}
\end{bmatrix}
$$