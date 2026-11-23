---
updated_at: 2026-11-22T19:30:44.091-05:00
edited_seconds: 430
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 30
Lecture Date: 2026-11-22
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[29 — Fluid Dynamics]]
Next: N/A
> [!quote] Recommended Reading 
> University Physics, 15.1—15.2 
> [[31 —Differentials and Separable Equations]] from ESC194 is also a good idea. 

> [!caution] Note
> This note will be using the differential equation approach to this, mainly since this way makes a lot more sense to me now. 

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Overview
We retake some of the definitions of oscillating systems here, just for the sake of the completeness of the note: 
* The frequency of an oscillating system is defined as the number of events per unit of time, that is:
  $$f = \frac{1}{T}$$
* The Period is the time elapsed per oscillation, and is defined by $T$. 
Frequency is defined in terms of Hertz (Hz), or in reciprocal seconds.
## Simple Harmonic Motion
> [!theorem] Simple Harmonic Motion (SHM)
> In a system undergoing Simple Harmonic Motion, the acceleration of the system (and thus the net force) is proportional to the displacement, and acts in the **opposite** direction of the displacement. 

> An example of a system undergoing SHM is a system attached onto a spring on a frictionless setting, where: 
> 
> $$F_{s} = -kx \implies -kx = ma$$

Simple Harmonic Motion (without damping) can be described as the following differential. Let $x$ be a function of position with respects time, and we note that the corresponding acceleration is opposite the direction of displacement. 
$$
\frac{d^{2}x}{dt^{2}} = -Cx
$$
Where $C>0$. Solving this differential can be done by setting our function of velocity to be some trigonometric function, that is: 
$$
x = A\cos\left( \frac{2\pi}{T}t +\phi\right) = A\cos(\omega t+\phi)
$$
From here, we actually derive the Equations of Simple Harmonic Motion: 

> [!theorem] Equations of SHM
> If we define SHM as the following differential equation: 
> $$\frac{d^{2}x}{dt^{2}}=-Cx$$
> We note that $x$ is a function of position based on some time, and that the solution to this differential is: 
> $$x=A\cos(\omega t+\phi)$$
> Where $\omega = \frac{2\pi}{t}$ where $\omega$ represents the **angular frequency** of our system. Differentiating, we find that: 
> $$\begin{align}\frac{dx}{dt}  & =  -A\omega \sin(\omega t+\phi) \\\frac{d^{2}x}{dt^{2}}  & = -A\omega^{2}\cos(\omega t+\phi)\end{align}$$
> Noting that if $x$ is some function of position, then $\frac{dx}{dt}$ and $\frac{d^{2}x}{dt^{2}}$ correspond to functions of velocity and acceleration. As such, the corresponding values in front of our expression correspond to the max velocity and acceleration of our system respectively: 
> $$\begin{align}a_{max}  & = A\omega^{2} \\v_{max} & =A\omega\end{align}$$

Plugging this into our differential, we find that: 
$$
\begin{align}
\frac{d^{2}x}{dt^{2}} & = -Cx \\
-A\omega^{2}\cos(\omega t +\phi) & = -CA\cos(\omega t + \phi) & \text{recall } A\cos(\omega t+\phi) = x(t) \\
-\omega^{2}x(t) & =-Cx(t) \\
\implies \omega^{2} & =C  \\
\implies \omega & =\pm\sqrt{ C }
\end{align}
$$

Recall that in an earlier example, we set our SHM to be based in terms of our elastic spring system, then: 
$$
\begin{align}
ma  & = -kx \\
\frac{d^{2}x}{dt^{2}}  & = -\frac{k}{m}x & C=\frac{k}{m} \\
\implies \omega  & =\sqrt{ \frac{k}{m} }
\end{align}
$$

