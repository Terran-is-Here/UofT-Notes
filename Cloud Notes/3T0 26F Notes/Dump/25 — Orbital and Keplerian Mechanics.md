---
updated_at: 2026-10-27T14:20:19.289-04:00
edited_seconds: 190
course:
tags:
"Lecture #": 0
Lecture Date: 2026-10-27
Week:
---
Hub: [[PHY180 Hub]]
Previous: [[24 — Gravitation]]
Next: N/A
> [!quote] Recommended Reading 
> Sections 13.4, 13.5 of University Physics


--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Circular Orbits
Consider now the concept of a perfectly circular object. Recall that for a circular body, a centripetal force is applied onto it as it's net force: 
$$
F_{c}=ma_{c}=\frac{mv^{2}}{r}
$$
Consider now that if an object is orbiting a planetary body, this force is solely provided by $F_{g}$, that is the force of gravity. Taking Newton's Law of Universal Gravitation, we find that: 
$$
\frac{GMm}{r^{2}} = \frac{mv^{2}}{r}
$$
Where $v$ represents the orbital velocity. Note that $m$ cancels out in this expression, and thus we can solve for $v$: 
$$
\begin{align}
\frac{GMm}{r^{2}} & =\frac{mv^{2}}{r} \\
\frac{GM}{r} & =v^{2} \\
v & =\sqrt{ \frac{GM}{r} }
\end{align}
$$
Recall that $v=\omega r$, as this is a rotating body, and recall that $\omega$ can be resolved as some $\frac{d\theta}{dt}$, or in terms of revolutions per second, $\frac{2\pi}{T}$, where $T$ represents the period, substituting this in, then: 
$$
\begin{align}
r\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r} } \\
\frac{2\pi}{T} & =\sqrt{ \frac{GM}{r^{3}} } \\
T  & = 2\pi \sqrt{ \frac{r^{3}}{GM} }
\end{align}
$$
Where $T$ represents the rotational period of our body. or in other words: how long it takes to orbit. 