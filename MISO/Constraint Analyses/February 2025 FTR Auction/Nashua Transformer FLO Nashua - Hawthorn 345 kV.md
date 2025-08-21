Last updated: 2025-01-07
### Basic Facts
**Monitored Element:** NASHUA T1_H
- Common Name: Nashua Transformer
- Voltage: 345/1 kV
- Equipment Type: 3-winding transformer
- From Bus: NASHUA 7
- To Bus: NASHUA
- From Zone: KCPL
- To Zone: KCPL
**ISO(s):** [[MISO]], [[SPP]]; SPP equipment
**Nearby Landmarks:** Kansas City International Airport
**For loss of:** KCP34102
1. NASHUA_HAWTH A
    - Common Name: Nashua-Hawthorn
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: NASHUA 7
    - To Bus: HAWTH 7
**Direction Bound:** from Nashua to Hawthorn

---
### Drivers
**Topology:**
The below outages cut off Southward flows from Iatan into the Craig substation and down to the 161 kV level.

CRAIG__STR_CR1 A from 2024-09-30 17:28 - 2024-10-18 11:02, 2024-12-09 10:46-2024-12-23 12:21.

87TH_ST CRAIG__STR_CR1 B from 2025-01-02 07:02 - 2025-01-09 17:00.

**Generation:**
Wind-driven. Coal generation also pushes on the constraint. Gas generation is on the high side.

**Load:**
Kansas City

**Line Ratings:**
Static post-contingent line rating of 715 MW.

**Flow Bias:**
Exclusively down the transformer from the 345 kV -> 1 kV -> 161 kV.

**Commentary:**
This constraint is driven by a voltage step-down bottleneck from the 345 kV level to the 161 kV level.

---
### Fair Value Modeling Notes
Craig KCPL 345/161 kV XFMR #11 (SPP equipment) is due to be out 2025-01-08 08:00 - 2025-02-25 16:00.

Wind generation pushes.

Iatan and Cooper push.

Hawthorn relieves.

---
### Highest Exposure Paths
MEC.FARMER -> AMMO.CALF_1.AZ. $9.91 Peak, $10.17 Off-Peak for G25 MCPs as of the F25 auction.