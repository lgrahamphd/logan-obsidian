Last updated: 2024-12-05
### Basic Facts
**Monitored Element:** HAYWARD TR1
- Common Name: Hayward TR1
- Voltage: 161/69 kV
- Equipment Type: Transformer
- From Bus: HAYWARD_L1_5
- To Bus: HAYWARD_J1_8
- From Zone: [[Alliant West|ALTW]]
- To Zone: [[Alliant West|ALTW]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Albert Lea, MN
**For loss of:** ALW16068
1. ADAMSHAYWA16_1 1
    - Common Name: Adams - Hayward
    - Voltage: 161 kV
	- Equipment Type: Transmission line
    - From Bus: ADAMS 5
    - To Bus: HAYWARD_L1_5
**Direction Bound:** Forward; downward in voltage from 161 kV to 69 kV
---
### History
Last 30 days: 11/6/2024-12/5/2024
- RT Peak shadow price: $24.23/MWh; 9.3 hours bound
- RT Off-Peak shadow price: $1.82/MWh; 1.4 hours bound
---
### Drivers
**Topology:**
The conjunction of the Murphy Creek - Hayward 161 kV and Glenworth - Hayward 161 kV outages leave Adams - Hayward and Freeborn - Hayward the only 161 kV lines incident to Hayward. See Request ID: 1-27245216, which refers to both outages. These outages started 2024-09-16 09:26, and they are scheduled to end 2024-12-20 11:00.

**Generation:**
Bent Tree Wind Farm pushes on the constraint. Freeborn Wind Farm relieves the constraint.

**Load:**
Albert Lea, MN at the 69 kV level.

**Line Ratings:**
Static at 72 MW.

**Commentary:**
The choice of the contingency mixed with the fact that the monitored element is a transformer are clues that the issue is getting flows to step down to the 69 kV level to supply Albert Lea, MN.

---
### Forward View
We expect this constraint to bind should Albert Lea, MN receive cold weather while the two 161 kV lines are out (as mentioned above, the outages last until 2024-12-20 11:00). We can't argue for a long position in January 2025. A counterflow position could be attractive if the market overpays for the recency bias, though we don't necessarily think that this will happen.

With that said, until 2024-12-20 11:00, this could be an attractive play via virtuals if one could secure cheap exposure via INCs at ALTW.BENT_TREE or DECs at ALTW.NSP or potentially ALTW.WELLS1 when load in Southern MN is forecast to be high.

---
### Highest Exposure Paths
Sources:
- ALTW.BENT_TREE
Sinks:
- ALTW.NSP
- ALTW.WELLS1