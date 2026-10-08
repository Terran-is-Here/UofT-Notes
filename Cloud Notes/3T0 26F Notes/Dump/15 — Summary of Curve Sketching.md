---
updated_at: 2026-10-08T10:28:29.511-04:00
edited_seconds: 340
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 15
Lecture Date: 2026-10-15
Week: 6
---
Hub: [[ESC194 Hub]]
Previous: [[14 — Derivatives, Function Shape, Horizontal Asymptotes]]
Next: [[16 — Optimization and Antiderivatives]]
> [!quote] Recommended Reading 
> Section 3.5 of the Stewart Textbook

--- 
# Lecture Notes

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