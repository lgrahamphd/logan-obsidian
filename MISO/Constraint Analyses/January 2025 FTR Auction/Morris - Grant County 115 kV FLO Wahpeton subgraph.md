Last updated: 2024-12-02
### Basic Facts
**Monitored Element:** MORRIGRANT11_1 1
- Common Name: Morris - Grant County
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: MORRIS 7
- To Bus: GRANTCO7
- From Zone: OTP
- To Zone: OTP
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Wahpeton, ND
**For loss of:** OTP23100
1. WAHPEHANKS23_1 1
    - Common Name: Wahpeton - Hankinson
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: WAHPETON XF4
    - To Bus: HANKSON4
2. WAHPEWAHPE23_1 S
	- Common Name: Wahpeton XF4 - Wahpeton
	- Voltage: 230 kV
	- Equipment Type: Transmission line
	- From Bus: WAHPETN4
	- To Bus: WAHPETON XF4
3. WAHPETN  TR21
	- Common Name: Wahpeton Transformer 2-1
	- Voltage: 230/1 kV
	- Equipment Type: Transformer (part of a 3-Winding Transformer)
	- From Bus: WAHPETON XF4
	- To Bus: WAHPETN 9120
4. WAHPETN TR22
	- Common Name: Wahpeton Transformer 2-2
	- Voltage: 115/1 kV
	- Equipment Type: Transformer (part of a 3-Winding Transformer)
	- From Bus: WAHPETN7
	- To Bus: WAHPETN 9120
5. WAHPETN TR23
	- Common Name: Wahpeton Transformer 2-3
	- Voltage: 41.6/1 kV
	- Equipment Type: Transformer (part of a 3-Winding Transformer)
	- From Bus: WAHPETN 9120
	- To Bus: WAHPETN 9000
**Direction Bound:** Forward; from Morris to Grant County
---
#### Notes
The bus with unique ID `WAHPETN 9120` is the hub in a star bus meant to represent a 3-Winding Transformer. There is a second 3-Winding Transformer at the Wahpeton station as well.

##### Wahpeton 3WTR1
![[Wahpeton 3WTR1.png]]

##### Wahpeton 3WTR2
This three-winding transformer is associated with the bus WAHPTN 9120, which is featured in the above contingency definition.
![[Wahpeton 3WTR2.png]]

---
### History
Last 30 days: 11/3/2024-12/2/2024
- RT Peak shadow price: $18.89/MWh; 10.3 hours bound
- RT Off-Peak shadow price: $4.39/MWh; 7.5 hours bound
---
### Drivers
**Topology:**

**Generation:**
- [[Dakota Range Wind Project]] (Phases 1 & 2, 300 MW; Phase 3, 154 MW)
- [[Crowned Ridge Wind Project]] (Phase 1, 200 MW; Phase 2, 201 MW)
- [[Big Stone]] (450 MW)
- [[Palmer's Creek Wind Farm]] (45 MW)

**Load:**
- Fergus Falls, MN
- Alexandria, MN

**Line Ratings:**
Morris - Grant County 115 kV's post-contingent line rating was uprated from 132.7 MW to 166.7 MW on 11/15/2024. This seasonal uprate should persist until 4/1/2025. The present constraint has not bound in RT since the uprate. It bound in the DAM for two days after the uprate, the last hour of which was HE 2 on 11/17/2024.

It appears that Morris - Grant County 115 kV was worked on between Feb. and April, 2024. The line was on outage during this time window, and afterwards, the summer post-contingent rating increased 29.7 MW. The latest SE data which reveal a new winter post-contingent rating of 166.7 MW (up from 140 MW in previous winters) as well.

**Commentary:** Appears to be positively correlated with [[Edge Tap - Pelican Rapids 115 kV FLO Silver Lake - Fergus Falls 230 kV]].

---
### Forward View
The uprate decreases the likelihood of the present constraint binding. However, should strong Northward flows materialize (due to high demand due to cold weather and/or high wind generation), then the constraint could bind.

---
### Highest Exposure Paths
Source:
- OTP.BENSON.ARR
Sink:
- OTP.GRANTCO