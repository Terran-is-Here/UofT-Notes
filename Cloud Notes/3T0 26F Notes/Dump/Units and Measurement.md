---
updated_at: 2026-09-06T18:55:35.440-04:00
edited_seconds: 560
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 0
Date': 2026-09-10
---
Previous: N/A
Next: N/A

--- 
> [!Quote] Textbook Chapters Discussed
> Chapters 1.1 to 1.7 
> (p5 - p33)

> [!note]
> These sections have been written in the order of their respective chapters. The summary is located at the bottom. 

### Order of Magnitude
Source: pg. 8 (1.1)
> Let $x$ be a measured value; then it's corresponding Order of Magnitude is defined by the equation below. 
> $$\text{OoM} = \text{round}\left(\log_{10}(x)\right)$$
> Where the corresponding logarithmic equation within is rounded to the nearest whole integer. 


This can also be simplified by noting that $\sqrt{ 10 } = 10^{0.5}$. Since $\sqrt{ 10 } \approx {3}$. We can quickly estimate the OoM of a value in Scientific Notation by comparing it's corresponding Mantissa: 

> Let $x$ be a measured value in scientific notation; notated as $M*10^n$; then the OoM of $x$ is defined by the following comparison. 
> 
> If $M > \sqrt{ 10 }$ or $M > 3$; $x$'s OoM is defined as $1 + n$. 
> If $M <  \sqrt{ 10 }$ or $M < 3$; $x$'s OoM is defined as $n$. 


[[Units and Measuremen|asd]]
### The SI Unit System
Source: [[university-physics-volume-1_-_WEB.pdf#page=25|university-physics-volume-1_-_WEB, p.25]]

The SI (Système Internationale d'Unités) System (otherwise known as the Metric System) is the predominant unit system used within engineering and physics. The SI system primarily has 7 **Base Units**; from which **Derived Units** well, derive their dimensions from: 

> [!info] The SI Base Units
> Length (m)
> Mass (kg)
> Time (s)
> Electrical Current (A)
> Thermodynamic Temperature (K)
> Amount of Substance (mol)
> Luminous Intensity (cd)


#### Time (s)
The SI dimension of Time is currently defined by the application of an atomic clock. Specifically; 1 *second* is defined as the time required for 9,192,631,770 vibrations to occur within a Cesium atom. 

#### Distance (m)
The SI dimension of Distance is currently defined as the distance light travels within $1/{299792458}$s (due to the speed of light being $299,792,458 \frac ms$), defined in 1983.

This is an improvement over the following past definitions: 
* 1/10,000,000 of the distance from the Equator to the North Pole (1791) 
* A literal meter stick of metal being used to define the Meter (1889) 
* 1,650,763.73 wavelengths of orange light emitted by Krypton atoms (1960) 

#### Mass (kg) 
The SI dimension of Mass is currently defined by a Kibble balance. No idea what that is yet; but yeah. 


### Dimensional Analysis 
Source: [[university-physics-volume-1_-_WEB.pdf#page=32|university-physics-volume-1_-_WEB, p.32]]

The units mentioned above in the SI base system are linked to the concept of a Physical Dimension: 
* $L$ = Length
* $M$ = Mass
* $T$ = Time
* $I$ = Current
* $\Theta$ = Thermodynamic Temperature (K) 
* $N$ = Substance amount
* $J$ = Luminous Intensity
Given some measurement defined by $x$; we often notate it's dimensions as $[x] = LT\dots$ etc. A pure number is defined as a term/value where it lacks any dimensions (or in other words; has a dimension of $1$.) 

The importance of physical Dimensions within an equation gives arise to the concept of Dimensional Analysis and Dimensional Consistency. For an equation to make physical sense (i.e. being Dimensionally Consistent); it must follow the following rules: 
1. All terms in an expression must have the same dimensions in their corresponding operations. You cannot add a term with the dimensions of $LT$ with the dimensions of $L\Theta$. 
	1. Conversely; this is extended to both sides of the equality needing to resolve to the same dimensions. 
2. Any arguments in standard mathematical expressions (the Trigonometric expressions; exponentials ($b^x$); and logarithms) must be pure numbers. 
	1. These functions also return pure numbers as outputs. 