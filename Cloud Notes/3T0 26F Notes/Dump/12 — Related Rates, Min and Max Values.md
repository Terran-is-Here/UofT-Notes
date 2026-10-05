---
updated_at: 2026-10-05T13:31:29.075-04:00
edited_seconds: 1090
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 12
Lecture Date: 2026-10-04
Week: 5
Created: October 4th 2026, 6:14:03 pm
---
Hub: [[ESC194 Hub]]
Previous: [[11 — Trigonometric, Chain and Implicit Differentiation]]
Next: [[13 — Mean Value Theorem, Linear Approximations and Differentials]]
> [!quote] Recommended Reading 
> Stewart Textbook Ch. 2.8, 3.1 
--- 
# Lecture Notes
## Related Rates (LEC) 
Take an example: 
> A lighthouse is on an island 3km away from a straight shoreline, and the light makes 4 rotations per minute. How fast is the beam of light from the lighthouse moving along the shoreline when the beam is 1km from the closest point on the shore? 

I'd draw a diagram but I don't have a diagram drawing software. Note that the lighthouse is *always* 3km from the shore. Then, from the closest point of the shore, the distance between the lighthouse's closest point and the beam is some value $x$. 

This question basically asks, can we relate the rate of rotation with the velocity of the beam. Note that: 
$$
\tan\theta = \frac{x}{3}
$$
Differentiating this with respects to $t$; then: 
$$
\begin{align}
\frac{d}{dt}\tan\theta = \frac{d}{dt} \frac{x}{3} \\
\sec^2\theta \ \frac{d\theta}{dt} =  \frac{1}{3} \frac{dx}{dt} \\
\frac{dx}{dt} &= 3\sec^2\theta  \frac{d\theta}{dt}
\end{align}
$$
Note that the beam revolves at 4 revolutions per minute. Note that this is equivalent to $\frac{8\pi}{min}=\frac{d\theta}{dt}$: Then we can evaluate this at the point of interest (which in our case is when the beam is is one 1km from the closest point of the shore), that is our point of interest is $x=1$:
$$
\begin{align}
\frac{dx}{dt}|_{x=1} = 3\sec^2(\theta|_{x=1})8\pi
\end{align}
$$
To evaluate our $\theta|_{x=1}$ recall that $\sec^2\theta = \tan^2\theta+1$; and $\tan\theta$ at $\theta=1$ means $\tan\theta=\frac{1}{3}$; then we can see that: 
$$
\begin{align}
\frac{dx}{dt}|_{x=1} &= 3\left( \frac{1}{3}^2+1 \right)8\pi \\
&=\frac{10}{3}8\pi \\
&=\frac{80\pi}{3} \text{km/m}
\end{align}$$
## Maximum and Minimum Values (LEC) 
* A function is considered to have a *local maximum* at $x=c\iff f(c)\geq f(x) \ \forall x\text{ sufficiently close to }c$ (This is an *intuitive* description for what close means.) 
* A function if considered to have a *local minimum* at $x=c\iff f(c)\leq x \ \forall x\text{ sufficiently close to }c$.  

From here, we can extend this to absolute maximum and minimums: Given $x=c\in D$ where $D$ is the domain of f.
* $f(c)$ is the absolute maximum of $f\in D$ if $f(c)\geq f(x) \ \forall x\in D$. 
* $f(c)$ is the absolute minimum of $f\in D$ if $f(c)\leq f(x) \ \forall x\in D$

> Example: $f(x)=x^2$,where $x\in(-\infty,\infty)$
> This creates a parabola. Note that $f(0)=0 \leq f(x)\ \forall x\in(-\infty,\infty)$, then $f(0)$ is an absolute minimum for $f(x)\in(-\infty,\infty)$. Note additionally that this function does not have an absolute maxima. 

> Example: $f(x)=\sin(x)$ where $x\in(-\infty,\infty)$
> Note that this sinusoidal function has *infinitely many* local minima and maxima. Note that since these all share the same value; then there are an *infinite* number of local and absolute minima and maxima on $(-\infty,\infty)$. 

## Extreme Value Theorem (LEC) 
> [!theorem] EVT (Extreme Value Theorem) 
> If $f$ is a continuous on the closed interval $[a,b]$, then $f$ takes on at least one *minimum* and *maximum* value on $[a,b]$. 
> > Note that $f$ needs to be continuous **on a closed interval**. 
> 

