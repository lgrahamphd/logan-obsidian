Last updated: 2025-05-14
#### Summary Characterization
This constraint arises due to a voltage step-down bottleneck from the 345 kV level to the 161 kV level. Wind-driven. Coal generation also pushes on the constraint. Gas generation is on the high side.
### Basic Facts
**Monitored Element:** NASHUA T1_H
- Common Name: Nashua Transformer
- From Bus: NASHUA 7
- To Bus: NASHUA
- From Zone: KCPL
- To Zone: KCPL
**For loss of:** KCP34102
1. NASHUA_HAWTH A
    - From Bus: NASHUA 7
    - To Bus: HAWTH 7
**Direction Bound:** from Nashua to Hawthorn

---
### Ratings, Flows, Generation, and Load
**Line Ratings:**
Static post-contingent line rating of 715 MW.

**Flow Bias:**
Exclusively down the transformer from 345 kV -> 1 kV -> 161 kV.

**Low-Side Generation:**
- Cooper (SPP)
- Iatan (SPP)
- Nebraska City (SPP)
- Lake Road (SPP)
- High Banks Wind Farm (SPP)
- Irish Creek Wind Farm (SPP)
- Soldier Creek Wind Farm (SPP)
- Clear Creek Wind (AECI)
- White Cloud Wind (AECI)

**High-Side Generation:**
- Hawthorn (SPP)
- Quindaro (SPP)
- Nearman Creek (SPP)

**Load:**
- Kansas City
- Meta data center (750 MW load; to be completed in late 2025, roughly)
---
### Binding Events and Drivers
**FG25**
- Stranger Creek - 87th Street 345 kV outage.
- Craig XF #11 345/161 kV outage.
**UV24**
- Stranger Creek - 87th Street 345 kV outage.
**Z24**
- Stranger Creek - 87th Street 345 kV outage.
---
