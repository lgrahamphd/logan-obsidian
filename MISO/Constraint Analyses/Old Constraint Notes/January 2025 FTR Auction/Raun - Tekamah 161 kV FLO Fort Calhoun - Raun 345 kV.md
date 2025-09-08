Last updated: 2024-12-06
### Basic Facts
**Monitored Element:** FAUNTEKAM16_1 1
- Common Name: Raun - Tekamah
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: RAUN 5
- To Bus: TEKAMAH5
- From Zone: [[MidAmerican Energy Company|MEC]]
- To Zone: [[Omaha Public Power District|OPPD]]
**ISO(s):** [[MISO]], [[SPP]]; tie line on which the price is set by SPP.
**Nearby Landmarks:** Sioux City, IA; Omaha, NE
**For loss of:** MECOPP1
1. FT_CARAUN34_1 1
    - Common Name: Fort Calhoun - Raun
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: FT_CAL (SPP; OPPD)
    - To Bus: RAUN (MISO; MEC)
**Direction Bound:** from Raun to Tekamah
---
### History
Last 30 days: 2024-11-07 - 2024-12-06
- RT Peak shadow price: $22.11/MWh; 21.6 hours bound
- RT Off-Peak shadow price: $7.75/MWh; 13.3 hours bound

---
### Drivers
**Generation:**
Wind generation in Northern Iowa and Southwestern Minnesota push on the constraint. George Neal North and South both push on the constraint as well. To a lesser degree, wind generation in Nebraska Southwest of Sioux City, IA can push on the constraint.

Walter Scott Jr., Nebraska City, Lon Wright, North Omaha are on the high side of the constraint and can solve.

**Load:**
Omaha, NE

**Line Ratings:**
MISO state estimator data show that this line was uprated from 217 MW to 284 MW on 11/8/2024.
SPP state estimator data show that the post-contingent line rating is still 217 MW, but that it briefly uprated to 262 MW in January, 2024, back down to 217 MW, then up again to 259 MW in February, 2024 before dropping to 217 MW once more.

There exists uncertainty around what the true line rating is, but we trust SPP's ratings data more.

12/5/2024 M2M FFE file indicates MISO flows of 36 MW, suggesting that SPP has substantially more control over the line.

**Commentary:**
This constraint will induce wind generation curtailment.

---
### Forward View
We expect Raun - Tekamah to continue to bind during high-wind generation periods in Northern Iowa and Southwestern Minnesota.

---
### Highest Exposure Paths
Sources:
- MEC.MEAN_7.AZ
- MEC.COMP.ARR
Sinks:
- ALTW.WSEC3
- MEC.FARMER

In January, 2024, these paths went significantly negative despite a moderately strong MCP. This lead to approximately -$15/MWh losses for the Peak class. The Off-Peak class was also painful for the market, but it did not produce negative revenue. January, 2023 was also challenging. Be conservative with assigning value to this constraint.