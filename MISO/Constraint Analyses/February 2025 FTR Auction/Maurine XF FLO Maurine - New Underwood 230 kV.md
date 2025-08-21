Last updated: 2025-01-06
### Basic Facts
**Monitored Element:** MAURINE KV1A1
- Common Name:  Maurine XF
- Voltage: 230/1 kV
- Equipment Type: 3-winding transformer
- From Bus: MAURINE4
- To Bus: MAURINE
- From Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
**ISO(s):** [[MISO]], [[SPP]]; SPP equipment
**Nearby Landmarks:** Maurine, SD; Badlands National Park
**For loss of:** WAU23040
1. MAURINUNDR23_1 1
    - Common Name: Maurine - New Underwood
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: MAURINE4
    - To Bus: NUNDRWD-LNX3
**Direction Bound:** up the transformer from the 1 kV level to the 230 kV level

---
### Drivers
**Topology:**
The Chapelle - Leland Olds 345 kV outage (2024-11-21 10:00 - 2025-01-23 17:00) was somewhat bullish, but it is unnecessary for the constraint to bind.

**Generation:**
- Wild Springs solar (new build -- June 2024)
- Willow Creek wind line
- Laramie River
- Gentleman

**Load:**
Northbound flows into North Dakota and Wyoming seem to be necessary conditions for the present constraint to bind.

**Line Ratings:**
Static 125 MW post-contingent rating.

**Flow Bias:**
Typical flows are up the transformer. Occasionally, the flow direction can reverse.

**Commentary:**
With the contingency (Maurine - New Underwood 230 kV) out, Northbound flows along Maurine - Bison 230 kV pull on the Maurine transformer to step up from the 115 kV level.

The Glenham - Whitlock 230 kV outage (2025-02-03 09:00 - 2025-03-28 16:00) is bullish. Malta - Richardson Coulee 161 kV is mildly bearish.

---
### Fair Value Modeling Notes
Planned February outages aren't particularly affective. If anything, they're slightly bullish.

[[Hettinger - Centipede 115 kV FLO Bowman - Hettinger 230 kV]] is closely related to Maurine XF. After a brief investigation with Ross, we found a perplexing misalignment with MISO and SPP in which the Maurine XF constraint was binding in SPP, but not in MISO. This led to periods during which the Hettinger-Centipede bound, but the Maurine XF did not. That's notable, since we would expect the Maurine XF constraint to bind before Hettinger-Centipede.

---
### Highest Exposure Paths
Any expressions of a view on the present constraint needs to be considered in concert with an expression of a view on [[Hettinger - Centipede 115 kV FLO Bowman - Hettinger 230 kV]].

It might make sense to consider a "high-to-higher" path along the lines of MDU.CEDARHLS -> MDU.TSWF1, but only if we believe that Hettinger - Centipede 115 kV will not bind.