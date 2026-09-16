---
updated_at: 2026-09-16T13:44:58.273-04:00
edited_seconds: 200
course: ESC194H1
tags:
  - ESC194H1
"Lecture #": 6
Lecture Date: 2026-09-21
Week: 3
created:
Created: September 14th 2026, 9:42:17 pm
---
Hub: [[ESC194 Hub]]
Previous: [[05 — The Limit of a Function]]
Next: N/A

--- 

# Lecture Notes
# Pre-Lecture Notes
## Epsilon-Delta Definition
The Epsilon-Delta Definition of a limit is the formal definition of a limit past the intuitive one we tackled in the previous note. It is formally defined as the following: 
$$\lim_{ x \to c }f(x)=L \iff \forall \epsilon>0, \exists\delta >0 \text{ s.t. }$$
$$|f(x)-L|<\epsilon$$
> Note that the above line can be rewritten as:
> $$-\epsilon+L < f(x) < \epsilon + L$$


$$0<|x-c|<\delta$$
Note that our first inequality gives us our equivalent $y$-tolerance, and our second inequality gives us our equivalent $x$-compliance. The main goal of using Epsilon Delta is found within the first line: 
$$
\forall\epsilon >0,\exists\delta > 0
$$
That is, for all $\epsilon$ greater than 0, there must exist a $\delta$ greater than 0. We need to find a consistent definition for $\delta$ with respects to $\epsilon$ 