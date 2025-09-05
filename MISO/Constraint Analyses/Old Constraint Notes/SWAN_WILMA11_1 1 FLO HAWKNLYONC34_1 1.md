### Basic Facts
**Monitored Element:** WILMART 115KV - SWAN_LK 115KV
	- 115 kV line
**ISO:** [[MISO]]
	- NSP, NSP
**Contingency Name**: NSP34107
**For loss of:**
1. HAWKNLYONC34_1 1
	- 345 kV line

**Direction:** backward
**Constraint ID:** 417785
**History:**
- **DA**: has never bound for this contingency
- **RT**: bound for 3.2 hours from 23:00 hrs. on 9/1/2023 to 03:00 hrs. on 9/2/2023
	- $525.94 shadow price for HE 24 on 9/1
	- $974.05 shadow price for HE 1 on 9/2
	- $868.38 shadow price for HE 2 on 9/2
	- $440.30 shadow price for HE 3 on 9/2
	
### Drivers
**Topology**
HELENSHEAS34_1 1, MANKATEC TRG301, SHEASLK TR5, SHEASLK TR9, SHEASWILMA34_1 1, and WILMAMANKA34_1 1 were all on outage when the constraint bound.  These are in series 345 kV lines and in series 345/115 kV, 115/69 kV transformers. Should HAWKNLYONC34_1 1 be lost, then flows along the West -> East 345 kV corridor, which acts as takeaway capacity for wind generation, would flow into Wilmart from 345 kV lines, then step down to the 115 kV level and overload the monitored element.
### Forward View
HELENSHEAS34_1 is planned to be on outage from 8/12/2024-8/23/2024. This could put pressure on the monitored element SWAN_WILMA11_1. However, with the outage uncertainty on 345 kV lines Northeast of Brookings, SD, there are many variables interacting. 