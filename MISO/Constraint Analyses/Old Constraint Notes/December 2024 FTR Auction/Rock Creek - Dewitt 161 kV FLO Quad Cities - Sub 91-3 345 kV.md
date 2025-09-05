---
aliases:
  - ROCK_CK-DEWITT
---
Last updated: 2024-11-08
### Basic Facts
**Monitored Element:**
- Common Name: Rock Creek - Dewitt
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: ROCK_CK_L2_5
- To Bus: DEWITT2 4417
**ISO(s):** [[MISO]], [[PJM]] (Cordova is a PJM bus)
- From Zone: [[Alliant West|ALTW]]
- To Zone: [[Alliant West|ALTW]]
**Nearby Landmarks:** Quad Cities; Davenport, IA
**For loss of:** CEMEC01
1. QUAD_SUB_934_1 1
    - Common Name: Quad Cities - Substation 91
    - Voltage: 345 kV
	- Equipment Type: Transmission line
    - From Bus: QUAD 1 3-11
    - To Bus: SUB_91
2. SUB_91 Q91_9T1
	- Common Name: Substation 91 Transformer 1
	- Voltage: 345/161 kV
	- Equipment Type: Transformer
	- From Bus: SUB_91
	- To Bus: SUB 91 5
**Direction Bound:** Forward; from Rock Creek to Dewitt
---
### History
Bound $45.6$ hours in RT from Oct. 28 - Nov. 7, 2024 at a $\$80.63/MWh$ average. Started binding during the evening load ramp on Oct. 28, suggesting a paradigm shift at this point in time.

---
### Drivers
**Topology:**
Cordova - Substation 39 345 kV has been out from 2024-10-27 (actual start) - 2024-11-10 16:00 (planned end). Note that this is a tie line between PJM (Cordova) and MISO (Substation 39). The constraint binds from East to West. With the Cordova - Sub 39 345 kV line out, Southward takeaway capacity from Quad Cities & Cordova is limited, leading to overloading Rock Creek - Dewitt.

**Generation:**
Quad Cities and Cordova Energy both push on the constraint.

**Load:**
Davenport, IA; Bettendorf, IA; Moline, IL, Rock Island, IL; East Moline, IL

**Commentary:**
There is tail risk that flows could reverse over the monitored element. During typically flow patterns, power flows Westward, yet Eastward flows have occurred on numerous occasions (both during summer and winter).

---
#### Line Rating Notes
Historically, Rock Creek - Dewitt 161 kV's post-contingent line rating is uprated on Nov. 1 from 219 MW to 251 MW. Despite the likely uprate on Nov. 1, the constraint has bound month-to-date at the time of this writing (11/8/2024).

---
### Forward View
The monitored element, Rock Creek - Dewitt 161 kV is scheduled to be on outage 2024-12-02 08:00 - 2024-12-11 17:00. After its return to service, the remainder of the Cordova - Substation 39 345 kV outage (through 12/15) is substantially bullish. The East Calamus - Dewitt 161 kV line outage 12/16 - 12/20 is substantially bearish, outweighing the bullish effects of the above for the five day window during which both outages are in effect.

The key consideration with the present constraint is the likelihood and impact of Westward flows reversing. Given the monitored element's outage and the Calamus - Dewitt 161 kV outage, the bullish effects of the Rock Creek - Dewitt 161 kV outage are heavily muted. For a month-long product, the risk/reward isn't attractive, particularly if outages slip. With that said, there appears to be a high likelihood that another constraint in the area will bind.