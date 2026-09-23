---
updated_at: 2026-09-23T16:04:42.070-04:00
edited_seconds: 250
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
Next:

> [!quote] Recommended Reading 
> 1.6
--- 

# Lecture Notes
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

Note that from here, exponentiation and fractional powers will also follow along. 
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
$$

$$

