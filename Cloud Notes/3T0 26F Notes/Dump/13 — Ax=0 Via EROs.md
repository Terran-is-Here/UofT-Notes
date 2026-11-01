---
updated_at: 2026-11-01T15:55:24.891-05:00
edited_seconds: 160
course: ESC103H1
tags:
  - ESC103H1
"Lecture #": 13
Lecture Date: 2026-11-02
Week:
---
Hub: [[ESC103 Hub]]
Previous: [[12 — Elementary Row Operations]]
Next: [[14 — Gaussian Elimination]]

--- 
# Lecture Notes

---
# Pre-Lecture Notes

## Forward Elimination
Forward Elimination *refers* to **the series** of elementary row matrices $E_{u}=E_{i}E_{i-1}\dots E_{1}$ multiplied to turn a matrix $A$ into an upper-triangular matrix $U$, that is $E_{u}A=U$; Recall that an upper triangular matrix refers to where all the entries **below** the diagonal entries equals zero. 

Note that with $A\vec{x}=0$, we know that for any matrix $E_{u}$, or even $M$, that $M 0 = 0$; thus $A\vec{x}=0$'s solution set for $\vec{x}$ is equivalent to $U\vec{x}=0$. Note that the position we multiply things with respect to matters; though at this point you should have enough ERO practice in order to perform this seamlessly. 

## Backwards Substitution
After obtaining some upper-triangular matrix $U$, we can perform *backwards substitution* in order to obtain some $R_{0}$ (otherwise known as the Row-Reduced Echelon Form) of $A$. A matrix in RREF requires the following characteristics: 
1. The first non-zero entry in each row **must** be one. 
2. Each leading one **must** be to the right of all leading ones above it. 
3. All other entries in the same column as a leading one must be 0. 

To get a matrix $U\to R_{0}$, we perform another set of EROs; note that we often term the leading terms the "pivot points", and the non-leading terms as potential free variables. The number of leading pivot points represents the number of linearly independent vectors within the space (and by extension, the corresponding nullity from the rank-nullity theorem).


