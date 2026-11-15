---
updated_at: 2026-11-15T18:29:15.727-05:00
edited_seconds: 190
course:
tags:
"Lecture #": 0
Lecture Date: 2026-11-15
Week:
---
Hub: [[ESC194 Hub]]
Previous: [[27 —  The Natural Exponential]]
Next: N/A

> [!quote] Recommended Reading 
> Section 6.4\* of the Stewart Textbook. 
--- 
# Lecture Notes

---
# Pre-Lecture Notes
## General Exponentials and Logarithms
Recall that we defined the following as our cancellation expressions pertaining to the concept of natural logarithms and their corresponding exponential equivalents: 
$$
\begin{align}
\ln(e^{x}) = x \\
e^{\ln(x)} = x
\end{align}
$$
Thus, we find that: 
$$
b^{r} = e^{r\ln(b)} = e^{\ln(b^{r})}
$$
From here, we derive the definition of the general Exponential: 
> [!theorem] General Exponential
> We let the following be the notation that we shall use for the definition of a General Exponential as the following: 
> $$b^{r} = e^{r\ln(b)}$$

Consider now that this allows us to extend some of the exponent laws that we derived earlier. 

> Property 1
> $$b^{x+y}=b^{x}b^{y}$$
> > Proof 
> > Consider that with our definition, we find that: $$b^{x+y} = e^{(x+y)\ln(b)} = e^{x\ln(b) + y\ln(b)} = e^{\ln(b^{x}) + \ln(b^{y})} = e^{\ln(b^{x}b^{y})} = b^{x}b^{y}$$

> Property 2 
> $$b^{x-y} = br$$
