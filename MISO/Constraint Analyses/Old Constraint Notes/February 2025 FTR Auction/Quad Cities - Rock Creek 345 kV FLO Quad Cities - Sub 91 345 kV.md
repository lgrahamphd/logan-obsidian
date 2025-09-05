Last updated: 2025-01-08
### Basic Facts
**Monitored Element:** QUAD_ROCK_34_1 1
- Common Name: Quad Cities - Rock Creek
- Voltage: 345 kV
- Equipment Type: Transmission line
- From Bus: QUAD 1 3-11
- To Bus: ROCK CK3
- From Zone: [[COMED]] (PJM)
- To Zone: [[Alliant West|ALTW]] (MISO)
**ISO(s):** [[MISO]], [[PJM]]
**Nearby Landmarks:** Davenport, IA
**For loss of:** CEMEC01
1. QUAD_SUB934_1 1
    - Common Name: Quad Cities - Substation 91
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: QUAD 1 3-11
    - To Bus: SUB 91 3
2. SUB_91 Q91_9T1
    - Common Name: Substation 91 XF
    - Voltage: 345/161 kV
	- Equipment Type: Transformer
    - From Bus: SUB 91 3
    - To Bus: SUB 91 5
**Direction Bound:** from Quad Cities to Rock Creek

---
### Drivers
**Topology:**
Cordova - Substation 39 345 kV was out 2024-12-03 15:15 - 2024-12-16 15:18. This was the primary driver. The constraint has not bound in RT since this outage ended. Without this line, flows from ComEd are bottlenecked and can overload the constraint.

**Generation:**
Quad Cities (2 GW, nuclear)
Cordova (611 MW, NG CC)

**Line Ratings:**
Uprated from 1,248 MW to 1,356 MW on 11/1.

**Flow Bias:**
Primarily from ComEd to MISO (i.e., from Quad Cities to Rock Creek). The direction can flip, often during March, April, May, but occasionally at other times of year.

**Commentary:**
It's clear that the Cordova - Substation 39 345 kV outage was the primary driver for the XZ24 binding events.

---
### Fair Value Modeling Notes
Inspect Quad Cities, Cordova planned outages.

---
### Highest Exposure Paths
Sources:
- AMIL.BSHPHL2
- CE.RETE.NU
Sinks:
- ALTW.8THST.ARR
- DPC.EDNF

A short could make sense. As of the F25 auction, the G25 MCPs are $5.31/MWh Peak, $2.14/MWh Off-Peak for the highest-exposure path.