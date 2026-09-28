---
updated_at: 2026-09-28T11:29:02.796-04:00
edited_seconds: 1160
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 8
Lecture Date: 2026-09-23
Week: 3
Created: September 23rd 2026, 4:21:26 pm
---
Hub: [[ESC194 Hub]]
Previous: [[07 — Limit Laws]]
Next: [[09 — Derivatives and Rates of Change]]
> [!quote] Recommended Reading 
> 1.8 in the Stewart Textbook, 3.3 of the Supplemental. 
--- 
# Lecture Notes
## Substitution Limits
There are limits in which you can directly substitute a value into a function to evaluate the limit. These normally arise during *rational inequalities* in which a denominator causes a division by 0 when the limit is taken. For instance: 
$$
\begin{align}
\lim_{ x \to 3 } \left(\frac{x^2-x-6}{x-3}\right) &=?&\text{Note that we can't distribute, limit would cause div by 0:}\\
\lim_{ x \to 3 } \left(\frac{x^2-x-6}{x-3}\right) &= \lim_{ n \to 3 } \left(\frac{(x-3)(x+2)}{x-3}\right) & \text{So we factor it: }\\
&=\lim_{ x \to 3 } (x+2)  \\
&= 5\end{align}$$

Another example: 
$$
\lim_{ x \to 5 } \frac{\sqrt{ x+4 }-3}{(x-5)}
$$
At this point, we can't use any of our rules. Let's try rationalizing the numerator by multiplying it by it's conjugate: 
$$
\begin{align}
\lim_{ x \to 5 } \frac{\sqrt{ x+4 }-3}{(x-5)} *\frac{\sqrt{ x+4 }+3}{\sqrt{ x+4 }+3} \\
=\lim_{ x \to 5 } \frac{x+4-9}{(x-5)(\sqrt{ x+4 }+3)} \\
=\lim_{ x \to 5 } \frac{x-5}{(x-5)(\sqrt{ x+4 }+3)} && \text{Cancel out our terms, then} \\
=\lim_{ x \to 5 } \frac{1}{\sqrt{ x+4 }+3} \\
= \frac{1}{6}
\end{align}
$$

Final Example: 
$$
\begin{align}
&f(x) = \begin{cases}
\sqrt{x^2-3}: x>2 \\
5-2x:x<2
\end{cases}\\
\text{find }\lim_{ x \to 2 } &f(x)  \\
\end{align}
$$
In this case, approach via one-sided limits: 
$$
\begin{align}
\lim_{ x \to 2^+ } f(x) = \lim_{ x \to 2^+ }\sqrt{ x^2-3 } = 1 && \lim_{ x \to 2^- }(5-2x) = 1  \\
\lim_{ x \to 2^+ }f(x) &= \lim_{ x \to 2^- } = 1 \implies\lim_{ x \to 2 } f(x) = 1    
\end{align}
$$
## Squeeze Theorem 
Note that this was taken up in a previous note already, that is [[07 — Limit Laws#Squeeze Theorem|in Limit Laws (07) - Squeeze Theorem]]. For purposes of completeness, they will be positioned here again (as they were mentioned in this lecture): 

> [!theorem] Squeeze Theorem
> $$\begin{align}\text{given }f(x),g(x),h(x) \text{ where } \\h(x) \leq f(x) \leq g(x)&&\text{where }\lim_{ x \to c } f(x) = \lim_{ x \to c } g(x) = L\\\implies \lim_{ x \to c } f(x)=L\end{align}$$
> Graphically, this is akin to us "squeezing" our desired though two bounding functions that converge onto the same location, since we can show that the space between these functions equals zero, then our function must converge onto this same value. 

### Example 
Evaluate the following: 
$$
\lim_{ x \to 0 } x^2\cos\left( \frac{1}{x^2} \right) =? 
$$
Note that our cos term is undefined when we evaluate $x\to 0$, therefore we need to consider using the squeeze theorem for this. Take the squeeze theorem: 
$$
\begin{align}
h(x) &\leq f(x) \leq g(x) && \text{Let } f(x) = \cos\left( \frac{1}{x^2} \right) \\
h(x) &\leq \cos\left( \frac{1}{x^2} \right) \leq g(x) && \text{Note that }\cos(\theta) \mapsto[-1,1] \therefore \\
-1 &\leq \cos\left( \frac{1}{x^2} \right) \leq 1 && \text{Multiply by } x^2 \\
-x^2 &\leq x^2\cos\left( \frac{1}{x^2} \right) \leq x^2 && \text{Note that } \lim_{ x \to 0 } x^2 = 0&&\text{Also applies to }\lim_{ x \to 0 } -x^2 = 0 \\
\end{align}
$$

Then, following from the Squeeze Theorem, then: 
$$\lim_{ x \to 0 } x^2\cos\left( \frac{1}{x^2} \right) = 0$$
## Continuity & Applications
The definition of Continuity below in Pre-Lecture segment of this note ([[08 — Continuity#Continuity|08 — Continuity\Continuity]]) still holds. Note that the implications that this gives: 
1. Our function is defined at $f(c)$, i.e. $f(x) \mapsto y$ then $c\in x$.
2. That the limit $\lim_{ x \to c }f(x)$ exists; which implies that $f(x)$ must be defined on some open interval *containing* $c$. 
	1. The above two statements basically state that $c$ is in $x$, and that $f(x)$ must be defined on an interval containing $c$. 
3. $\lim_{ x \to c }f(x) = f(c)$
	1. This mainly deals with the concept of holes/jump discontinuities present. 
### Continuity Types
There are generally 4 Continuity Types: 
> [!theorem] Infinite Discontinuity
> Given a function $f(x)$, we say that it has a infinite discontinuity at $x=a$ if the limit at that point does not inherently exist. 

> [!theorem] Removable Discontinuity
> Given a function $f(x)$, we say that it has a removable discontinuity if:
> * at $x=a$, $f(a)=B$ .
> * However, $\lim_{ x \to a }f(x)=L$, where $L$ is some finite value. 
> * And, $B \neq L \implies f(a) \neq \lim_{ x \to a }f(x)$
> 
> Or, in shorthand: 
> $$\begin{align}f(x=a) &= B \\\lim_{ x \to a } f(x) &= L \\L \neq B \implies f(a) &\neq \lim_{ x \to a }f(x) \end{align}$$

> [!theorem] Jump Discontinuity
> Given a function $f(x)$, we say it has a jump discontinuity at $a$ if: 
> * $\lim_{ x \to a^+ }f(x) \neq \lim_{ x \to a^- }f(x) \implies \nexists\lim_{ x \to a }f(x)$

> [!theorem] Other Discontinuities
> Other discontinuities exist; for instance take the Dirichlet Function, defined as: 
> $$f(x) = \begin{cases}1: x\text{ is rational}\\0: x\text{ is irrational}\end{cases}$$
> Note that this function is discontinuous, as this has an infinite number of jump discontinuities between rational and irrational values present. 
### Monodirectional Continuities
That is, right-handed and or left-handed continuities. These are essentially sub-definitions of our earlier limit-based continuity expressions (see [[08 — Continuity#Continuity|the section in the pre-lecture about it]])

> Right-Handed Continuity
> We state that a function is continuous from the right at some value $x=c$ if $\lim_{ x \to c^+ }f(x) = f(c)$

> Left-Handed Continuity
> We state that a function is continuous from the right at some value $x=c$ if $\lim_{ x \to c^- }f(x) = f(c)$

## Interval Continuity
We say that a function is continuous on an interval if it is continuous on every point *on* that interval. Note that at the end-points of the interval, we define their concept of "continuous" as the corresponding monodirectional continuity as appropriate. 

*Example*: Show that $f(x) = \sqrt{ x^2-4 }$ is continuous on the domain of $(-\infty,-2]\cup[2,\infty)$. For this, we will consider this in terms of cases. 

Consider the case when $c>2 \lor c<-2$ is defined as: 
$$
\begin{align}
\lim_{ x \to c } \sqrt{ x^2-4 } = \sqrt{ \lim_{ x \to c } x^2-4 } = \sqrt{ c^2-4 } && \text{Note, }\sqrt{ c^2-4 } = f(c) \\
\therefore, \text{f(x) is continous if } x<-2\lor x>2 
\end{align}
$$
Consider now the case at our endpoints that are defined at $c=2$ and $c=-2$: 
$$
\begin{align}
x=-2 \implies c&=-2 \\
\lim_{ x \to -2^- } \sqrt{ x^2-4 } = \sqrt{ \lim_{ x \to -2^- }x^2-4 }  = \sqrt{ (-2)^2-4 } &= 0 = f(-2) \\
\therefore f(x)\text{ is continuous at -2 (from the left)}
\end{align}
$$
$$
\begin{align}
x=2 \implies c&=2 \\
\lim_{ x \to 2^+ } \sqrt{ x^2-4 } = \sqrt{ \lim_{ x \to -2^+ }x^2-4 }  = \sqrt{ (2)^2-4 } &= 0 = f(2) \\
\therefore f(x)\text{ is continuous at 2 (from the right)}
\end{align}
$$
From this, we show that from all these cases, that $f(x)$ is continuous for our entire interval $x\in$


# Pre-Lecture Notes
## Continuity 
The concept of continuity can be generally defined as the idea of "not lifting your hand from the page". Mathematically however, this is defined as the following: 

> [!theorem] Continuity
> A function $f(x)$ is continuous at $x=c$ if and only if: $$\lim_{ x \to c } f(x) = f(c)$$

That is, a function is both defined at it's limit, and that it's limit converges onto this point. In terms of Epsilon Delta: 
$$\forall\delta, \exists\epsilon >0 \text{ s.t. } |x-c| < \delta \implies |f(x) - f(c)| < \epsilon$$
This has some interesting properties. Given two continuous functions $f$ and $g$: 
* $f+g$ will result in some continuous function. 
* $fg$ will result in some continuous function. 
* $\frac{f(x)}{g(x)}$ will be continuous in all of it's domain with the exception of $g(x) = 0$. 

### Polynomials
Note that Polynomials are continuous in all of it's domain, that is $x\in \mathbb{R}$ for any polynomial. This arises from our [[07 — Limit Laws|Limit Laws]]: 
Given the following polynomial: 
$$
f(x) = c_{1}x^n + c_{2}x^{n-1} + \dots + c_{n}x^0
$$
Taking the limit of this for some arbitrary value $a \in x$, then: 
$$
\lim_{ x \to a } f(x) = \lim_{ x \to a } c_{1}x^n + c_{2}x^{n-1} + \dots + c_{n}x^0
$$
Recall that: 
$$
\lim_{ x \to a } c_{1} = c_{1}
$$
And 
$$
\lim_{  x \to a } x^n = a^n \iff n\in \mathbb{N}
$$
Since both of these are continuous, and that a polynomial is the sum of these polynomial functions, then it arises that any polynomial is continuous along it's entire domain. 

> [!theorem] Rational Functions
> From this, it also extends to the concept that rational functions are continuous everywhere in it's domain *with the exception of places in which the denominator resolves to a value of 0.*



