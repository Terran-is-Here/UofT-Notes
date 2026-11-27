---
updated_at: 2026-11-27T13:12:17.210-05:00
edited_seconds: 820
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 30
Lecture Date: 2026-11-22
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[29 — Fluid Dynamics]]
Next: [[31 — SHM Analysis and Pendulums]]
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
> Where $\omega = \frac{2\pi}{T}$ where $\omega$ represents the **angular frequency** of our system. Differentiating, we find that: 
> $$\begin{align}\frac{dx}{dt}  & =  -A\omega \sin(\omega t+\phi) \\\frac{d^{2}x}{dt^{2}}  & = -A\omega^{2}\cos(\omega t+\phi)\end{align}$$
> Noting that if $x$ is some function of position, then $\frac{dx}{dt}$ and $\frac{d^{2}x}{dt^{2}}$ correspond to functions of velocity and acceleration. As such, the corresponding values in front of our expression correspond to the max velocity and acceleration of our system respectively: 
> $$\begin{align}a_{max}  & = A\omega^{2} \\v_{max} & =A\omega\end{align}$$
> And $A$ itself is equivalent to the maximum deflection present within the spring. 

> [!caution]- Extending further into ODEs
> Note that with the expressions above, and with our differential, we can actually derive expressions for the Amplitude of our system from the initial conditions of our system (an IVP). Consider if we are given some value $x(0)$ and $v(0)$: 
> $$\begin{align}x(0)  & = A\cos(\phi) \\v(0)  & = -A\omega\sin(\phi) \to \frac{v(0)}{\omega} = -A\sin \phi\end{align}$$
> Then we can see that:
> $$\begin{align}x(0)^{2} + \left( \frac{v(0)}{\omega} \right)^{2}  &  = A^{2}\cos ^{2}(\phi) + A^{2}\sin ^{2} \\& =A^{2}(\cancel{ \cos ^{2}(\phi) + \sin ^{2}(\phi) }) & \cos ^{2}(\phi) + \sin ^{2}(\phi) = 1 \\x(0)^{2} + \left( \frac{v(0)}{\omega} \right)^{2} & = A^{2} \\\sqrt{ x(0)^{2} + \left( \frac{v(0)}{\omega} \right)^{2} }  & =A\end{align}$$
> Consider as well that: 
> $$\begin{align}\frac{\frac{v(0)}{\omega}}{x(0)}  & = \frac{-A\sin \phi}{A\cos \phi} \\\frac{v(0)}{\omega x(0)} & =-\tan \phi \\-\frac{v(0)}{\omega x(0)}  & =\tan \phi\end{align}$$

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
## Total SHM Energy
Consider now if we were asked the question: what is the energy of a simple harmonic oscillator? Consider the case in which a SHM is located on a frictionless table. We note that their potential energy would thus be defined as being based on the elastic potential energy present.
$$
W = \int -kx\,dx = \left\{-\frac{1}{2}kx^{2}\right|_{x_{1}}^{x_{2}} = -\Delta U
$$
Setting $x_{1}=0$ (as the equilibrium position), and $x_{2}=x$ (the displacement), then: 
$$
\frac{1}{2}kx^{2} = U
$$
Conversely, we know that the energy of our spring will also have a term of kinetic energy, thus: 
$$
\frac{1}{2}mv^{2} = K
$$
Solving for the total energy, and noting that $v=\frac{dx}{dt}$, and that our differential is in terms of Hooke's Law, then:, $\frac{d^{2}x}{dt^{2}} = -\frac{k}{m}x \implies \omega^{2}=\frac{k}{m}$
$$
\begin{align}
E_{T}  & = \frac{1}{2}kx^{2} + \frac{1}{2}mv^{2} \\
 & =\frac{1}{2}k(A\cos(\omega t + \phi))^{2} + \frac{1}{2}m(-A\omega \sin (\omega t+\phi))^{2} \\
 & =\frac{1}{2}kA^{2}\cos ^{2}(\omega t+\phi) + \frac{1}{2}mA^{2}\omega^{2}\sin ^{2}(\omega t+\phi) & \omega^{2} = \frac{k}{m} \\
 & =\frac{1}{2}kA^{2}\cos ^{2}(\omega t+\phi) + \frac{1}{2}\cancel{ m }A^{2} \frac{k}{\cancel{ m }}\sin ^{2}(\omega t+\phi) \\
 & = \frac{1}{2}kA^{2}(\cancel{ \cos ^{2}(\omega t+\phi) + \sin ^{2}(\omega t+\phi) }) & \cos ^{2}(x) + \sin ^{2}(x) = 1 \\
 E_{T}& = \frac{1}{2}kA^{2} 
\end{align}
$$
Note that this implies that, for a spring on a flat table, the corresponding value for the total energy is defined in terms of the maximum amplitude of the spring, as well as the spring constant. This implies that the spring energy of the system is actually constant! 

Because of this, we can now actually solve for the corresponding velocity of our object at any given point $x$: 
$$
\begin{align}
 \cancel{ \frac{1}{2} }kx^{2} + \cancel{ \frac{1}{2} }mv^{2}  & =\cancel{ \frac{1}{2} }kA^{2} \\
 kx^{2} + mv^{2} & = kA^{2} \\
 mv^{2} & = k(A^{2}-x^{2}) \\
 \left| v \right| & = \sqrt{ \frac{k}{m}(A^{2}-x^{2}) }
\end{align}
$$
Note that this expression fails to exist if $A^{2}<x^{2}$, as this resolves in an imaginary number. 
