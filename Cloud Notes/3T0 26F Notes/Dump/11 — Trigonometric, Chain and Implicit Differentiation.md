---
updated_at: 2026-10-05T11:28:21.392-04:00
edited_seconds: 1550
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
Next: [[12 — Related Rates, Min and Max Values]]
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
\text{arc BA} = \pi r^2 *\left( \frac{\theta}{2\pi} \right) =\frac{(1)^2\theta}{2} &= \frac{1}{2}\theta \\
\triangle ODA &= \frac{1}{2}\tan\theta
\end{align}
$$
Therefore, our inequality becomes: 
$$
\begin{align}
\frac{1}{2}\sin\theta &< \frac{1}{2}\theta < \frac{1}{2}\tan\theta \\
\sin\theta &< \theta < \frac{\sin\theta}{\cos\theta} & \text{Divide by a term of }\sin\theta \\
1 &< \frac{\theta}{\sin\theta} < \frac{1}{\cos\theta} &\text{ Take the reciprocal} \\
1 &> \frac{\sin\theta}{\theta} > \cos\theta & \text{Take the limits} \\
\cos\theta < \frac{\sin\theta}{\theta} < 1 \implies \lim_{ \theta \to 0 } 1 &< \lim_{ \theta \to 0 } \frac{\sin\theta}{\theta} < \lim_{ \theta \to 0 } \cos\theta \\
1 &< \lim_{ \theta \to 0 } \frac{\sin\theta}{\theta} < 1
\end{align}
$$
Therefore from squeeze theorem, $\lim_{ \theta \to 0 } \frac{\sin\theta}{\theta} = 1$.
> [!caution] 
> Take the one-sided limits as needed before taking the bidirectional limit, as you still need to show that you can take it inherently. Either that or $\epsilon-\delta$, pick your poison.
## Other Trigonometric Derivatives 
Using the same methods as earlier, you can solve for the other trigonometric derivates as shown below: 
* $$\frac{d}{dx}\tan(x) = \sec^2(x)$$
* $$\frac{d}{dx}\cot(x)=-\csc^2(x)$$
* $$\frac{d}{dx}\sec(x) = \sec(x)\tan(x)$$
* $$\frac{d}{dx}\csc(x) =- \csc(x)\cot(x)$$
## Chain Rule 
Say that we want to differentiate the following: 
$$
f(x) = (3x^2 + 1)^{173}
$$
Note that if we let $u = 3x^2 + 1$, then $f(x) = f(u(x)) = u^{173}$
Then: 
$$
\frac{d}{dx}f(x) = \frac{df(u)}{du}* \frac{du}{dx}
$$
Or: 
$$
\begin{align}
f(g(x)) = f'(g(x))g'(x) \\
f \circ g(x) \implies f'(g)g'
\end{align}

$$
For instance: $\frac{d}{dx}\sin(3x^2+2)$, Let $u = 3x^2 + 2$, then: 
$$
\begin{align}
\frac{d}{dx}\sin(3x^2 + 2) = \cos(3x^2+2)*6x
\end{align}
$$
### Extending Chain Rule 
Take the following: 
$$
y=y(u), u=u(x), x=x(t)
$$
Then: 
$$
\frac{dy}{dt} = \frac{dy}{du} \frac{du}{dx} \frac{dx}{dt}
$$
For example: 
$$
\begin{align}
y(u) = (u+1)^2 \\
u(x) = x^3 \\
x(t) = 14-t
\end{align}
$$
Then: 
$$
\begin{align}
\frac{dy}{du} = 2(u+1) \\
\frac{du}{dx} = 3x^2 \\
\frac{dx}{dt} = -1
\end{align}
$$
Then: 
$$
\begin{align}
\frac{dy}{dt} &= 2(u+1)(3x^2)(-1) \\
&=-x(x^3+1)
\end{align}

$$
## Explicit and Implicit Functions
Explicit functions are defined as having all independent variables on one side, and a dependent on the left, such as $y=\frac{x^2+1}{x^3}$. 

An implicitly defined function is where this is defined as a combination of $x,y$, such as $x^3y-x^2-1=0$. Note that if we define $y=y(x)$, then if we differentiate this, then: 
$$
\begin{align}
\frac{d}{dx}(x^3y-x^2-1) &= \frac{d}{dx}(0) \\
x^3 \frac{dy}{dx} + 3x^2y -2x&= 0 \\
\frac{dy}{dx} = \frac{2x-3x^2y}{x^3}
\end{align}
$$
Note that we can isolate for a term of $y$ in our original expression, that is $y=\frac{1+x^2}{x^3}$; then we can back-substitute this back into some explicit derivative of $\frac{dy}{dx}$. 
> [!ila] In Lecture Addendum 
> Implicit differentiation does not require us to separate our independent variables to differentiate!

For instance, taking the function: 
$$
\begin{align}
x^3y\sin (x^{1/3}y) = \frac{1}{1-xy}
\end{align}
$$
We can't isolate this as some sole term of $y$ as a function of $x$; we can implicitly differentiate this: 
$$
\begin{align}
x^3y\sin\left(x^{1/3}y \right)=\frac{1}{1-xy}
\end{align}$$ Will be done later. 
$$$$
### Higher Order Implicit Differentiation: 
For instance, take $y^3-x^2=4$. 
The first derivative with respects to dx gives us: 

$$
\begin{align}
\frac{d}{dx}(y^3-x^2) = 3y^2y'-2x= 0 \\
\implies y' = \frac{2x}{3y^2}
\end{align}
$$
Taking the second derivative with respects to $\frac{d}{dx}$, then: 
$$
\begin{align}
y'' &= \frac{d}{dx} \left( \frac{2x}{3y^2} \right) \\
&=\left( \frac{2(3y^2)-6yy'2x}{9y^4} \right)
\end{align}
$$
## Extending the Power Rule to Rational Powers
Recall, that $\frac{d}{dx}x^n=nx^{n-1}$ for $n\in \mathbb{Z}$. We can show that we can extend this to *all rational numbers*. 

That is, prove that $$\frac{d}{dx}x^{p/q} = \frac{p}{q}x^{(p/q)-1}$$where $q\neq0$

Let $y=x^{p/q}$, then $y^q=x^p$. Differentiating this implicitly with respects to $x$: 
$$
\begin{align}
\frac{d}{dx}y^q &= \frac{d}{dx}x^p \\
qy^{q-1}y' &= px^{p-1} \\
y'&=\frac{px^{p-1}}{qy^{q-1}} & \text{Resubstitute back y} \\
y' &= \frac{px^{p-1}}{q(x^{p/q})^{q-1}} = \frac{p}{q}x^{(p/q)-1}
\end{align}

$$

---
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


