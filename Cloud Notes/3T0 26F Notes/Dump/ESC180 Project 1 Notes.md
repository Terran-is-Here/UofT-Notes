---
updated_at: 2026-09-28T19:56:50.225-04:00
edited_seconds: 320
course:
tags:
"Lecture #": 0
Lecture Date: 2026-09-28
Week:
---
Hub: [[ESC180 Hub]]
Previous:  N/A 
Next: N/A 

--- 
# Project Notes
> [!quote] Recommended Reading 
> Refer to the actual project document. 

## Initial Battery Parameters: 
* Good Health
* 50% Charge
	* $C$
* 20C Temperature
	* $T$

The battery is always charging, used, or is idle. 
### Notation
For the sake of this note, assume that $C_{0},T_{0}$ is pertaining to the original value of these parameters before being updated. 

## Charging Rules
Note that if fast charging is possible, it WILL occur. States can change between these in the same session. 
### Fast Charging 
* Increases charge by 3%/minute
	* $C_{t} = C_{0}+3t$
* Increases temperature by 0.5C/m
	* $T_{t} = T_{0} + 0.5t$
* Occurs when: 
	* $T\in[0,40]$
	* Good Health 
	* $C_{0} > 80\%$
### Slow Charging
* Increases charge by 1%/minute 
	* $C_{t} = C_{0} + t$
* Increases temperature by 0.25C/
	* $T_{t} = T_{0} + 0.25t$
* Occurs when: 
	* Not Fast Charging 

## Usage 
* Discharges the battery by 2/minute
	* $C_{t} = C_{0}-2t$
* Increases temperature by 1C/m
	* $T = T_{0} + t$
## Idle 
* Discharges the battery by 0.5/minute 
	* $C_{t} = C_{0}-0.5t$
* *Decreases* temperature by 1c/m
	  $T = T_{0}-t$
## Low Battery
If battery reaches 0% when Idling *or in usage*, decrease temperature by 1C per minute dead. 

# Battery Health 
* Charging *at* or *past* 90% reduces battery health. 
	* If this happens 3 times within $6$ hours, the battery is in a bad health state.
* Batteries in Bad Health state cannot charge past 80%. 
	* If it initially switches to a bad health state, it will not charge past 80% until discharged. 


## Overcharge Logic 
* If battery reaches 100% while charging, temperature will continue to increase by 0.25C / minute; while charge does not exceed past 100%. 
* For Bad Health State:
	* Reaches 80% while charging
	* Switches to bad health state while being at or above 90% 
	* battery charge will not go further. 