Last updated: 2025-01-06
### Basic Facts
**Monitored Element:** WILMART TR9
- Common Name: Wilmarth TR9
- Voltage: 345/1 kV
- Equipment Type: 3-winding transformer
- From Bus: WILMART3
- To Bus: WILMART
- From Zone: [[Northern States Power Company|NSP]]
- To Zone: [[Northern States Power Company|NSP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Mankato, MN
**For loss of:** NSP34007
1. CRANDWILMA34_1 1
    - Common Name: Crandal - Wilmarth
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: CRANDAL 3
    - To Bus: WILMART3
**Direction Bound:** from the 345 kV level to the 1 kV level

---
### Drivers
**Topology:**
Wilmarth substation has a ring bus topology. As such, the Crandal - Wilmarth contingency leads to a split bus.

The 3-winding transformer is between WILMART3 (345 kV), WILMART7 (115 kV), and WILMART (13.8 kV). The present constraint has bound during time periods in which one of these three windings or the Mankato Energy Center - Wilmarth 345 kV is on outage.

![[Wilmarth node-breaker.png]]

**Generation:**
[[Mankato Energy Center]] 

**Line Ratings:**
Static 498 MW post-contingent branch rating that is subject to manual derates (e.g., Aug. 1-11, 2023) and uprates (e.g., July 4-22, 2022).

**Flow Bias:**
Flow direction oscillates, both up and down this 345/1 kV portion of the 3-winding transformer.

**Commentary:**
During the first week of January, 2025, two forced outages drove this constraint.

---
### Fair Value Modeling Notes
Closely investigate the risk of breaker, transformer, and line outages associated with Wilmarth substation and/or Mankato Energy Center.

---
### Highest Exposure Paths
