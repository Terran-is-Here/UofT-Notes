---
updated_at: 2026-10-18T21:47:54.854-04:00
edited_seconds: 300
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 18
Lecture Date: 2026-10-19
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[17— Optimization, Antiderivatives and Sigma Notation]]
Next:
> [!quote] Recommended Reading 
> Section 4.1 of the Stewart Textbook 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Reimann Sums
We are now tackled with an interesting problem: *how do we find the area under a graph*? An approach that we can take is by using rectangles to approximate the area under a graph; with the height being some term $f(x)$ , and the width being some term $\Delta x$ across some interval. 

![[18 — Areas and Distances-1792374288706.webp]]The question now arises: how *do* we exactly define which side of that rectangle we use? 

We could use either the left side; or the right side of that interval defined by some $(x, x+\Delta x)$, and both would fall under our definition. 

However, note that if we take the limit as $\Delta x \to dx$; we note that the areas of these rectangles *should* converge; that is as we make $\Delta x$, the left endpoint case of our usage of rectangles converge onto the same value that the right endpoint case does. 

From here, we actually derive the concept 