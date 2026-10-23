---
updated_at: 2026-10-23T11:15:28.546-04:00
edited_seconds: 220
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 21
Lecture Date: 2026-11-02
Week: 8
---
Hub: [[ESC194 Hub]]
Previous: [[20 — The Fundamental Theorem of Calculus]]
Next: N/A 
> [!quote] Recommended Reading 
> Sections 4.4, 4.5 of the Stewart Textbook
> [[17— Optimization, Antiderivatives and Sigma Notation]]
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Indefinite Integrals
Recall that the Fundamental Theorem of Calculus only pertains to *definite integrals*, that is, integrals where we're measuring the area within a certain, closed interval $[a,b]$; Retaking it here for reference: 

> The Fundamental Theorem of Calculus
> 1. $g(x) = \int_{a}^{b}f(x)dx,g'(x)=f(x)\implies \frac{d}{dx}\int_{a}^{b}f(x)dx=f(x)$ (Integration and Differentiation are inverse functions) 
> 2. $g(x)=\int_{a}^{b}f(x)=F(b)-F(a), F'(x)=f(x)$ (A discrete integral can be evaluated as the difference of the antiderivatives) 

Recall how we said that for a discrete integral, we can define it as the difference of the two antiderivatives calculated. From here, we can derive the definition of an indefinite integral: 

$$
\int f(x)~dx = F(x)
$$
Where this now describes a *family* of functions; that is some $F(x)+C$ (similar concepts applied from Antidifferentiation). This means that our second theorem can be expressed as: 
$$
\int _{a}^{b}f(x) \, dx  = \left[]\int f(x) \, dx\right]^{b}_{a}
$$