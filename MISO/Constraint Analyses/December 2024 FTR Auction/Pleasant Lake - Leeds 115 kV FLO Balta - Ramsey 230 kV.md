Last updated: 2024-11-9
### Basic Facts
**Monitored Element:** PLESNLEEDS11_1
- Common Name: Pleasant Lake - Leeds
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: PLEASANT LK7
- To Bus: LEEDS 7
**ISO(s):** [[MISO]], [[SPP]]; Pleasant Lake - Leeds 115 kV is SPP equipment; Balta - Ramsey 230 kV is MISO equipment
- From Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
**Nearby Landmarks:**
**For loss of:** GRE23016
1. BALTARAMSE23_1 1
    - Common Name: Balta - Ramsey
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: GRE-BALTA 4
    - To Bus: GRE-RAMSEY 4
**Direction Bound:** Forward; from Pleasant Lake to Leeds
---
### History
Bound 139.1 hours in RT from Oct. 1 - Nov. 8, 2024 at a $\$60.63/MWh$ average.

---
### Drivers
**Topology:**
Branch rating decrease on 7/24/2024
- A and B summer ratings were originally 121 MW through 7/23/2024.
- A and B ratings both decreased to 61 MW from 7/24/2024-8/2/2024.
- A and B ratings both increased to 94 MW from 8/3/2024-10/1/2024 (the latest available SE case at the time of this writing).

Seasonal ratings changes started in 11/2020. From 2016-8/2020, A and B ratings were different. Thereafter, both ratings are the same. *Note that MISO's SE branch ratings are incorrect for this line, which is owned by SPP.*

Southward flows from Manitoba along PEACGRUGBY23_1 1 230 kV are upstream of the monitored element.

**Generation:**
- Rugby Wind Farm
- Coal Creek
- Border Winds Wind Farm

### Forward View
This constraint is driven by the line derate. It first bound immediately after the derate, and it's bound for a large portion of the hours thereafter. However, the line was uprated to 143 MW on Nov. 1. Since the uprate, there has been a marked decrease in the constraint's RT run rate, though it has continued to bind in the DAM albeit at slightly weaker shadow prices than pre-uprate. It seems plausible that the DA value should converge downwards to the RT value of the constraint while the Winter uprate remains in effect.