Last updated: 2025-05-14
#### Summary Characterization
Primarily driven by the Sarepta - Longwood 345 kV outage.
### Basic Facts
**Monitored Element:** COUCH__LEWISV3 A
- Common Name: Couch - Lewisville
- Voltage: 115 kV
- Equipment Type: line
- From Bus: 3COUCH%
- To Bus: 3LEWISVILLE#
- From Zone: EAI
- To Zone: EAI
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Texarkana, AR
**For loss of:** EECSW16
1. LAYFL_MTOL A
    - Common Name: Layfield - Mt. Olive
    - Voltage: 500 kV
	- Equipment Type: line
    - From Bus: LAYFLD8
    - To Bus: 8MT_OLIVE%
**Direction Bound:** from Couch to Lewisville

---
### Ratings, Flows, Generation, and Load
**Branch Ratings:** dynamic; ranging from 164 MW to 219 MW.

**Flow Bias:** bidirectional; Westward (from Couch to Lewisville) in the winter, Eastward (from Lewisville to Couch) in the summer. Perhaps slightly stronger in the Westward direction, but quite even.

**Transmission Outages:**
- Sarepta - Longwood 345 kV was heavily bullish.
- Carroll - Ringold 138 kV
- Johnco - Pittsburg 345 kV ([[SPP]] equipment)
- Kiowa - Pittsburg 345 kV ([[SPP]] equipment)
- Moss Bluff - Gillis 500 kV, Nelson area 500 kV

**Low-Side Generation:**
- Union Power Station (2.4 GW, NG CC)
- Hot Spring Generating Facility (715 MW, NG CC)
- Arkansas Nuclear One (1.84 GW, nuclear)
Low side generation is on the nearby 500 kV level.

**High-Side Generation:**
- Welsh (1.1 GW, subbituminous coal ST)
- Fulton (155 MW, NG GT)
- Narrows (25 MW, hydro WT)
- Turk (610 MW, subbituminous coal ST)

**Load:**

---
### Binding Events and Drivers
**J25**
- Sarepta - Longwood 345 kV outage.
- Valiant - Pittsburg - Johnston County 345 kV outages (cutting off Diamond Spring Wind and Kiamichi CC supply).
- Turk generation outage.

---
### Fair Value Modeling Notes
Sarepta - Longwood 345 kV outage is scheduled to end 5/15/2025. Once this outage ends, the risk of Couch - Lewisville binding drops significantly. We don't expect it to bind post-outage. The LEWISV_PATWX3 115 kV and FULTON_PAT_WX3 115 kV outages 5/5-5/10/25 are heavily bearish. As such, there are 9 days in K25 during which this constraint can bind.

---
### Sibling Constraints
- Couch - Lewisville 115 kV FLO Sarepta - Longwood 345 kV.
