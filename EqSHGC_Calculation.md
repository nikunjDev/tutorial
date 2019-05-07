# SEF and Eq. SHGC Calculator

## Step1:

### Prerequisite
* Is WWR <40%? [Y/N]
* Is VLT >0.27? [Y/N]

If No Display "Prescriptive Trade-Off approach is not applicable"
	
## Step2:
**Input**
* Compliance Level [ECBC / ECBC+ / SuperECBC]
* Location [Note: map location to Climate Zone and Latitude]
* WWR
* VLT
* U-Value [Note: U-factor should be inclusive of sash and frame]
* SHGC {assume this value as 'Y'}


**Process**

Lookup and check SHGC and U-value from Table 4.10 and 4.11, if requirements are met *SKIP* and dispplay "<Compliance level> compliance met." & Exit
	
else Start SEF & Eq. SHGC Calculation

## Step3: SEF & Eq.SHGC Calculation
Store SHGC Value from table {assume this value as 'X'}

**Input**

* Orientation
* Height
* Width 
* Is there shading?
	* if Yes Show 'Overhang' and 'Fin' Checkbox.
	*[Checkbox] Overhang
		* input Depth (d1)
		* calculate : PF1 = d/H
	*[CHeckbox] Fin
		* input Depth of shortest fin (d2)
		* calculate : PF2 = d/W
* Is There any Obstruction?
	* If Yes assume PF3 = 0.4
	
**Process**

* Take MaxPF
* MaxPF should be greater than or equal to 0.25 otherwise show msg "Equivalent Shadding is not applicable" and Exit
* Lookup SEF value (assume A) from Table 4.12 & 4.13 on the basis of latitude, orientation, MaxPF
* Eq.SHGC (Z) = A * X

**Compliance Check**
if Y<Z , Display ""<Compliance level> compliance met.", else "<Compliance level> compliance not met."
		
