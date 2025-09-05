Last updated: 2024-12-04
### Basic Facts
**Monitored Element:** MUDLABENTO23_1 1
- Common Name: Benton - Mud Lake
- Voltage: 230 kV
- Equipment Type: Transmission line
- From Bus: MUDLAKE4
- To Bus: GRE-BENTON 4
- From Zone: [[Minnesota Power and Light Company|MP]]
- To Zone: [[Northern States Power Company|NSP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Saint Cloud, MN
**For loss of:** MPNSP03
1. 9P9_SERCAP50_1 S
    - Common Name: Chisago County North - Chisago County
    - Voltage: 500 kV
	- Equipment Type: Transmission line (very short; within the substation)
    - From Bus: CHIS CO2
    - To Bus: CHIS-N 2
2. FORBTCHIS_50_1 1
    - Common Name: Forbes Tap - Chisago County
    - Voltage: 500 kV
	- Equipment Type: Transmission line
    - From Bus: FORBTAP27494
    - To Bus: CHIS-N 2
3. FORBTFORBE50_1 1
    - Common Name: Forbes Tap - Forbes
    - Voltage: 500 kV
	- Equipment Type: Transmission line
    - From Bus: FORBTAP27494
    - To Bus: FORBES
**Direction Bound:** Backwards; from Benton to Mud Lake
---
### History
Last 30 days: 11/4/2024-12/4/2024
- RT Peak shadow price: 0 hours bound
- RT Off-Peak shadow price: $4.16/MWh; 14.9 hours bound
---
### Drivers
**Topology:**
Bunker - Sherco 345 kV has been out since 2024-11-18 10:41, and it's due to return to service 2025-03-28 16:00. This outage reduces takeaway capacity from Sherburne County into Minneapolis.

**Generation:**
- Sherburne County
- Monticello
- Sherco Solar
- Elk River

**Load:**
Brainerd, MN; Duluth, MN; Winnipeg, MB

**Line Ratings:**
Benton - Mud Lake uprated from 385 MW to 478 MW from 11/18/2024-11/20/2024. It is possible (but very unlikely) for this line to derate during the winter.

**Commentary:**
The present constraint cuts Minneapolis-St. Paul and Saint Cloud off from the Northern half of MN, Manitoba, and North Dakota. Sherburne County, Monticello, Sherco Solar, and Elk River can push on the constraint if their flows aren't needed by the Twin Cities load pocket.

During winter, flows along Benton - Mud Lake are biased Northward (during the summer, Southward flows are the theme).

---
### Forward View
Risk remains that the present constraint will bind over the winter. If the above units are running and Northern MN, Manitoba are very cold, then the constraint could bind. However, the run rate is low. Fair values should be muted.

---
### Highest Exposure Paths
Sources:
- NSP.GRANTY.ARR
- NSO.STCLOUD1
- NSP.SHERCO.3
Sinks:
- MP.AEPE14
- GRE.BEPCMP.CWT
