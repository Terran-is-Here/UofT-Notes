---
updated_at: 2026-09-28T11:58:03.021-04:00
edited_seconds: 1700
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
From this, we show that from all these cases, that $f(x)$ is continuous for our entire interval $x\in (-\infty,-2]\cup[2,\infty)$ 
## Continuity Rules 
We have the following theorems that can help for simplifying these rules: 

> [!theorem] Theorem
> Let $f(x),g(x)$ be continuous at $x=c$, and $x$ is a constant, then the following are also continuous at $c$: 
> * $f(x) \pm g(x)$
> * $af(x) \lor ag(x)$
> * $f(x)g(x)$
> * $\frac{f(x)}{g(x)}$ (if $g(c)\neq 0$)

For instance, the product rule: 
*Proof:* If $f,g$ continuous at $x=c$, their product will also be continuous at $c$
$$
\begin{align}
&f(x),g(x)\text{ are continuous at }x=c \\
&\implies \lim_{ x \to c } f(x) = f(c) &\lim_{ x \to c } g(x)=g(c) \\
&\implies \lim_{ x \to c } f(x)g(x) = \lim_{ x \to c } f(x) * \lim_{ x \to c } g(x) & \text{From the Product Law of Limits}\\
&= f(c)g(c)
\end{align}
$$

*Corollary:* Consider this extended to some interval, that is $f,g,$ are continuous on an interval. 

This can be extended to an interesting result: 
* Any Polynomial Function is *Continuous* on $\mathbb{R}$. 
  Recall the definition of a polynomial: 
  $$\begin{align}f(x) &= a_{1}x^n + a_{2}x^{n-1} + \dots + a_{n} & \text{Where } n \text{ is an integer} \\\lim_{ x \to a } f(x) &= \lim_{ x \to a } \left[a_{1}x^n + a_{2}x^{n-1} + \dots + a_{n}\right] \\&=\lim_{ x \to a } a_{1}x^n + \lim_{ x \to a }a_{2}x^{n-1} +\dots+\lim_{ x \to a } a_{n}  \\&=a_{1}\lim_{ x \to a } x^n + a_{2}\lim_{ x \to a } x^{n-1} +\dots + a_{n} & \text{via Constant Multiplication Rule}\\f(x)&=a_{1}a^n + a_{2}a^{n-1} +\dots + a_{n}  & \text{via Exponentiation Rule}\\&\therefore\text{ Any polynomial is continuous for any arbitrary  }a\end{align}$$
* Any *Rational* Function is Continuous on it's domain, that is: 
$$\begin{align}
f(x) = \frac{P(x)}{Q(x)} && \text{Where } f(x), x\in \{ x\in \mathbb{R}|Q(x) \neq 0 \}
\end{align}$$
We can prove this statement, recall that $P(x)$ and $Q(x)$ are continuous over an interval (from our first point above) , and from our previous theorem, that $\frac{P(x)}{Q(x)}$ is continuous over it's interval on regions where our denominator is not equal to 0, as these are the ratio of two continuous functions.
  
## Function Composition
> [!theorem] 
> If $f$ is continuous at some point $b$, and $\lim_{ x \to c }g(x)=b$, then: 
> $$\lim_{ x \to c } f(g(x)) =f(\lim_{ x \to c } g(x)) = f(b)$$

This can be extended: 
> [!theorem]
> If $g$ is continuous at $x=c$, and $f(x)$ is continuous at $g(x)$, then: 
> $$f\circ g(x) = f(g(x))$$
> Where this is continuous at $x=c$. 
### Example
Consider: 
$$
f(x) = \frac{1}{\cos^2(x)+1}
$$
Note that $f(x) = f_{1}\circ f_{2} \circ f_{3}$, where: 
* $f_{1} = \frac{1}{x}$
* $f_{2} = x^2 +1$
* $f_{3} \cos(x)$
Note that $f_{1},f_{2},f_{3}$ are continuous over it's entire domain (except for $f_{1}$ at $x=0$ as per our above theorem); then: 
$$
D = \{ x \in \mathbb{R} | \cos^2(x) + 1 \neq 0 \}
$$
Note that $\nexists\cos^2(x) < 0$, then this implies that $D=\{ x \in \mathbb{R} \}$. 

Consider a case when our function is composed of functions with discontinuities: 
![[08 — Continuity-1790610668792.webp|284]]
Let us try checking if a function of $h(x)=f(f(x))is$ continuous at some value $x=0$. Let's first evaluate it at $f(0)$: 
$$
h(0) = f(f(0)) = f(2) = 2
$$
Now, consider it's limits from left and right of $x=0$: 
$$
\begin{align}
\lim_{ x \to 0^+ }h(x)  &= \lim_{ x \to 0^+ } f(f(x)) & \text{ Consider approaching from the right, then} \lim_{ x \to 0^+ } f(x) = 2 \\
&= f(2) = 2 \\
\lim_{ x \to 0^- }h(x)  &= \lim_{ x \to 0^- } f(f(x)) & \text{ Consider approaching from the left, then} \lim_{ x \to 0^- } f(x) = 2 \\
&= f(2) = 2 \\ 
\lim_{ x \to 0^+ }h(x) = \lim_{ x \to 0^- } h(x) = 2 &= h(x) & \text{Therefore, our function is continuous at }x=0.
\end{align}
$$


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



