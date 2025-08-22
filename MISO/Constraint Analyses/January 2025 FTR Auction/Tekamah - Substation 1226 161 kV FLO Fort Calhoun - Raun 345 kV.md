Last updated: 2024-12-06
### Basic Facts
**Monitored Element:** TEKAMSUB1216_1 1 (yes -- 12**1**6 even though the substation is 12**2**6)
- Common Name: Tekamah - Substation 1226
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: TEKAMAH5
- To Bus: S1226 5
- From Zone: [[Omaha Public Power District|OPPD]]
- To Zone: [[Omaha Public Power District|OPPD]]
**ISO(s):** [[MISO]], [[SPP]]. The monitored element is SPP equipment, and the contingency is a MISO tie line.
**Nearby Landmarks:** Sioux City, IA; Omaha, NE
**For loss of:** MECOPP1
1. FT_CARAUN34_1 1
    - Common Name: Fort Calhoun - Raun
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: FT_CAL (SPP; OPPD)
    - To Bus: RAUN (MISO; [[MidAmerican Energy Company|MEC]])
**Direction Bound:** from Tekamah to Substation 1226
---
### History
Last 30 days: 2024-11-07 - 2024-12-06
- RT Peak shadow price: $43.12/MWh; 46.7 hours bound
- RT Off-Peak shadow price: $28.73/MWh; 47.5 hours bound

---
### Drivers
**Generation:**
Wind generation in Northern Iowa and Southwestern Minnesota push on the constraint, To a greater degree than is the case for [[Raun - Tekamah 161 kV FLO Fort Calhoun - Raun 345 kV]], wind generation in Nebraska Southwest of Sioux City, IA pushes on the constraint.

Walter Scott Jr., Nebraska City, Lon Wright, North Omaha are on the high side of the constraint and can solve.

**Load:**
Omaha, NE.

**Line Ratings:**
SPP state estimator data indicate that post-contingent line ratings are static at 256 MW.

**Commentary:**
This constraint will induce wind generation curtailment.

---
### Forward View
We expect Raun - Tekamah to continue to bind during high-wind generation periods in Northern Iowa, Southwestern Minnesota, and Nebraska to the Southwest of Sioux City, IA.

---
### Highest Exposure Paths
Sources:
- ALTW.WSEC3
- MEC.SHENDO_1
Sinks:
- MEC.MEAN_7.AZ
- MEC.COMP.ARR
- ALTW.JOUNEAL3
- MEC.PLYMOUTH1

In January, 2024, these paths went significantly negative despite a moderately strong MCP. This lead to approximately -$15/MWh losses for the Peak class. The Off-Peak class was also painful for the market, but it did not produce negative revenue. January, 2023 was also challenging. Be conservative with assigning value to this constraint.