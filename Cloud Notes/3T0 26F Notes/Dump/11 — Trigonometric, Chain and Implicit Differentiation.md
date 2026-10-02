---
updated_at: 2026-10-02T13:51:31.372-04:00
edited_seconds: 1070
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 11
Lecture Date: 2026-10-02
Week: 4
Created: September 27th 2026, 12:09:30 pm
---
Hub: [[ESC194 Hub]]
Previous: [[10 — Differentiation Formulas and Applied Derivatives]]
Next: N/A 
> [!quote] Recommended Reading 
> Stewart Textbook: 2.4-2.6
--- 
# Lecture Notes
## Derivative of Sin(x) 
See the proof at the top of the Trigonometric Derivatives section in this note, however an alternative geometric proof exists. Retaking the following diagram: 
![[11 — Trigonometric, Chain and Implicit Differentiation-1790605672585.webp]]
We can define this in terms of the inequality of areas, that is $\triangle OBA_{A} < \text{arc BA} < \triangle ODA_{A}$
$$
\begin{align}
\triangle OBA_{A} = \frac{1}{2}*\sin\theta &= \frac{1}{2}\sin\theta \\
\text{arc BA} = \pi r^2 *\left( \frac{x}{2\pi} \right) =\frac{(1)^2x}{2} &= \frac{1}{2}x \\
\triangle ODA &= \frac{1}{2}\tan\theta
\end{align}
$$
Therefore, our inequality becomes: 
$$
\begin{align}
\frac{1}{2}\sin\theta &< \frac{1}{2}x < \frac{1}{2}\tan\theta \\
\sin\theta &< x < \frac{\sin\theta}{\cos\theta} & \text{Divide by a term of }\sin\theta \\
1 &< \frac{x}{\sin\theta} < \frac{1}{\cos\theta} &\text{ Take the reciprocal} \\
1 &> \frac{\sin\theta}{x} > \cos\theta & \text{Take the limits} \\
\cos\theta < \frac{\sin\theta}{x} < 1 \implies \lim_{ \theta \to 0 } 1 &< \lim_{ \theta \to 0 } \frac{\sin\theta}{x} < \lim_{ \theta \to 0 } \cos\theta \\
1 &< \lim_{ \theta \to \infty } \frac{\sin\theta}{x}
\end{align}
$$
## Other Trigonometric Derivatives 
Using the same methods as earlier, you can solve for the other trigonometric derivates as shown below: 
* $$\frac{d}{dx}\tan(x) = \sec^2(x)$$
* $$\frac{d}{dx}\cot(x)=\csc^2(x)$$
* $$\frac{d}{dx}\sec(x) = \sec(x)\tan(x)$$
* $$\frac{d}{dx}\csc(x) =- \csc(x)\cot(x)$$
# Pre-Lecture Notes
## Trigonometric Derivatives
Trigonometric Derivatives can be generally obtained from the Differentiation Formulas that we derived in our previous note, as well as some angle sum identities. For this segment, we will take the derivative of $\sin(x)$: 
$$
\begin{align}
f(x) &= \sin(x) \\
f'(x) &= \lim_{ h \to 0 } \frac{\sin(x+h)-\sin(x)}{h} \\
&= \lim_{ h \to 0 } \frac{\sin (x)\cos(h) + \sin(h)\cos(x) - \sin(x)}{h} \\
&=\lim_{ h \to 0 } \frac{\sin (x)\cos(h) - \sin(x)+ \sin(h)\cos(x) }{h}  \\
&= \lim_{ h \to 0 } \sin(x) \frac{\cos(h)-1}{h} + \lim_{ h \to 0 } \frac{\sin(h)\cos(x)}{h} \\
&= \sin(x) \lim_{ h \to 0 } \frac{\cos(h)-1}{h} + \cos(x)\lim_{ h \to 0 } \frac{\sin(h)}{h} &\lim_{ h \to 0 } \frac{\cos(h)-1}{h} =0 &&\lim_{ h \to 0 } \frac{\sin(h)}{h}=1\\ \\
&=\sin(x)(0) + \cos(x)(1)  \\
&=\cos(x)
\end{align}
$$
Note that the two limits that we have shown on the right will be proved in their respective subsection
### Trigonometric Derivatives 


### Special Trigonometric Limits 
The following are two useful identities that we can have for evaluating some limits and potential derivatives. 

