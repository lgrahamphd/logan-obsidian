Last updated: 2025-05-14
#### Summary Characterization
Driven by Southward wind transfer and bullish constraints.

MISO lacks the ability to dispatch impactful generation on the constraint's high side, as these units are in SPP's footprint. Should MISO overestimate how much SPP will dispatch Iatan and Lake Road and underestimate wind curtailment in the relevant areas in SPP, then MISO might error on the side of under-curtailing the wind generation that pushes on the constraint.
### Basic Facts
**Monitored Element:** 11303 A
- Common Name: Maryville - Midway
- Voltage: 161 kV
- Equipment Type: line
- From Bus: MIDWAY_5
- To Bus: MARYVLE5
- From Zone: MPS (SPP)
- To Zone: MPS (SPP)
**ISO(s):** [[MISO]], [[SPP]]
**Nearby Landmarks:** Maryville, MO; North of St. Joe, MO
**For loss of:** MPSNPP01
1. ST_JOCOOPE34_1 A
    - Common Name: St. Joe - Cooper
    - Voltage: 345 kV
	- Equipment Type: line
    - From Bus: COOPER 3
    - To Bus: ST JOE 3
**Direction Bound:** Southward from Maryville to Midway.

---
### Ratings, Flows, Generation, and Load
**Line Ratings:**
- Winter (Dec. 1 - Mar 31): 204 MW post-contingent
- Summer (June 1 - Sep. 30): 180 MW post-contingent
- Intermediate rating? (April 1 - May 31, Oct. 1 - Nov. 30): 192 MW post-contingent

**Flow Bias:**
Southward from Maryville to Midway 80% of the time.

**Transmission Outages:**
- Creston - Maryville 161 kV
- Cooper - Fairport 345 kV

**Low-Side Generation:**
- Clear Creek Wind Farm (242 MW)
- White Cloud Wind Project (236 MW)
- Adams (MidAmerican) Wind Farm (150 MW)
- Contrail Wind Farm (112 MW)
- Conception Wind Project (50 MW)
- Nodaway (316 MW, NG, GT)
- Bluegrass Ridge Wind Farm (57 MW)

Even when it's windy, if Clear Creek and/or White Cloud (both [[AECI]] wind farms) and/or Contrail ([[MidAmerican Energy Company|MEC]] wind farm) are curtailed, then constraints defined on Maryville - Midway might not bind.

**High-Side Generation:**
- Lake Road (230 MW NG ST; 43 MW Oil CT); SPP plant
- Iatan (1.6 GW, subbituminous coal, ST); SPP plant
- Soldier Creek Wind (300 MW); SPP wind farm
- Irish Creek Wind (300 MW); SPP wind farm
- High Banks Wind (643 MW); SPP wind farm

**Load:**
- St. Joseph, MO
---
### Binding Events and Drivers
**J25**
- Fairport - St. Joe 345 kV outage.
- High wind.
- Southward flows.

---
### Sibling Constraints
Maryville - Midway 161 kV FLO Fairport - Gentry - Nodaway 161 kV
- At least equally as prominent as the St. Joe - Cooper 345 kV contingency.
- Binds more often in DA and RT than the St. Joe - Cooper 345 kV contingency.
Maryville - Midway 161 kV FLO Nodaway - Maryville 161 kV
- Strongest historical performance in the family of Maryville - Midway constraints.
- Was particularly strong from 2020-2023.
