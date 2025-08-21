Last updated: 2025-05-14
#### Summary Characterization
Transmission outage-driven. The entirety of IA, WI, NE, SD, ND, MN, MB are on the low side, and the high side is comprised of the locations listed in the load section.
### Basic Facts
**Monitored Element:** ST_JOCOOPE34_1 A
- Common Name: Cooper - St. Joe
- Voltage: 345 kV
- Equipment Type: line
- From Bus: COOPER 3 (SPP)
- To Bus: ST JOE 3 (SPP)
- From Zone: NPPD
- To Zone: MPS
**ISO(s):** [[MISO]], [[SPP]], [[AECI]]
**Nearby Landmarks:** Saint Joseph, MO
**For loss of:** MPS34002
1. SIBLEY_KETCH A
    - Common Name: Sibley - Ketchem
    - Voltage: 345 kV
	- Equipment Type: line
    - From Bus: SIBLEY 7 (SPP)
    - To Bus: KETCHEM7 (SPP)
**Direction Bound:** Southward from Cooper to St. Joe.

---
### Ratings, Flows, Generation, and Load
**Line Ratings:**
Static post-contingent rating of 1.195 GW, occasionally dropping to 1.185 GW.

**Flow Bias:**
Southward from Cooper to St. Joe 75% of the time.

**Low-Side Generation:**
- Cooper
- Nebraska City
- Monticello
- Prairie Island
- Wind generation to the North

**High-Side Generation:**
- Lake Road
- Iatan
- High Banks Wind Farm
- Irish Creek Wind Farm
- Soldier Creek Wind Farm

**Load:**
Kansas City, MO, and the entirety of AECI, Western MO, Western AR, OK, KS, the Shreveport, LA area, the Amarillo, TX area, the Lubbock, TX area, the College Station, TX area, and the extreme Southeast of NM.

---
### Binding Events and Drivers
Binds like clockwork when Cooper - Fairport 345 kV is out of service. This outage seems necessary for the constraint to bind.

**HJ25**
- Cooper - Fairport 345 kV outage.
**UV23**
- Cooper - Fairport 345 kV outage.
**UV22**
- Cooper - Fairport 345 kV outage.
**VX21**
- Cooper - Fairport 345 kV outage.

---
### Fair Value Modeling Notes
Worth looking at getting long this sometime in UX25 in case a Cooper - Fairport outage is taken.

---
### Highest Exposure Paths
MEC.FARMER -> CWLD.BLRG ~50% exposure.

---
### Sibling/Related Constraints
See Cooper - Fairport 345 kV FLO Sibley - Ketchem 345 kV, which is analogous.