---
updated_at: 2026-09-24T13:58:52.524-04:00
edited_seconds: 370
course:
tags:
  - ESC194H1
"Lecture #": 7
Lecture Date: 2026-09-21
Week: 3
created:
Created: September 21st 2026, 10:49:06 am
---
Hub: [[ESC194 Hub]]
Previous: [[06 — Precise Limit Definition]]
Next: [[08 — Continuity]]

> [!quote] Recommended Reading 
> 1.6
--- 

# Lecture Notes
> [!theorem] Theorem - Uniqueness of a Limit 
> $$\begin{align}\text{ if } \lim_{ x \to c } f(x) = L \land \lim_{ x \to c } f(x) = M\\\implies L=M \end{align}$$
> The proof of this can be derived from $\epsilon-\delta$. 


# Pre-Lecture Notes
## Limit Laws
The Limit Laws can be derived from application of the $\epsilon-\delta$ definition of the Limit, though those have been linked in a separate segment. They have been listed here below: 

For the purposes of this section, assume that $c$ is some constant, and that $\lim_{ x \to c }f(x)$ and $\lim_{ x \to c }g(x)$ exist, then: 
> Sum Law & Difference Law: $$\lim_{ x \to c } \left[f(x) + g(x)\right] = \lim_{ x \to c } f(x) + \lim_{ x \to c } g(x) $$
> $$\lim_{ x \to c } \left[f(x) - g(x)\right] = \lim_{ x \to c } f(x) - \lim_{ x \to c } g(x) $$


> Multiplication Laws 
> $$\lim_{ x \to c } Df(x) = D\lim_{ x \to c } f(x)$$
> $$\lim_{ x \to c } f(x)g(x) = \lim_{ x \to c } f(x) \cdot \lim_{ x \to c } g(x)$$

> Division Laws: 
> $$\lim_{ x \to c } \frac{f(x)}{g(x)} = \frac{\lim_{ x \to c } f(x)}{\lim_{ x \to c } g(x)}$$
> That is, assuming $\lim_{ x \to c }g(x) \neq 0$. 

Note that from here, exponentiation and fractional powers will also follow along. Note that two other simple cases arise: 
* $$\lim_{ x \to c } x = c$$
* $$\lim_{ x \to c } b=b$$

### Squeeze Theorem
The squeeze theorem states that, given the functions in the following relation: 
$$
g(x) \leq f(x) \leq h(x) 
$$
And: 
$$
\lim_{ x \to c } g(x) = \lim_{ x \to c } h(x) = L
$$
Then: 
$$
\lim_{ x \to c } f(x) = L
$$
That is, when we let $g(x)$ and $h(x)$ approach $c$, their values constrict $f(x)$ to have a same set of values that they do, eventually granting us the above theorem.

Generally, interpretation and implementation of the Squeeze Theorem requires knowledge of the domains of one of the functions present; recall that given: 
$$
a < b < c
$$
Letting $D>0$, then
$$
Da < Db < Dc
$$
From here, for instance some function $\sin\left( \frac{1}{x} \right)$ can be expressed based off it's domain range, and then restricted from there: 
$$
-1 \leq \sin\left( \frac{1}{x} \right) \leq 1
$$
Let $D = x^2$, note that for all $x$, $D\geq 0$, thus: 
$$
-x^2 \leq x^2\sin\left( \frac{1}{x} \right) \leq x^2
$$
From our squeeze theorem above, $\lim_{ x \to 0 }-x^2 = \lim_{ x \to 0 }x^2 = 0$, implying that $\lim_{ x \to 0 }x^2\sin\left( \frac{1}{x} \right)=0$. 
