Last updated: 2025-01-06
### Basic Facts
**Monitored Element:** HETINCENTP11_1 1
- Common Name: Hettinger - Centipede
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: HETINGR7
- To Bus: CENTIPED-UM7
- From Zone: [[Montana-Dakota Utilities Company|MDU]]
- To Zone: [[Montana-Dakota Utilities Company|MDU]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Hettinger, ND
**For loss of:** WAU23073
1. BOWMAHETIN23_1 1
    - Common Name: Bowman - Hettinger
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: HETINGR7
    - To Bus: CENTIPED-UM7
**Direction Bound:** from Hettinger to Centipede

---
### Drivers
**Topology:**
During the mid-September - mid-October, 2024 period, the constraint bound at a relatively high frequency. This aligned with the following outage cluster:
- FTTHONBND4_1 A
- FTTHOOAHE23_2 1
- NBEND_NBENDW A
- OAHE TR3
- OAHENBND_1 A
- OAHEOAHE14_2_O S
- OAHESULLY23_1 1
- PHILTOAHE23_1 1

With the above components out of service, flows through Oahe were forced to Maurine and, from there, Northward to Hettinger.

**Generation:**
Thunder Spirit Wind (155.5 MW) pushes on the constraint. The generator shift factor is 33.3. 

**Line Ratings:**
Since the September - October binding event, the post-contingent line rating uprated from 115 MW to 120 MW (at the start of November).

**Flow Bias:**
Hettinger -> Centipede is much more prevalent.

**Commentary:**
The conjunction of the Oahe-area outages and, secondarily, high output from Thunder Spirit led to the high binding rate during mid-September - mid-October.

---
### Fair Value Modeling Notes
Hettinger-Centipede is closely related to [[Maurine XF FLO Maurine - New Underwood 230 kV]]. After a brief investigation with Ross, we found a perplexing misalignment with MISO and SPP in which the Maurine XF constraint was binding in SPP, but not in MISO. This led to periods during which the Hettinger-Centipede bound, but the Maurine XF did not. That's notable, since we would expect the Maurine XF constraint to bind before Hettinger-Centipede.

---
### Highest Exposure Paths
Any expressions of a view on the present constraint needs to be considered in concert with an expression of a view on [[Maurine XF FLO Maurine - New Underwood 230 kV]].
