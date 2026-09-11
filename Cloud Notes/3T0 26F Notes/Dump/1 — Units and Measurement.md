---
updated_at: 2026-09-11T16:59:26.312-04:00
edited_seconds: 1280
course: PHY180H1
tags:
  - PHY180H1
"Lecture #": 0
Date': 2026-09-10
custom-width: 30
---
Hub: [[PHY180 Hub]]
Previous: N/A
Next: [[2 — Vectors (Physics)]]

--- 
> [!Quote] Textbook Chapters Discussed
> Chapters 1.1 to 1.7 
> (p5 - p33)

> [!note]
> These sections have been written in the order of their respective chapters. The summary is located at the bottom. 


### Overview of Physics   
Physics (the field) deals with describing the interactions of energy, matter, space, and time to uncover the mechanisms behind every phenomenon. Physics deals with scales as small as a particle; to galaxies. In general; physics governs everything in the observable universe at all measurable scales of length. 
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
	1. These functions also return pure numbers as outputs; i.e. Dimensionless IN - Dimensionless OUT 
### Significant Figures and Precision

Recall from our previous classes on the difference between Accuracy and Precision: 
* Accuracy is the relative difference between measurements; the average difference between measurements is termed as their **uncertainty**
* Precision is the relative difference a measurement and the accepted value; where this difference is denoted as their **discrepancy**. 

Generally: 
* Leading zeros do not count as S.Fs. 
* Enclosed Zeros do count as SFs. 
* Trailing Zeros do not *normally* count as SFs.
	* With a decimal point; Trailing Zeros DO count. 

## Standard Deviation 
Repeated measurements normally *do not* return the same number over and over again. This is a naturally present effect within experimental science. **Distributions** of numbers within a cluster give a rough idea of the true factual number being searched for. 

Distributions are meant to be described; and our goal in labs are to reduce uncertainties (if possible). 

* Uncertainty is around half of the trailing digit (if no other options are available for uncertainty)

A distribution can be generally defined by the Gaussian Distribution: 
$$Ae^{\frac{-(x-\bar{x})^2}{2\rho}}$$
Where $\bar{x}$ is the mean, and $\rho$ is the standard deviation.

The mean can be found by: 
$$
\bar{x}=\frac{1}{N}\sum^n_{{i=1}} x_{i}
$$
While the standard deviation can be found by: 
$$
\sigma = \sqrt{ \frac{1}{N-1}\sum^n_{i=1}\left(x_{i}-\bar{x}_{est}\right)^2 }
$$
Note that $N-1$ is defined by the degrees of freedom; we lose a degree of freedom when we use the data set to actually calculate the mean. If we know the mean independently; this is divided by solely N instead. 

$\sigma$ is equivalent to the uncertainty present in every instance of data within this dataset! 

## Uncertainty Propagations 
These rules are already written within another document; but are left here. For the purposes of this section, let $x,y$ be equal to independent measurements. 

> [!axiom] Addition/Subtraction
> $$z = x+y \lor z=x-y$$
> With this, uncertainty of $z$ is defined by: 
> $$u_{z} = \sqrt{ u_{x}^2 + u_{y}^2  }$$
> We linearly add our uncertainties. 

> [!axiom] Multiplication / Division
> $$z=xy \lor z=\frac{x}{y}$$
> In general, you add the *fractional* uncertainties of our units. 
> $$\frac{u_{z}}{z} = \sqrt{\left(\frac{u_{x}}{x}\right) + \left(\frac{u_{y}}{y}\right) }$$
> Note that for constants; that is their uncertainty is 0; you can directly multiply the uncertainty by this constant (normally for unit conversions)

> [!axiom] Power
> $$z = x^n$$
> $$\frac{u_{z}}{z} = n* \frac{u_{x}}{x}$$
> Or that is; you multiply the fractional uncertainty of the term being exponentiated by the degree of the exponent. 

In terms of uncertainty of the *mean* with the same uncertainty (that is, it is always represented by the same $u_{x}$): 
$$\bar{x} = \frac{\sum^n_{i=1}x_{1}}{N} = \frac{x_{sum}}{N} = \frac{1}{N} * x_{sum}$$

In general, you can describe the uncertainty of the sum as: 
$$u_{sum} = \sqrt{ \sum^N_{i=1} u_{xi}^2  } = \sqrt{ Nu_{x}^2 } = \sqrt{ N } * u_{x}$$ 
And the mean can be appropriately scaled as dividing the above equation by $\frac{1}{N}$ as defined by our multiplication rules. 
### Significant Figure Rules 
For this course: 
1. No rounding before the final answer. 
2. Uncertainties should be rounded to 1 (or at most 2) significant figures. 
3. The most precise uncertainty column should be the most precise column for the value 
	1. e.g. uncertainty specified to 1/100ths, value should also be specified to 1/100ths appropriately. 
	2. These can also be rounded to 1sf; though normally uncertainties are rounded to 2sfs. 