Last updated: 2024-12-06
### Basic Facts
**Monitored Element:** BVISTALTMU69_1 1
- Common Name: Buena Vista - Alta
- Voltage: 69 kV
- Equipment Type: Transmission line
- From Bus: BUENA VISTA8
- To Bus: ALTAMUNITAP8
- From Zone: [[MidAmerican Energy Company|MEC]]
- To Zone: [[MidAmerican Energy Company|MEC]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Alta, IA
**For loss of:** MEC16X52
1. LIT_SX LSX_AC
    - Common Name: Little Sioux XF
    - Voltage: 161/69 kV
	- Equipment Type: Transformer
    - From Bus: LTL SIOUX 5
    - To Bus: LTL SIOUX 8
**Direction Bound:** from Buena Vista to Alta
---
### History
Last 30 days: 2024-12-07 - 2024-12-06
- RT Peak shadow price: $68.61/MWh; 13.8 hours bound
- RT Off-Peak shadow price: $63.59/MWh; 14.3 hours bound

Buena Vista - Alta 69 kV FLO Little Sioux - Clipper 161 kV has also bound (as recently as 2024-11-12 23:00), yet at a substantially lower shadow price.

---
### Drivers
**Topology:**
- ALTAMALTMU69_1 1. This might be a known switching solution? It's been out since 2019-01-19.
- HOSPELSXC69_1
- MARCUMEAD_69_1
- PLYMOSIOUX69_1

The latter three lines are scheduled to be out through 2024-12-06. They seem to have been key drivers (together with wind generation and winter demand). Afterwards, a different set of outages is bearish the constraint.

**Generation:**
- Storm Lake Wind Farm (194 MW)
- Pomeroy Wind Farm (286 MW)
- Pocahontas Prairie Wind Farm (80 MW)

**Load:**
Alta, IA; Storm Lake, IA; Cherokee, IA.

**Line Ratings:**
Dynamic post-contingent line ratings varying from 44 MW to 83 MW.

**Commentary:**
Storm Lake Wind Farm Phase 1 (114 MW) connects into the 24.9 kV STORM LK W bus. Attached to this are two generator step-up transformers that connect STORM LK W to BUENA VISTA5 at the 161 kV level. For flows to step down to the 69 kV level at the Buena Vista substation, the 161/69 kV transformer incident to BUENA VISTA5 (161 kV) and BUENA VISTA8 (69 kV) is necessary.

If the Little Sioux 161/69 kV transformer were lost, then the 161/69 kV transformer mentioned above would receive increased flows which would then overload the incident line/monitored element, Buena Vista - Alta 69 kV.

![[Buena Vista substation, Storm Lake Wind Farm.png]]

---
### Forward View
We predict a substantial decrease in binding probability and severity after the aforementioned outages conclude on 12/6/2024. That said, extremely high wind generation or a forced outage at the 69 kV level could lead to this constraint binding.

---
### Highest Exposure Paths
It's challenging to find a source PNode that is exposed to this constraint. Shift factors indicate that 0.45% is the largest shift factor. The highest-exposure sink has a shift factor of -8.8%. This maximum exposure path is relatively ineffectual.

Sources:
- ALTW.FCLDFCL1
Sinks:
- MEC.MEAN_5.AZ

Paths constructed around this constraint are likely to be heavily influenced by Raun - Tekamah - Sub congestion. Historically, such congestion has dominated the price decomposition to the point at which a path like ALTW.FCLDFCL1 -> MEC.MEAN_5.AZ is primarily a way to express a view on Raun - Tekamah - Sub rather than a view on Buena Vista - Alta.