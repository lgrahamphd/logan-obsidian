---
aliases:
  - RAUN-TEK
---
Last updated: 2024-11-08
### Basic Facts
**Monitored Element:** RAUN 161KV - TEKAMHO 161KV
- Common Name: Raun - Tekamah
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: RAUN 5
- To Bus: TEKAMAH5
**ISO(s):** [[MISO]], [[SPP]]; MEC is in MISO; OPPD is in SPP; monitored element is from MISO bus to SPP bus; contingency is from SPP bus to MISO bus
- From Zone: MEC (MISO)
- To Zone: OPPD (SPP)
**Nearby Landmarks:** Sioux City, IA
**For loss of:**
1. MECOPP1
    - Common Name: Fort Calhoun - Raun (from SPP to MISO)
    - Voltage: 345 kV
	- Equipment Type: Transmission Line
    - From Bus: FT_CAL
    - To Bus: RAUN
**Direction Bound:** Backwards; from Raun to Tekamah
---
### History
Bound for 172.8 hours in RT from Oct. 1 - Nov. 7, 2024 at a $\$80.43/MWh$ average.

---
### Drivers
**Topology:**
- Tekamah - Oakland 115 kV outage (SPP equipment)
	- 2024-09-26 09:51 actual start, 2024-10-31 10:48 actual end.
Tekamah - Oakland 115 kV provides the only East-to-West flow capacity along the 115 kV path from Raun to Northern Omaha. With Tekamah - Oakland 115 kV out, if Fort Calhoun - Raun 345 kV were to be lost to outage, the Raun - Tekamah5 - S1226 5 115 kV path would overload.

**Generation:**
George Neal North and George Neal South both push on the constraint.

Large baseload generators push on the constraint.
- Monticello
- Prairie Island
- Sherburne County
- Coal Creek
- Milton R. Young

---
#### Related Constraints
[[MISO/Constraint Analyses/Old Constraint Notes/Tekamah - Substation 1226 161 kV FLO Ft. Calhoun - Raun 345 kV]], which is in series with Tekamah - Oakland 115 kV.

---
#### Bearish Risks
Flows along the monitored element can reverse. Typically, flows are from North-to-South from Souix City, IA to Omaha, NE. As such, there does exist counterflow risk. See the 9/27/2024-9/28/2024 period, for example.

Thee SPP outages Cooper NPPD - S3458 345 kV (out in Dec. from 12/1-12/20) and East DC Tie - Welsh 345 kV are slightly bearish ($2\%$ the monitored element's line rating) for the present constraint. No noteworthy bullish planned transmission outages exist for December.

**Solving Generation:**
- Wolf Creek
- Iatan
- Walter Scott Jr.

---
### Forward View
The Tekamah - Oakland 115 kV outage appears to have been a key driver. Since it's return to service on 11/1/2024, the present constraint has bound at a much weaker run rate. Our view is that the present constraint has lost much of its value for December.