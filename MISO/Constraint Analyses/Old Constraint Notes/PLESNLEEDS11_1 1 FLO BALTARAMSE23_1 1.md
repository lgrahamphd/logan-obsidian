### Basic Facts
**Monitored Element:** PLESNLEEDS11_1 1
- Voltage: 115 kV
- Equipment Type: Line
- From Bus: PLEASANT LK7
- To Bus: LEEDS 7
- Common Name: Pleasant Lake - Leeds
**ISO(s):** [[MISO]], [[SPP]]; SPP equipment
- SPP equipment
- From Zone: WAU, WAUE
- To Zone: WAU, WAUE
**Contingency Name**: GRE23016
**For loss of:**
1. BALTARAMSE23_1 1
    - Voltage: 230 kV
	- Equipment Type: Line
    - From Bus: GRE-BALTA 4
    - To Bus: GRE-RAMSEY 4
**Direction Bound:** Forward
**Constraint ID:** 455851
**History**
- Interval Considered: 8/1/2024-8/27/2024 (present)
- **DA**:
	- $\$100.94/MWh$
	- Hours Bound: 542
		- 252 Peak
		- 290 Off-Peak
- **RT**:
	- $\$72.41/MWh$
	- Hours Bound: 74.8
		- 46.4 Peak
		- 28.3 Off-Peak
### Drivers
**Topology:**
Branch rating decrease on 7/24/2024
- A and B summer ratings were originally 121 MW through 7/23/2024.
- A and B ratings both decreased to 61 MW from 7/24/2024-8/2/2024.
- A and B ratings both increased to 94 MW from 8/3/2024-8/27/2024 (present, inferred).

Seasonal ratings changes started in 11/2020. From 2016-8/2020, A and B ratings were different. Thereafter, both ratings are the same. *Note that MISO's SE branch ratings are incorrect for this line, which is owned by SPP.*
### Forward View
There is a high level of risk that this constraint will continue to bind as long as the derate persists. Branch flows on the monitored element have remained typical (slightly below average, in fact) during the period in which the constraint has bound.

Moreover, the constraint first bound immediately after the derate, and it's bound for a large portion of the hours thereafter.

Follow-up analysis on the nature of the derate is needed.