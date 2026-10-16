---
updated_at: 2026-10-16T13:24:26.563-04:00
edited_seconds: 970
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 15
Lecture Date: 2026-10-15
Week: 6
Created: October 8th 2026, 9:10:38 am
---
Hub: [[ESC194 Hub]]
Previous: [[14 — Derivatives, Function Shape, Horizontal Asymptotes]]
Next: [[16 — Optimization, Antiderivatives and Sigma Notation]]
> [!quote] Recommended Reading 
> Section 3.5 of the Stewart Textbook

--- 
# Lecture Notes
## Horizontal Asymptotes
Recall how we defined the concept of a *vertical* asymptote: The value of a function diverges into infinity either from one or both sides into $\pm \infty$; 

By contrast; we can define the concept of the horizontal asymptote as the following: 
$$
\lim_{ x \to \infty } f(x) =L  \lor \lim_{ x \to -\infty } f(x) = L \implies y=L \text{ is the horizontal asymptote of }f(x)
$$
From here, we need to derive a new definition as to how we should actually formally describe the concept of an infinite limit. For limits at infinity: 

Let $f(x)$ be defined on some interval $(a,\infty)$, then: 
$$
\begin{align}
\lim_{ x \to \infty } f(x)  & = L \\
 & \implies \forall\epsilon>0,\exists N \text{ s.t. } \\
x > N  & \implies |f(x)-L| < \epsilon
\end{align}
$$
An example: 
$$
\lim_{ x \to \infty }  \frac{x^2-1}{x^2+1} = 1
$$
Then; from above: 
$$
\begin{align}
\forall\epsilon>0, \exists N \text{ s.t} \\
x > N  & \implies \left|\frac{(x^2-1)}{x^2+1} -1\right| < \epsilon \\
 & \implies \left|\frac{-2}{x^2+1}\right| = \frac{2}{x^2+1} < \epsilon \implies \frac{2}{x^2} < \frac{2}{x^2+1} < \epsilon \\
 &\implies \frac{2}{x^2} < \epsilon \implies \frac{2}{\epsilon} < x^2 \implies x > \sqrt{ \frac{2}{\epsilon} } = N \\
\end{align}
$$
Choosing $\sqrt{ \frac{2}{\epsilon} }$ as $N$, then: 
$$
\left|\frac{(x^2-1)}{x^2+1} -1\right| < \frac{2}{x^2+1} < \frac{2}{x^2} < \frac{2}{N^2} < \frac{2}{\left( \frac{2}{\epsilon} \right)} = \epsilon 
$$

## Evaluating Infinite Limits 
Consider the following limit: 
$$
\lim_{ x \to \infty } \frac{6x^2+x+5}{2x^2-x+3} = \lim_{ x \to \infty } \frac{\left( x^2\left( 6 + \frac{1}{x} + \frac{5}{x^2} \right) \right)}{x^2\left( 2-\frac{1}{x}+\frac{3}{x^2} \right)} = \frac{6}{2} = 3
$$
This requires us to however see that; 
$$
\lim_{ x \to \infty } \frac{1}{x^r}=0
$$
Which we can easily prove: 
$$
\begin{align}
\forall\epsilon>0, \exists N \text{ s.t. } \\
x > N  & \implies \left|\frac{1}{x^r}\right| < \epsilon \\
 & \implies \left| \frac{1}{x}\right|^r < \epsilon  \implies \frac{1}{x} < \sqrt[r]{ \epsilon } \\
 & \implies \frac{1}{\sqrt[r]{ \epsilon }} < x \implies N = \frac{1}{\sqrt[n]{ \epsilon }}
\end{align}
$$
Then we can prove the forward direction as required. 

## Infinite Limits at Infinity 
Take the following: 
$$
\lim_{ x \to \infty } x^2=\infty
$$
To formally prove this; then: 
$$
\begin{align} 
f(x)\text{ defined on } (a,\infty)\\
\lim_{ x \to \infty } f(x) = \infty \text{ can be stated as} \\
\forall M>0, \exists N>0\text{ s.t. } \\
x > N \implies f(x) > M
\end{align}
$$
## Indeterminate Forms 
Consider the following: 
$$
\lim_{ x \to \infty } x^3-x^2=\infty-\infty????
$$
Consider rewriting this function as the following: 
$$
\lim_{ x \to \infty } x^2(x-1) = \infty*\infty??
$$
Note that intuitively; $\infty\pm\infty \land \infty*\infty = \infty$. However, what do we do with $\frac{\infty}{\infty}$ and $\infty-\infty$? These should be avoided; and these are what we term as indeterminate forms (also including $\frac{0}{0}$, etc. )

## Vertical Tangents and Cusps 
Recall the concept of a vertical tangent; the idea that a tangent expression explodes out to infinity. We can formally define it here. 

> Vertical Tangent
> Let $f(x)$ be continuous at $x=c$, if $\lim_{ x \to c }f'(x) = \pm \infty$, then we say that a vertical tangent exists at $x=c$. 

> Vertical Cusp
> $f(x)$ is continuous at $x=c$, and $\lim_{ x \to ^-c }f(x) = \mp\infty$ and $\lim_{ x \to ^+c }f(x) = \pm\infty$, then $x=c$ has a vertical cusp. 

For instance, take the following: 
$$
	\begin{align}
	f(x) &  = 3 + (x+1)^{2/3} \\
	f'(x)  & =\frac{2}{3(x+1)^{1/3}} \\
	\lim_{ x \to ^--1 } f'(x) & =-\infty \\
	\lim_{ x \to ^+-1 } f'(x) & =\infty \implies f(x) \text{ has a vertical cusp at } x=-1
	\end{align}