> The following holds true: 
> $$\lim_{ x \to 0 } \frac{\sin(x)}{x} = 1$$

> [!theorem]- *Proof*
> Take the following diagram: 
> ![[11 — Trigonometric, Chain and Implicit Differentiation-1790605672585.webp]]
> Where $\theta$ is within $0<\theta< \frac{\pi}{2}$, And where $|BC| = |OB|\sin\theta = \sin\theta$. Note that in this case, $\text{arc BA} = \theta r = \theta$
> From here, we can tell that:$$\begin{align}|BC| < |AB| &< \text{arc AB} \\\sin\theta &< \theta \\\frac{\sin\theta}{\theta} &< 1 \end{align}$$
> Note that we now extend the tangent lines from $A$ and $B$, when note that $\text{arc AB} < |DA| = |OA|\tan\theta = \tan\theta$
> Then we have the set of following relations: 
> $$\begin{align}\frac{\sin\theta}{\theta} < 1\\\theta < \tan\theta \implies \theta < \frac{\sin\theta}{\cos\theta}\end{align}$$
> From here: $$\begin{align}\theta &< \frac{\sin\theta}{\cos\theta}  \\\implies \cos\theta &< \frac{\sin\theta}{\theta}  \\\implies \cos\theta &< \frac{\sin\theta}{\theta} <1 \\\lim_{ \theta \to 0 } \cos\theta &< \lim_{ \theta \to 0 }  \frac{\sin\theta}{\theta} < \lim_{ \theta \to 0 } 1 & \text{Following from Squeeze Theorem, then} \\\implies \lim_{ \theta \to 0 } \frac{\sin\theta}{\theta} &= 1\end{align}$$


> The following also holds true: 
> $$\lim_{ x \to 0 } \frac{\cos(x) - 1}{x} = 1$$

> [!theorem]- *Proof*
> Multiply numerator and denominator by a term of $\cos(x) + 1$
> $$\begin{align}\lim_{ x \to 0 } \frac{\cos(x)-1}{x}& =\lim_{ x \to 0 } \frac{\cos(x)-1}{x} \frac{(\cos(x) +1)}{(\cos(x) +1)} \\&= \lim_{ x \to 0 } \frac{\cos^2(x)-1}{x(\cos(x) + 1)} \\&= \lim_{ x \to 0 } \frac{-\sin^2(x)}{x(\cos(x) + 1)} \\&=-\left[\lim_{ x \to 0 } \frac{\sin(x)}{x}\right] \left[ \lim_{ x \to 0 } \frac{\sin (x)}{\cos(x) + 1} \right] & \text{Using } \lim_{ x \to 0 } \frac{\sin(x)}{x} = 1 \\&=-1\left[ \lim_{ x \to 0 } \frac{\sin (x)}{\cos(x) + 1} \right]& \text{Evaluating the limits} \\&=-1* \frac{0}{2} = 0 \\\lim_{ x \to 0 } \frac{\cos(x)-1}{x}&= 0\end{align}$$

Note that if we can algebraically manipulate a term into one of these forms, we can back substitute this as their corresponding values. 

## Chain Rule 
Take the following function: 
$$F(x) = \sqrt{ x^2 +1 }$$
Note that this can be expressed as some function composition of $f\circ g(x)$, where $f(x) = \sqrt{ x }$, and $g(x) = x^2 +1$. The chain rule is generally defined as the following: 

> Given some function $F(x) = f\cdot g(x) = f(g(x))$, then: 
> $$F'(x) = f'(g(x))g(x) = \frac{df}{dg} \frac{dg}{dx}$$

## Implicit Differentiation
Implicit Differentiation essentially allows us to take the derivative of functions taken implicitly. For instance, take the following implicitly defined function: 
$$
x^2 +y^2 = 25
$$
We *can* define this in terms of $x$ as two separate functions. What happens if we take the derivative of this function? In this case, we can perform some *implicit* differentiation. Note that we can define $y$ as some function of $x$, therefore taking the derivative on both sides with respect to $x$:
$$
\begin{align}
2x + 2y \frac{dy}{dx} &= 0 \\
\frac{dy}{dx}&=-\frac{2x}{2y} \\
&= -\frac{x}{y}
\end{align}
$$
This equation gives us the equation of the slope of a point on our original implicit function of $x^2 + y^2 = 25$. Note that $y^2 \to y(x)^2 \to 2y(x)y'(x) \to 2yy'$. 


