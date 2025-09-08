Last updated: 2024-12-03
### Basic Facts
**Monitored Element:** SWAN_WILMA11_1 1
- Common Name: Swan Lake - Wilmarth
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: SWAN LK7
- To Bus: WILMART7
- From Zone: [[Northern States Power Company|NSP]]
- To Zone: [[Northern States Power Company|NSP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Mankato, MN
**For loss of:** NSP34011
1. HELENSHEAS34_1 1
    - Common Name: Helena - Sheas Lake
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: HELENA 3
    - To Bus: SHEAS LK3
**Direction Bound:** Backwards; from Wilmarth to Swan Lake
---
### History
Last 30 days: 11/4/2024-12/3/2024
- RT Peak shadow price: $18.09/MWh; 45.2 hours bound
- RT Off-Peak shadow price: $19.31/MWh; 30.5 hours bound

---
### Drivers
**Topology:**
- Crandal - Wilmarth 345 kV was out 2024-10-31 10:26 - 2024-11-07 18:56.
- Wilmarth - Huntely 345 kV was out 2024-11-04 12:11 - 2024-11-08 10:56.
- Wilmarth TR9 345/1 kV was out 2024-11-04 12:11 - 2024-11-07 18:56.

Each of the above contributed to the above constraint binding. However, this constraint has continued to bind in RT and DA after the above outages completed.

**Generation:**
[[Mankato Energy Center]]
Wind generation to the South:
- [[Odell Wind Farm]]
- [[Palo Alto Wind Farm]]
- [[Trimont Area Wind Farm]]
- [[Elm Creek Wind Farm]]

**Load:**
Load on lower voltage levels (115 kV, 69 kV) in New Ulm, MN and to its Northwest pull on the constraint. Should Helena - Sheas Lake 345 kV be lost, then its flows shift onto Swan Lake - Wilmarth 115 kV, resulting in an overload.

**Line Ratings:**
Historical SE data indicate that Swan Lake - Wilmarth's post-contingent line ratings reach a maximum of 207 MW from Dec. 1 - end of Feb. Outside of winter, the line ratings can fluctuate on a daily and/or sub-daily basis. At the time of this writing, the 11/19/2024 SE data show a rating of 181 MW. Despite the expected uprate on 12/1/2024, the constraint bound in RT on 12/2/2024 for 5.3 hours at a $105.71/MWh daily average.

**Commentary:**
Load on at lower voltage levels (115 kV, 69 kV) pulls on the constraint.

---
### Forward View
Despite the winter uprate, risk persists that Swan Lake - Wilmarth 115 kV will continue to bind in December, 2024 and January, 2025. This is particularly true if the New Ulm, MN and Twin Cities areas are hit with cold weather. The former pulls on the constraint; the latter would potentially drive Mankato Energy Center to run at a high capacity factor, which would push on the constraint.

Avoid overpaying due to recency bias. Sharp decrease in MCP from Nov24 to Dec24 auctions ($12.77 to $6.50) for the NSP.CC.MANKAT1 -> NSP.NU path. If it's cheap, then some layering with some different sinks could be interesting.

---
### Highest Exposure Paths
Sources:
- NSP.CC.MANKAT1
- NSP.WILMAR1
Sinks:
- NSP.NU
- NSP.CMMPA.SE
- NSP.CMMPA.FAIR
- NSP.RWF__1_QS