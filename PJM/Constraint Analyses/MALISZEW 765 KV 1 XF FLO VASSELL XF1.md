### Basic Facts
**Monitored Element:**
- Voltage: 765/138 kV
- Equipment Type: Transformer
- From Bus: 05MALIS
- To Bus: MALISZE 2327
- Common Name: Maliszewski 765/138 kV Transformer
**ISO(s):** [[PJM]]
- From Zone: AEP
- To Zone: AEP
**Contingency Name**: 765/345.Vassell.T1
**For loss of:**
1. VASSELL XF1
    - Voltage: 765/138 kV
	- Equipment Type: Transformer
    - From Bus: 05VASSEL
    - To Bus: 05VASSEL
**Direction Bound:** forward
---
### History
**First Bound in RT:** 13:55 hrs. 6/13/2022
**Last Bound in RT:** 20:20 hrs. 8/27/2024

**Lifetime DA History**:
- Shadow Price: $\$5,698.08$
- Hours Bound: $58$
**Lifetime RT History**:
- Shadow Price: $\$44,099.03$
- Hours Bound: $35.3$
#### Selected Events
8/28/2024
- Constraint bound for $9.8$ hours (all on-peak) in RT at a $\$523.36/MWh$ 24-hour average.
- $1.99\%$ load shift factor for AD Hub
- $\$250.46$ aggregate impact to AD Hub
---
### Drivers
**Topology:**
The MAL-MAR1 1 (Maliszewski - Mary SVI2) 765 kV line is out due to an operational emergency. This outage began at 02:18 hrs. on 7/10/2024, and it is planned to end at 16:00 hrs. on 9/30/2024. MAL-MAR1 1 is adjacent to the monitored element.

In the Northern Columbus, OH area, there are two 765/138 kV transformers -- one at Maliszewski and the other at Vassell. Should the 765/138 kV transformer at Vassell be lost, flows from Guernsey along the 765 kV circuit will overload the the Maliszewski transformer. This risk is particularly prevalent with MAL-MAR1 1 out, which renders the Maliszewski substation radial on the 765 kV circuit. With MAL-MAR1 1 in service, it's possible for East-to-West flows from Guernsey along the 765 kV circuit to pass through Maliszewski to the 05MARYSV bus.

**Generation:**
Guernsey
- 3 unit natural gas combined cycle
- 2.055 GW

**Load:**
Columbus, OH.

---
### Forward View
With the MAL-MAR1 1 765 kV line outage to persist through 9/30/2024, risk persists that the considered constraint will bind. That said, such risk is contingent upon Columbus, OH load materializing. Once MAL-MAR1 1 returns to service, the risk of constraints binding on the Maliszewski 765/138 kV monitored element plummet.