$$
## Slant Asymptotes (Oblique Asymptotes) 
Slant Asymptotes are defined as the following: 
$$
\lim_{ x \to \infty } [f(x)-(mx+b)] = 0
$$
Where $mx+b$ is our Oblique Asymptote; or in other words, $f(x) \to (mx+b)$. 

## Curve Sketching Procedure
1. Find the domain of the function, and end points if they exist.
2. Find $y,x$ intercepts if they exist. 
3. Determine the shape of the function (symmetry? periodicity?) 
4. Find asymptotes (if any) 
	1. Vertical, Horizontal, Oblique
5. Find the derivative of the function if it exists; determine CPs -> IoIs and IoDs, VTs / VCs 
6. Find the second derivative if it exists; determine PoInf -> Changes in Concavity
7. Evaluate extremums. 

For instance, sketch the following: 
$$
f(x) = \frac{1}{4}x^4 - 2x^2 + \frac{7}{4}
$$
Following our steps: 
1. All $x\in$ domain, no end points. 
2. Intercepts
	1. $f(0) = \frac{7}{4}$ y intercept, 
	2. Solutions are $x=\pm_{1}, \pm \sqrt{ 7 }$
3. Symmetry: 
	1. Function has even symmetry (test via $f(x)=f(-x)$), which holds true. 
4. Asymptotes
	1. No asymptotes detected ($\lim_{ x \to \pm\infty }f(x)=\pm \infty$)
5. Derivative of the function: $f'(x) = x^3 -4x=x(x^2-4)=x(x+2)(x-2)$, solutions for CPs are $x=0,\pm2$; no cases where VTs/VCs arise. 
	1. Intervals of Decrease: $(-\infty,-2)\cup(0,2)$
	2. Intervals of Increase: $(-2,0)\cup(2,\infty)$
6. Second Derivative of the function: $f''(x) = 3x^2 -4$, Then solutions for $f''(x)=0$ are $x=\pm\frac{2}{\sqrt{ 3 }}$: 
	1. Concave Up: $\left( -\infty,-\frac{2}{\sqrt{ 3 }} \right)\cup\left( \frac{2}{\sqrt{ 3 }},\infty \right)$
	2. Concave Down: $\left( -\frac{2}{\sqrt{ 3 }}, \frac{2}{\sqrt{ 3 }} \right)$
	3. Inflection points are present at $x=\pm \frac{2}{\sqrt{ 3 }}$. 
7. Local Extrema. 
	1. We can find local extrema using our critical points: $0,\pm2$, Using the second derivative test: 
	2. $f''(0)=-4 <0 \implies$ $f(0)$ is a local max. 
	3. $f''(2)=f''(-2)=8 >0 \implies$ $f(-2),f(2)$ is a local min. 

---
# Pre-Lecture Notes
## Curve Sketching
Curve Sketching is predominantly based on the tests that we have derived within the previous chapter; primarily taking end behaviors (limits to infinity), Points of Inflection, IoC/IoD, etc. Recall the tests that we had for these. 

> [!theorem] Intervals of Increase / Decrease Test 
> > $f'(c)>0$ in some interval, then that interval is an interval of *increase*. 
> > $f'(c)<0$, in some interval, then that interval is an interval of *decrease*. 

> [!theorem] Concavity Test
> > $f''(x) > 0, x\in I \implies I$ is a concave *up* interval for $f(x)$. 
> > $f''(x) < 0, x\in I \implies I$ is a concave *down* interval for $f(x)$. 

> [!theorem] First Derivative Test 
> Let $f$ have a critical number at some value $c$, then: 
> > If $f'(c)$ goes from $+ \to -$, $f(c)$ is a local maximum. 
> > If $f'(c)$ goes from $- -\to +$, $f(c)$ is a local minimum. 
> > If $f'(c)$ goes from $- \to -\lor+ \to+$, then $f(c)$ is neither. 

> [!theorem] Second Derivative Test
> If $f''(c)$ exists at some value $c$ then: 
> > $f'(c)=0 \land f''(c)>0$, then $f(c)$ is a local minimum. 
> > $f'(c)=0\land f''(c)<0$, then $f(c)$ is a local maximum. 

We generally follow the following steps: 
1. Determine the *domain* of the function. 
2. Determine the *intercepts* of the function ($y$ intercepts, and $x$ intercepts if they aren't too difficult to derive) 
3. Determine if the function has some kind of symmetry, or has some kind of periodicity.
	1. $f(c)=f(-c)$ implies a symmetry across $y$
	2. $f(-c)=-f(c)$ implies a symmetry across the origin (rotational symmetry) 
	3. $f(c+p) = f(c),p\in \mathbb{R}\neq0$, implies a periodicity, where our function is repeated after some period $p$. 
4. Determine Asymptotes: 
	1. Recall our definition for them: $$\begin{align}\lim_{ x \to ^+a } f(x) = \pm \infty && \lim_{ x \to ^-a } f(x) = \pm \infty\end{align}$$
	   Where the sign is dependent on what direction this limit ends up taking. 
	2. Also determine if a *horizontal* asymptote exists. 
5. Intervals of Increase / Decrease 
	1. Use the intervals of increase / decrease test that we had above. 
6. Determine Local Maxima / Minima 
	1. Use either the First or Second Derivative test (though the first is often ideal) 
7. Determine changes in Concavity
	1. Use the Concavity test to determine changes in concavity. 
Following all the information above; then from this we can start sketching our behavior. 