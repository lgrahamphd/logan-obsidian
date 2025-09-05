Last updated: 2024-12-05
### Basic Facts
**Monitored Element:** ARROWHD TR7
- Common Name: Arrowhead TR7
- Voltage: 230/115 kV
- Equipment Type: Transformer
- From Bus: ARROWHD4
- To Bus: ARD1BUS7
- From Zone: [[Minnesota Power and Light Company|MP]]
- To Zone: [[Minnesota Power and Light Company|MP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Duluth, MN
**For loss of:** MP23X03
1. ARROWHD TR6
    - Common Name: Arrowhead TR6
    - Voltage: 230/115 kV
	- Equipment Type: Transformer
    - From Bus: ARROWHD4
    - To Bus: ARD1BUS7
**Direction Bound:** Backward; stepping down in voltage from 230 kV to 115 kV
Panorama seems to have an issue with respect to reporting the constraint's direction. As a result, constraint flow and shift factors have the incorrect sign.

---
### History
Last 30 days: 11/5/2024-12/4/2024
- RT Peak shadow price: $10.98/MWh; 20.1 hours bound
- RT Off-Peak shadow price: $9.83/MWh; 14.6 hours bound
Started binding 11/6/2024.
---
### Drivers
**Topology:**
St. Lake - Arrowhead 345 kV was out 2024-11-04 10:26 - 2024-11-22 13:56.
Hilltop - 98L Tap4 230 kV in addition to its 230/115 kV transformer, Hilltop TR1, have been out since 2024-11-05 08:56, and it's planned to return 2024-12-19 17:00. This appears to be the leading topological driver.

**Generation:**
[[Clay Boswell]] (940 MW, subbituminous coal) pushes on the constraint.

**Load:**
Duluth, MN at the 161 kV and 115 kV levels.

**Line Ratings:**
Static post-contingent line ratings at 391 MW.

**Commentary:**
Flows from Winnipeg through Chisago County

---
### Forward View
In Jan. 2025, the Rush - Rock Creek 230 kV, Forbes - Arrowhead 230 kV, and Eau Claire - King 345 kV outages are bearish for the constraint. None of the planned transmission outages appear bullish. In concert with the conclusion of the Hilltop - 98L Tap4 230 kV and Hilltop TR1 outages 12/19, we see a substantial decrease in binding risk for Jan. 2025.

---
### Highest Exposure Paths
Sources:
- MP.HVDCE
- NSP.NWEC.AZ
Sinks:
- MP.HIBBAR3
- MP.FONDLA1
- MP.THOMSON
- GRE.AEPEML

The maximum exposure path MP.HVDCE -> MP.HIBBAR3 has been an excellent trade for XZ24 (in the ballpark of $6/MWh-$11/MWh profits). It's worth a try to short the path at a favorable premium, say, $3/MWh or more. For this to clear, we'd need the market to fall victim to fundamentally-misaligned recency bias, but this could happen.