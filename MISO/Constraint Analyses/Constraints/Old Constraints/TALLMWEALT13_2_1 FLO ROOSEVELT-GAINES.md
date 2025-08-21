### Basic Facts
**Monitored Element:** TALLMWEALT13_2 1
- 128 kV line
- From Bus: 18TALLMG
- To Bus: 18WEALTHYW
- Part of a 138 kV double circuit
	- TALLMWEALT13_1 1
**ISO:** [[MISO]]
- CONS, CONS
**Contingency Name**: MET34088
**For loss of:**
1. GAINEROOSE34_1 1
    - 345 kV line
    - From Bus: 18GAINES
    - To Bus: 18ROSVLT

**Direction Bound:** forward
**Constraint ID:** 457446
**History:**
- **DA**: no constraint with MB TALLMWEALT13_2 1 has every bound in DA
- **RT**: bound 4.7 hours HE 14 - HE 19 on 8/26/2024
	- $\$200.79/MWh$
### Drivers
**Topology:**
- Parallel circuit TALLMWEALTH13_1 1 is out 06:28 8/19/2024 - 15:00 8/30/2024.
- 345 kV line LUDINTALLM34_1 in addition to numerous 138 kV lines are out in the area as a result of a transmission rebuild project.

**Generation:**
- Ludington (1.6 GW pumped hydro); pushes on the constraint during on-peak periods.
- Zeeland (900 MW NG combined cycle).
- J. H. Campbell (1.4 GW coal) is also in the area, but it doesn't appear to push on the constraint.

**Load:**
- Grand Rapids, MI
	- CONS.KENCNTY1
	- CONS.ADA
- Between Grand Rapids, MI and Kalamazoo, MI
	- CONS.DR.CETR
### Forward View
Until the parallel circuit TALLMWEALTH13_1 1 returns from outage (planned: 15:00 hrs. 8/30/2024), risk of this constraint binding remains during on-peak medium-high load events associated with Grand Rapids, MI.

This constraint did not bind in the DA market for 8/27/2024. Given that 8/26/2024 is the first time this constraint ever bound, it's likely that the market hasn't yet converged to an efficient price with respect to the constraint. In our view, *this constraint presents a decrement bid opportunity in the short term*.