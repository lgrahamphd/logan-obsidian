Last updated: 2024-09-13 10:00
### Basic Facts
**Monitored Element:**
- Voltage: 230 kV
- Equipment Type: Line
- From Bus: PLEASNT45850
- To Bus: 6ASHBURN
- Common Name: Pleasant View - Ashburn
**ISO(s):** [[PJM]]
- From Zone: DOM
- To Zone: DOM
**Contingency Name**: L230.GooseCreek-Ashburn-Beaumeade.227
**For loss of:**
1. ASHBURN-BEAUMEAD 227B
    - Voltage: 230 kV
	- Equipment Type: Line
    - From Bus: 6ASHBURN
    - To Bus: 6BEAMEAD
    - Comments: Part of a 230 kV double-circuit.
2. ASHBURN-GOOSECRE 227D
	- Voltage: 230 kV
	- Equipment Type: Line
	- From Bus: 6ASHBURN
	- To Bus: GOOSECR45726
	- Comments: Single-circuit in series with ASHBURN-BEAUMEAD double-circuit.
**Direction Bound:** Forward
---
### History
**Lifetime DA History**:
- First Bound in DA: 2024-02-12 11:00
- Last Bound in DA: 2024-09-13: 21:00
- Shadow Price: $\$12,991.93$
- Hours Bound: $328$

**Lifetime RT History**:
- First Bound in RT: 2024-02-12 11:00
- Last Bound in RT: 2024-09-12 16:55
- Shadow Price: $\$10,461.81$
- Hours Bound: $11.6$
#### Selected Events
2024-09-10 - 2024-09-12
- Constraint bound for $11.6$ hours (all on-peak) in RT at a $\$145.30/MWh$ 24-hour average.
- $-2.26\%$ load shift factor for Western Hub. $-\$3.29/MWh$ 24-hour average impact on Western Hub.
- Bound for 14 hours in the 2024-09-13 DAM, the first time at which it's bound in the DAM since 2024-08-28.
---
### Drivers
**Topology:**
The POL-SOJO 1 (Poland Road - Sojourner) 230 kV line is out due to new equipment cut-in construction. The outage began at 2024-09-03 08:43 and is scheduled to last until 2024-09-21 16:00.

The bottleneck arises at the juncture of 500 kV backbone transmission and the 230 kV transmission system in Eastern Loudoun and Western Fairfax Counties in Northern Virginia (near Dulles International Airport). The Northern VA load pocket in question draws from 500 kV North-to-South flows into the Goose Creek, Pleasant View, and (to a lesser extent) Brambleton substations. At the 500 kV voltage level, Pleasant View is radial and adjacent to Goose Greek. Brambleton and Goose Creek are also adjacent, and South-to-North flows at the 500 kV level from the former to the latter only strengthen Goose Creek's bottleneck effect. Each of the Goose Creek, Pleasant View, and Brambleton substations feature 500/230 kV transformers that step flows down to the 230 kV level, the singular voltage supporting the aforementioned load pocket.

Once 500 kV flows have stepped down to the 230 kV level at Goose Creek and Pleasant View, they flow along Goose Creek - Ashburn and Pleasant View - Ashburn, respectively, then along the 230 kV double-circuit Ashburn - Beaumeade. The contingency in the present constraint is the 230 kV series comprised of Goose Creek - Ashburn and one of the two Ashburn - Beaumeade lines. Should this 230 kV series be lost, then the Pleasant View - Ashburn - Beaumeade series (the latter with just one of its two lines in service) would become the primary route for North-to-South flows into the aforementioned load pocket (see also the Belmont Substation which is also adjacent to Goose Creek and Pleasant View and supports 230 kV transshipment).

If Poland Road - Sojourner were in service, then there would be more capacity to support South-to-North flows at the 230 kV level from Brambleton to the load pocket between Ashburn, Sterling, and Broadlands, VA. Indeed, shift factors indicate that the Poland Road - Sojourner outage is the greatest driver of additional flows on the monitored element.

**Generation:**
Stone Wall Energy Park
- 812 MW
- 2x1 NG CC
- Adjacent to the 6BELMONT bus associated with the BLMNTDOM substation.
- Panorama's mapping of EIA data looks to be off for this generator, so I cross-checked with EV.
Dickerson
- 326 MW
- 2 gas turbines still operating; 12 HR

In addition to the above, generation shift factors indicate that supply feeding onto the 500 kV system to the Northeast of the monitored element pushes on the constraint. Since large nuclear generators dominate the generation capacity that supplies this 500 kV system, the following plants push on the constraint:

[[Peach Bottom]]
- 2.876 GW
- 2 unit nuclear reactor
 [[Susquehanna]]
 - 2.532 GW
 - 2 unit nuclear reactor
[[Hope Creek]]
- 1.291 GW
- 1 unit nuclear reactor
[[Salem]]
- 2.34 GW
- 2 unit nuclear reactor
[[Limerick]]
- 2.277 GW
- 2 unit nuclear reactor

**Load:**
Northern VA load pocket in Eastern Loudoun and Western Fairfax Counties.

---
#### Impact on Western Hub
The present constraint is materially bearish with respect to Western Hub, given the corresponding $-\$2.29\%$ load shift factor. This is due to the fact that roughly one dozen of Western Hub's Pnodes in the Dickerson, Germantown, MD, and Northwestern Washington, D.C. area are on the low side of the present constraint, whereas the Dulles load pocket on the high side of the present constraint is not represented by any Pnodes in Western Hub's aggregate LMP definition.

---
### Forward View
The return of the Poland Road - Sojourner 230 kV line at 2024-09-21 16:00 can only weaken the constraint's shadow prices. However, I'm unconvinced that the return of this line alone will mitigate the constraint. Risk remains that the constraint will continue to bind. More analysis is needed to better understand the drivers given the complexity of this constraint.