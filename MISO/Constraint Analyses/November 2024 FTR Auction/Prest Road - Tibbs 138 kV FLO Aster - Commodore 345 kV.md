Last updated: 2024-10-15
### Basic Facts
**Monitored Element:** PRES_TIBB_1558 A
- Common Name: Prest Road - Tibbs 138 kV
- Voltage: 138 kV
- Equipment Type: Transmission line
- From Bus: 4PREST
- To Bus: 4TIBBS
**ISO(s):** [[MISO]]
- From Zone: [[Ameren Illinois|AMIL]]
- To Zone: [[Ameren Illinois|AMIL]]
**Nearby Landmarks:** Baldwin
**For loss of:**
1. AMI34108
    - Common Name: Aster - Commodore
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: 7ASTER
    - To Bus: 7CMDR
**Direction Bound:** forward; Prest Road -> Tibbs
---
### History
Bound 274.7 hours in RT from Sep. 15 - Oct. 15, 2024 at a $\$84.08/MWh$ average. This was the #2 RT constraint over this period. Pleasant Lake - Leeds was the top RT constraint at $\$101.23/MWh$.

---
### Drivers
**Topology:**
The below two in-series line outages eliminate 345 kV Eastward takeaway capacity from Prairie State. In turn, should Aster - Commodore 345 kV be lost, Prest Road - Tibbs 138 kV would overload as Southward flows along Prairie State - Aster 345 kV would step down to the 138 kV level and join Baldwin - Prest Road 138 kV flows.
- 7 Mt. Vernon W - 7 West Frankfort E 345 kV outage
	- Ongoing outage: 2024-09-19 07:00 actual start, 2024-12-17 17:00 scheduled end.
- Prairie State - 7 Mt. Vernon W 345 kV outage
	- Planned outage: 2024-10-28 08:00 scheduled start, 2024-11-15 17:00 scheduled end.

**Generation:**
- Prairie State
- Baldwin

**Load:**
- Paducah, KY
- Carbondale, IL
- Marion, IL

### Bearish Factors
- Prairie State Unit 2 is scheduled to be out 2024-10-31 - 2024-11-29 for "Major Boiler Maintenance, Heater Section (Air, Super, Reheat), Ducts, Fans, Cooling Tower Maintenance, Tube Replacement, Drums, Cleaning) Turbine Inspection, Balance of Plant, Testing."
	- This is 883 MW, 1/2 of Prairie State's capacity.
- 4CAMPBHL JCT - 4STEELEVLE N 138 kV, 4CAMPBHL JCT - 4GRAND TW 138 kV, 4CAMPBHL JCT - 4CAMPBELLHIL 138 kV planned outage
	- 2024-11-21 09:00 - 2024-11-21 17:00
	- 2024-11-25 09:00 - 2024-11-27 17:00
	- During these two outage windows, it's unlikely that the constraint will bind, as flows through the monitored element along paths through Campbell Hill Junction substation in Steeleville, IL will not be possible.
- Labadie Unit 3 is out through 12/12/2024. This is 1/4 of Labadie's capacity. Generation shift factors indicate that Labadie pushes on the presently-considered constraint. However, this feels tenuous given the local topology. It's possible that Labadie's size (as well as Callaway County's size) are dominating, leading to a false positive relationship with the constraint.
---
#### Line Rating Notes
- The branch rating for Prest Road - Tibbs appears to be both dynamic and seasonal. It historically hits the annual post-contingent maximum rating of 236 MW in mid-October (up from 202 MW summer rating).
- The line rating should be at/near its max as of the time of this writing (10/15/2024), and the constraint is still binding in RT.

---
### Forward View
With the Prairie State Unit 2 outage, the present constraint becomes less attractive. Expect Baldwin to run at a high capacity factor to pick up the slack from Rush Island's retirement and 883 MW of Prairie State capacity offline due to outage.
