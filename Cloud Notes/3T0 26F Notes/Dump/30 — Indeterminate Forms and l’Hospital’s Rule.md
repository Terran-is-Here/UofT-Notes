---
updated_at: 2026-11-20T11:31:20.237-05:00
edited_seconds: 220
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-20
Week:
---
Hub: 
Previous: 
Next:
> [!quote] Recommended Reading 
> Section 6.8 of the Stewart Textbook
> [[13 — Mean Value Theorem, Linear Approximations and Differentials#Cauchy's Mean Value Theorem]] (as we use it for the proof of l\`Hospital's rule). 

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Indeterminate Forms
Consider the case in which we have a function such as the following: 
$$
f(x)=\frac{\ln(x)}{x-1}
$$
Where we want to find the following: 
$$
\lim_{ x \to 1 } f(x) = \lim_{ x \to 1 }  \frac{\ln(x)}{x-1} \to \frac{0}{0}
$$
We have an issue: If we wanted to find the value of such a function, where taking the limit results in something that we term as an *indeterminate* form. We now define the following as indeterminate forms *which we can analyze*. 
* $\frac{0}{0}$
* $\frac{\infty}{\infty}$
In terms of the means we analyze this, we now introduce the concept of l\`Hospital's Rule: 
### l\`Hospital's Rule 
l\`Hospital's Rule (noted from here as LHoR) is defined as the following: 

> [!theorem] LHoR
> Let $f,g$ be differentiable and $g'(x) \neq 0$ on an open interval $I$ that contains $a$ (except possibly at $a$), Suppose that: 
> $$\lim_{ x \to a } f(x) = 0, \lim_{ x \to a } g(x) = 0\text{ or }\\ \lim_{ x \to a } f(x) = \infty, \lim_{ x \to a } g(x) = \infty$$
> Or in other words, we have the following expression that evaluates into an indeterminate form as the ones that we have had above. 
> $$\lim_{ x \to a } \frac{f(x)}{g(x)} \to\frac{0}{0} \lor \lim_{ x \to a } \frac{f(x)}{g(x)} \to \frac{\infty}{\infty}$$
> Then we define that:
> $$\lim_{ x \to a } \frac{f(x)}{g(x)} = \lim_{ x \to a } \frac{f'(x)}{g'(x)}$$
> If the limit on the right side exists. 

In other words, it states that given a ratio of functions which, when the limit is taken, that they fall into an indeterminate form of $\frac{\infty}{\infty}$ or $\frac{0}{0}$, 
### Proof 
We can prove this by reconsidering the Mean Value Theorem from earlier. For the purpose of completeness, we will prove the necessary theorems that we need to prove that this rule holds true. 

Recall the 