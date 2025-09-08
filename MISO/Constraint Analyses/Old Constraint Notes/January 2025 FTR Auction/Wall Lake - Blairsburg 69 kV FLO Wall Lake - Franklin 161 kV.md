Last updated: 2024-12-09
### Basic Facts
**Monitored Element:** WALLLBLRSB69_1 1
- Common Name: Wall Lake - Blairsburg
- Voltage: 69 kV
- Equipment Type: Transmission line
- From Bus: WALL LAKE8
- To Bus: BLAIRSBU8
- From Zone: [[MidAmerican Energy Company|MEC]] (MISO)
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]] (SPP)
**ISO(s):** [[MISO]], [[SPP]]
**Nearby Landmarks:** Webster City, IA
**For loss of:** MEC16126
1. FRANKWALLL16_1 1
    - Common Name: Wall Lake - Franklin
    - Voltage: 161 kV
	- Equipment Type: Transmission line
    - From Bus: FRANKLIN51
    - To Bus: WALL LAKE5
**Direction Bound:** from Wall Lake to Blairsburg
---
### History
Last 30 days: 2024-11-10 - 2024-12-09
- RT Peak shadow price: $45.11/MWh; 21.8 hours bound
- RT Off-Peak shadow price: $2.09/MWh; 2.5 hours bound

In RT, bound for roughly 1 hour on 11/20, then for roughly 17 hours between 12/3-12/4. Has bound again in RT on 12/9.

---
### Drivers
**Topology:**

**Generation:**
Century Wind Farm (200 MW). This constraint is the primary mechanism for curtailing Century Wind Farm's generation.

Wellsburg and Ivester wind farms are on the high side.

**Load:**
Ames, IA at the 69 kV and 115 kV levels.

**Line Ratings:**
Post-contingent line ratings were uprated from 66 MW to 72 MW on 11/1/2024.

**Commentary:**
Should the contingency, Wall Lake - Franklin 161 kV be lost, then the 115/69 kV transformer from WALL LAKE5 to WALL LAKE8 will receive increased flows. Downstream of this transformer, the monitored element, Wall Lake - Blairsburg 69 kV will also receive increased flows. While there exists another constraint -- Wall Lake 161/69 kV XF FLO Wall Lake - Franklin 161 kV -- in which the transformer is the monitored element and the contingency is the same (Wall Lake - Franklin 161 kV), the present constraint -- Wall Lake - Blairsburg 69 kV -- has bound the vast majority of the time. This is because the transformer has a post-contingent line rating of 105 MW, whereas the Wall Lake - Blairsburg 69 kV line has a post-contingent line rating of 72 MW.

---
### Forward View
Scheduled outages are bearish the constraint in January according to Panorama's Forward Impact Decomposition tool. These include LAUREM_TOW16_1 (1/20-1/31), ADAMSMITCH34_1 (1/6-2/14), T61 @ RIEL in MHEB (1/12-1/18), and PRAR_M_TOW11_1 (1/6-2/18). With that said, the Forward Impact Decomposition tool was not bullish Z24, but the constraint has bound. It appears that this constraint can bind when flows along Wright - Wall Lake 161 kV are Eastward and Century Wind Farm is running at a high capacity factor.

---
### Highest Exposure Paths
Sources:
- MEC.CENTURY_1
Sinks:
- ALTW.HCPD.STHP
- ALTW.DR.AURLD -- *is this a new CPNode? Any path I construct with it shows no data in the FTR Path History tool.*
The current Peak F25 MCP for MEC.CENTURY_1 -> ALTW>HCPD.STHP is $0.37/MWh, which is a deal.