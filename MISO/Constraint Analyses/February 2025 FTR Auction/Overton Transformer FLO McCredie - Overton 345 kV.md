Last updated: 2025-01-08
### Basic Facts
**Monitored Element:** OVER XFMR_1_345
- Common Name: Overton transformer
- Voltage: 345/161 kV
- Equipment Type: Transformer
- From Bus: 7OVERTON
- To Bus: 5OVERTON 2
- From Zone: [[Ameren Missouri|AMMO]]
- To Zone: [[Ameren Missouri|AMMO]]
**ISO(s):** [[MISO]], [[AECI]]
**Nearby Landmarks:** Columbia, MO
**For loss of:** AECAMO03
1. MCRD_OVER_5475 A
    - Common Name: McCredie - Overton
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: 7MCCRED (AECI)
    - To Bus: 7OVERTON (MISO)
**Direction Bound:** from the 345 kV level to the 161 kV level

---
### Drivers
**Topology:**
McCredie - Montgomery 345 kV Ckt. 2 was retired 2024-06-13 08:00. A parallel circuit is still in place.

**Generation:**
Wind pushes heavily on the constraint. Nuclear (Callaway County) and natural gas-fired generation ease the constraint.

Coal generation around and to the West of Kansas City can also push on the constraint.

The primary driver appears to be surplus generation in NPPD (Nebraska), MEC (Iowa), ALTW (Iowa), WESTAR (Eastern Kansas), and SECI (Western, Central Kansas).

**Line Ratings:**
Static 560 MW post-contingent line rating.

**Flow Bias:**
Greater than 99% of the time, flows are down the transformer.

**Commentary:**
Should McCredie - Overton 345 kV be lost, then flows from the West along KCP Overton - Overton 345 kV will rip down the transformer, as the 345 kV circuit would become radial at the Overton substation.

---
### Fair Value Modeling Notes
Focus on modeling surplus generation in the aforementioned balancing authorities, likely coming from high wind generation during periods of muted load.

The MYWD_SUBT_4577 outage is moderately bullish. It is scheduled for 2025-02-03 09:00 - 2025-02-07 17:00. Other scheduled outages are mostly ineffectual, but perhaps mildly bullish.

Take a close look at the AECI situation nearby.

---
### Highest Exposure Paths
Sources:
- CWLD.BLRG
- MEC.FARMER
Sinks:
- AECI.CWLD
- CWLD.UMC

The above paths are expensive. They're worth a bid, but we might also look for cheaper exposure through a high-to-higher path construction approach.