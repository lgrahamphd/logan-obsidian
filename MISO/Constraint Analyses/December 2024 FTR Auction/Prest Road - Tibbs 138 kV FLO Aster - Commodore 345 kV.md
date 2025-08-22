---
aliases:
  - PRES-TIBB
---
Last updated: 2024-11-08
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
Bound 324.6 hours in RT from Oct. 1 - Nov. 6, 2024 at a $\$84.39/MWh$ average.

---
### Drivers
**Topology:**
The below two in-series line outages eliminate 345 kV Eastward takeaway capacity from Prairie State. In turn, should Aster - Commodore 345 kV be lost, Prest Road - Tibbs 138 kV would overload as Southward flows along Prairie State - Aster 345 kV would step down to the 138 kV level and join Baldwin - Prest Road 138 kV flows.
- Mt. Vernon W - West Frankfort E 345 kV outage
	- Bullish $12\%$ of the monitored element's line rating
	- Ongoing outage: 2024-09-19 07:00 actual start, 2024-12-17 17:00 scheduled end.
- Prairie State - Mt. Vernon W 345 kV outage
	- Bullish $26\%$ of the monitored element's line rating
	- Planned outage: 2024-11-18 09:00 scheduled start, 2024-12-08 17:00 scheduled end.

The following outages are brief, yet impactful and bullish, adding to the bullish sentiment from the above:
- Rush Island - Baldwin 345 kV
	- Bullish $3\%$ of the monitored element's line rating
	- Planned outage: 2024-12-03
- Massac - Kelso 345 kV
	- Bullish $5\%$ of the monitored element's line rating
	- Planned outage 2024-12-10 09:00 - 2024-12-11 17:00

**Generation:**
- [[Prairie State]]
- [[Baldwin]]

**Load:**
- Paducah, KY
- Carbondale, IL
- Marion, IL

### Bearish Factors
- Prairie State Unit 2 is scheduled to be out 2024-10-15 - 2024-11-22 for "Major Boiler Maintenance, Heater Section (Air, Super, Reheat), Ducts, Fans, Cooling Tower Maintenance, Tube Replacement, Drums, Cleaning) Turbine Inspection, Balance of Plant, Testing."
	- This is 883 MW, 1/2 of Prairie State's capacity.
	- If this outage were to slip, then the constraint would lose some of its value (our view is that it would still bind, but at weaker shadow prices).
- Prairie State Unit 1 is scheduled to be out 2024-12-03 - 2024-12-13 for "Balance of Plant and Preventative Punch List Boiler and Turbine Maintenance."
	- This is 883 MW, 1/2 of Prairie State's capacity.
- Labadie Unit 3 is out through 12/12/2024. This is 1/4 of Labadie's capacity. Generation shift factors indicate that Labadie pushes on the presently-considered constraint.
---
#### Line Rating Notes
- The branch rating for Prest Road - Tibbs is both dynamic and seasonal. It historically hits the annual post-contingent maximum rating of 236 MW in mid-October (up from 202 MW summer rating). On 2024-10-16, SE data show that the post-contingent line rating hit 239 MW, which appears to be a record high. Due to the dynamic nature, the line rating fell from this maximum through the balance of October.
- Despite the line rating fluctuations, the constraint has persistently bound in RT.

---
### Forward View
With Prairie State Unit 1 out for 11 days in Dec., the constraint loses some of its value. Our view is that it will still bind, but at weaker shadow prices. While Prairie State pushes on the constraint, the Prairie State - Mt. Vernon W 345 kV and Mt. Vernon W - West Frankfort E 345 kV line outages are the primary drivers.