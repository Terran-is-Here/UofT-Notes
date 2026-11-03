---
updated_at: 2026-11-03T08:42:26.173-05:00
edited_seconds: 250
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 15
Lecture Date: 2026-11-03
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[14 — Gaussian Elimination]]
Next: N/A

--- 
# Lecture Notes

---
# Pre-Lecture Notes
## Gaussian Elimination Solutions
When Considering the potential cases in Gaussian Elimination, we generally have *three* sets of possibilities pertaining to the resulting solution. 
1. If all columns are defined by a leading one (that is, there exists no free variables / $A$ is linearly independent), then we say that a *unique, consistent* solution exists. 
2. If free variables are present (that is, there exists columns not defined by a leading one), then we say that a *consistent, but infinite* number of solutions exist. 
3. If an inconsistent solution arises (e.g. $0=1$ in one of our rows), then we state that this is inconsistent, and that no solution exists.
	1. Geometrically, this means that for some $A\vec{x}=\vec{b}$ where this is the case, $\vec{b}\not\in A$'s column space. 

Consider that we can also extend this to our previously defined concept of $\text{rank}(A)$. Recall that $A$ represents some $m\times n$ matrix, then: 
* $\text{rank}(A) =m$, then our system is fully consistent, as this states that for any vector in $\mathbb{R}^{m}$, some linear combination of our corresponding column vectors present in our matrix where this resolves to $\vec{b}$ in $\mathbb{R}^{m}$. 
* $\text{rank}(A)<m$, then our system may not be fully consistent, some $\vec{b}$ may not be in the column space of $A$. 
* $\text{rank}(A)=n$, then our system is fully composed of pivot variables (that is, full linear independence), thus **one unique solution exists**. 
* $\text{rank}(A)<n$, then our system may have one or more free variables, then multiple solutions may concurrently exist (i.e. non-existence of unique solution). 

### Rank-Nullity
Consider that for a matrix $A$ of some size $m\times n$, we can see that for some given rank, this corresponds to the number of linearly independent vectors present in $A$, and thus the corresponding amount of pivot variables; that is $\text{rank}(A)=r$. For this system then, the corresponding number of free variables is given to us by the expression of $n-r$; and we note this corresponds to the nullity of a system; thus: 
$$
\begin{align}
r + n - r  & = n  \\
\text{rank}(A)+\text{nullity}(A) & =n
\end{align}
$$
Which is what we define as the Rank-Nullity Theorem as Desired.)