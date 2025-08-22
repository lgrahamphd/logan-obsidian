Last updated: 2025-01-06
### Basic Facts
**Monitored Element:** FTTHOMP KU1B1
- Common Name: Fort Thompson XF B
- Voltage: 345/1 kV
- Equipment Type: 3-winding transformer
- From Bus: FTTHOMP47206
- To Bus: FTTHOMP
- From Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
**ISO(s):** [[MISO]], [[SPP]]; SPP equipment
**Nearby Landmarks:** Fort Thompson, SD
**For loss of:** WAU34X20
1. FTTHOMP KU1A1
    - Common Name: Fort Thompson XF A1
    - Voltage: 345/1 kV
	- Equipment Type: 3-winding transformer
    - From Bus: FTTHOMP47206
    - To Bus: FTTHOMP
2. FTTHOMP KU1A2
	- Common Name: Fort Thompson XF A2
	- Voltage: 230/1 kV
	- Equipment Type: 3-winding transformer
	- From Bus: FTTHOMP4
	- To Bus: FTTHOMP
3. FTTHMOP KU1A3
	- Common Name: Fort Thompson XF A3
	- Voltage: 13.8/1 kV
	- Equipment Type: 3-winding transformer
	- From Bus: FTTHOMP
	- To Bus: FTTHOMP
**Direction Bound:** from the 345 kV level to the 1 kV level

---
### Drivers
**Topology:**
Chapelle - Leland Olds 345 kV has been on outage since 2024-11-21 10:00. It's planned to be out until 2025-01-23 17:00. With this line out, flows from Grande Prairie - Fort Thompson 345 kV have no outlet at CHAPELLE-BE3. Instead, such flows along the 345 kV level must step down via the two Fort Thompson 3-winding transformers (one of which is the contingency, and one of which is the monitored element in the present constraint).

**Generation:**
Big Bend Dam

**Line Ratings:**
Static 313 MW post-contingent line rating.

**Flow Bias:**
The bias is in favor of flowing down the transformer (from the 345 kV level to the 1 kV level). However, there have been periods during which flows have been observed going *up* the transformer.

---
### Fair Value Modeling Notes
Model the risk of the Chapelle - Leland Olds 345 kV outage being extended into February.
Our view is that there is a high likelihood that this constraint stops binding after the Chapelle - Leland Olds 345 kV outage has finished.

Glenham - Whitlock 230 kV (SPP equipment) is due to be out of service 2025-02-03 09:00 - 2024-03-28 16:00. This is bearish the constraint.

This seems like a good opportunity to go short.

---
### Highest Exposure Paths
It's tough to construct a high-exposure path. 12% exposure seems to be the maximum possible value.

Sources:
- MEC.FARMER
- CWLD.BLRG
- MEC.CONTRAIL1
- AECI
- SPA

Sinks:
- MDU.TSWF1
- MDU.BEPC
- MDU.CEDARHLS
- numerous others
