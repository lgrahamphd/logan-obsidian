### Basic Facts
**Monitored Element:** AURORA_BROOKNG A
- Voltage: 115 kV
- Equipment Type: Line
- From Bus: AURORA 7
- To Bus: BROOKNG 7
- Common Name: Aurora - Brookings
**ISO(s):** [[MISO]], [[SPP]]
- SPP equipment
- From Zone: WAU WAUE
- To Zone: WAU WAUE
**Contingency Name**: NSPWAU10
**For loss of:**
1. SPLT_WHITE34_1 1
    - Voltage: 345 kV
	- Equipment Type: Line
    - From Bus: SPLT RK3
    - To Bus: WHITE 3
**Direction Bound:** forward
**Constraint ID:** 377193
**History:**
- Interval Considered: 8/1/2024-8/27/2024 (present)
- **DA**:
	- $\$23.11/MWh$
	- Hours Bound: 97
		- Peak: 57
		- Off-Peak: 40
- **RT**:
	- $\$40.64/MWh$
	- Hours Bound: 40
		- Peak: 27.3
		- Off-Peak: 13.7
### Drivers
**Topology:**
- BS1_GEN1 - LYON CO 3 345 kV line is on outage from 5/31/2024 - 9/30/2024
- HAWKSNEST 3 - BRKNGCO3 345 kV line is out of service (since 5/31/2024).

With these 345 kV lines out, key takeaway capacity is lacking from the below generation. White - Split Rock is the only North-South 345 kV transmission line in the area, providing a route for power to flow from the generation pocket to the Northeast of Brookings, SD to Sioux Falls, SD. Should White - Split Rock be lost, then North-South flows would overload the monitored element.

**Generation:**
- Buffalo Ridge, Buffalo Ridge 1, Buffalo Ridge 2
	- Wind
	- 300 MW
- Coyote Ridge
	- Wind
	- 100 MW
- Tatanka Ridge
	- Wind
	- 150 MW
- Blazing Star 1, Blazing Star 2
	- Wind
	- 200 MW
	- Currently radial; future West-to-East takeaway capacity to Hawk's Nest/Lyon CO 3 will ameliorate this situation
- Astoria
	- Gas
	- GT
	- 350 MW
- Deer Creek Station
	- Gas
	- CC
	- 324 MW
	
**Load:**
Sioux Falls, SD
#### Related Constraints
In series with WHITE_BROOKNGS A FLO WATERTOWN-WHITE_345.
### Forward View
Stepp Bank Lake - Lyon CO 345 kV (LYONCSTPBN34_1) is expected to enter service 9/30/20204. This will provide West-to-East takeaway capacity from Blazing Star wind farm. Even still, with Southeast-Northwest flows from BRKNGCO3 to WHITE 3 along WHITEBRKNG_34_1 1 and WHITEBRKNG_34_2 1 (which is common, though not ubiquitous, when the West-to-East 345 kV circuit is closed), loss of White - Split Rock 345 kV poses significant risk of overloading the monitored element.