*Proof:* (Provided in the *supplement*, so really just a transcript of the section in [[12 — Related Rates, Min and Max Values#Extreme Value Theorem|EVT (below)]]). 

> Lemma 1.1
> If $f$ is continuous on a closed interval $[a,b]$, then $f$ is also bounded on $[a,b]$. 

From this we can work on a proof. Then, assume $f(x)$ is continuous as given in the theorem, then by Lemma 1.1, $f$ is bounded. 

Let $M$ be the Least Upper Bound of $f$ on $[a,b]$. Recall that from [[02 — The Real Number System#Completeness of the Reals Axiom (CORA)|CORA]], that $M$ exists due to $f$ being bounded. 

Using this information, we want to show that for some $f(c), c\in[a,b]$ where $f(c)=M$. From here, we can proceed by a contradiction. 

Assume that $f(x) < M$ on $[a,b]$, then define $g(x)=\frac{1}{M-f(x)}$. If $f(x) < M$ on $[a,b]$, then $g(x)$ is continuous *and positive* on $[a,b]$. By the lemma, this is bounded. 

Then, $0<g(x)<K$ where $K$ is some bound on $g(x),x\in AB$. This implies that: 
$$
g(x) = \frac{1}{M-f(x)} \leq K
$$
Rearranging: 
$$
\frac{1}{K}\leq M-f(x)
$$
$$
f(x)\leq M-\frac{1}{K}
$$
Note that this contradicts our concept, that the LUB of $f(x)$ is $M$, but here, f(x)'s LUB is $M-\frac{1}{k}$. Therefore, $f(x)$ must take on it's maximum $M$ somewhere on $[a,b]$. 

---
# Pre-Lecture Notes
## Related Rates
Related rates are an extension of the concept of the [[11 — Trigonometric, Chain and Implicit Differentiation#Chain Rule|Chain Rule]]. For instance, the volume of a sphere is defined as the following: 
$$
V(r) = \frac{4}{3}\pi r^3
$$
If, in some case, we are given some term $\frac{dr}{dt}$'s value; we can solve for a corresponding term of $\frac{dv}{dt}$; 
$$
\begin{align}
\frac{dV}{dt} &= \frac{d\left( \frac{4}{3}\pi r^3 \right)}{dr} \frac{dr}{dt} \\
\frac{dV}{dt}&=4\pi r^2 * \frac{dr}{dt}
\end{align}
$$
Note that terms should only be substituted *after* we have appropriately differentiated some of our terms; for instance if $\frac{dr}{dt}=C$, then this should only be substituted when $\frac{dV}{dr}$ has been differentiated. 
## Maximum and Minimum Values 
We follow the following definitions for the maximum and minimum values of a function. Let $c\in D$ , where $D$ is the domain of some function $f$, then $f(c)$ is the: 
* **absolute maximum** value for $f$ if $f(c)\geq f(x)$ for all $x\in D$
* **absolute minimum** value for $f$ if $f(c) \leq f(x)$ for all $x\in D$
* **local maximum** value for $f$ if $f(c) \geq f(x)$ for all $x$ near $c$
* **local minimum** value for $f$ if $f(c)\leq f(x)$ for $x$ near $c$
Note that the definition for $x$ near $c$ is that it is true for some open interval $S\in D$ where $c\in S$. 

### Extreme Value Theorem 
The extreme value theorem is the following

> Extreme Value Theorem 
> > *Given:* $f$ is defined and continuous on $[a,b]$
> 
> Prove: $f$ assumes a maximum *and* minimum value on $[a,b]$. 

For us to prove this; we need to apply another theorem called the Boundness Theorem. 
#### Boundness Theorem 
The Boundness Theorem lets us show that, for any function defined and continuous on a closed interval $[a,b]$, it is bounded within that interval. 

> > *Given:* 
> > $f$ is a function defined and continuous on the interval $[a,b]$
> 
> Prove: $f$ is bounded on $[a,b]$.
> 
> Proof: 
> We can perform this proof by a contradiction. 
> > Assume that $f$ is not bounded on $[a,b]$. 
> 
> Let $c$ be the midpoint of $[a,b]$, if $f(x)$ is unbounded on $[a,b]$, then it is unbounded on either $[a,c]$ or $[c,b]$. Define now that $[a_{1},b_{1}]$ to be the half in which $f(x)$ is unbounded; if $f(x)$ is unbounded in both, take the left half. 
> 
> Progressively subdividing this gives us a set of $A$, defined by the left-most endpoints. From [[02 — The Real Number System#Completeness of the Reals Axiom (CORA)|Completeness of the Reals Axiom]] this set has some LUB $\gamma$; where $\gamma\in[a,b]$; then $f(\gamma)$ is continuous. Note that the length of a subinterval is some value $\frac{b-a}{2^n}$ for some bound $[a_{n},b_{n}]$. 
> 
> Then; using the concept of being continuous, we can choose an $\epsilon=1$ with [[06 — Precise Limit Definition#Epsilon-Delta Definition|Epsilon Delta]] (primarily [[06 — Precise Limit Definition#One-Handed Limits|One Handed Limits]])
> * $\gamma=a$, then approaching this from the right, then: 
>   $\exists\delta>0$ in $[a,a+\delta)\implies|f(x)-f(\gamma)|<\epsilon=1\implies |f(x)|<1+|f(\gamma)|$
> * $\gamma=b$, then approaching this from the left, then: 
>   $\exists\delta>0$ in $(b-\delta,b] \implies |f(x)-f(\gamma)|<\epsilon \implies |f(x)|<1+|f(\gamma)|$
> * $a<\gamma<b$, then our interval is $(a-\delta,a+\delta)$. 
> In either case, $f(x)$ is bounded on $[a,b]$ by some $1+|f(\gamma)|$.
> Note that with some $[a_{n},b_{n}]$, it will lie in one of the cases above.

### Extreme Value Theorem (Proof) 
