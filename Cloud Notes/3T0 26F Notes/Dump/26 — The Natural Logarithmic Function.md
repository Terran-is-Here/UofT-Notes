---
updated_at: 2026-11-11T13:47:51.117-05:00
edited_seconds: 160
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 26
Lecture Date: 2026-11-13
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[25 — Inverse Functions]]
Next:
> [!quote] Recommended Reading 
> Section 6.2\* of Stewart. 
> Not to be confused with Section 6.2 normally. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## The Natural Logarithmic Function
We define the Natural Logarithmic function as the following expression: 
$$
\ln x = \int_{1}^{x} \frac{1}{x}\,dx
$$
Or in other words, the area under the reciprocal expression $\frac{1}{x}$ from $x\in[1,x]$. Note that this form of integral was discussed within the Fundamental Theorem of Calculus (specifically, [[20 — The Fundamental Theorem of Calculus#^d40ade|FTC1, though both are in this link]], retaking it here): 
$$
\frac{d}{dx}\int_{a}^{x}f(t)\,dt = f(x)
$$
Then we see that: 
$$
\frac{d}{dx}\ln x = \frac{1}{x}
$$
Which is a *very useful expression for evaluating some properties of the natural logarithmic function.* 
### Properties of Ln(x) 
> The textbook actually goes into a series of proofs pertaining to the nature of this function! 

> Prove that $\ln(xy) = \ln(x) + \ln (y)$

To prove this, first consider a function with any positive number $a$ that is some $\ln (ax)$, then taking the derivative of this gives us the following: 

$$
\frac{d}{dx}\ln(ax) = \frac{1}{ax} \frac{d}{dx}(ax) = \frac{1}{ax}a = \frac{1}{x}
$$
We note that $\ln (x)$ and $\ln(ax)$ share the same derivative, thus $\ln(ax)$ must differ by some **constant value**, that is: 
$$
\ln (ax) = \ln(x) + C
$$
Note that if $x=$