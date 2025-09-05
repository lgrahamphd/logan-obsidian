Last updated: 2024-11-12
### Basic Facts
**Monitored Element:**
- Common Name: Maryville - Midway
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: MIDWAY_5
- To Bus: MARYVLE5
- From Zone: MPS
- To Zone: MPS
**ISO(s):** [[MISO]], [[SPP]], AECI; Maryville - Midway 161 kV is an SPP line; Nodway - Gentry - Fairport is a path comprised of AECI equipment
**Nearby Landmarks:** borders of Missouri, Nebraska, and Iowa
**For loss of:** AEC16011
1. GENTRY-FAIRPT A
    - Common Name: Gentry - Fairport
    - Voltage: 161 kV
	- Equipment Type: Transmission line
    - From Bus: 5GENTRY
    - To Bus: 5FAIRPTB2
2. GENTRY-NODAWY A
    - Common Name: Gentry - Nodway
    - Voltage: 161 kV
	- Equipment Type: Transmission line
    - From Bus: 5GENTRY
    - To Bus: 5NODWAY
**Direction Bound:** Backwards; from Maryville to Midway
---
### History
Bound $213$ hours in RT from Oct. 13 - Nov. 11, 2024 at a $\$29.16/MWh$ average.
In SPP, this constraint has bound for only $2$ hours in RT at a $\$0.15/MWh$ average over the same period.

---
### Drivers
**Topology:**
Clarinda - Hastings 161 kV has been out since 2024-11-1, and its outage is planned to end on 2024-12-15.

Northboro - Orient 345 kV is planned to be out of service 2024-12-2 07:00 - 2024-12-20 15:00.
- Takeaway capacity from Orient Wind Farm (400 MW).
- Downstream of Rolling Hills Wind Farm (484 MW) and Southern Hills Wind Farm (254 MW).

SPP line Cooper NPPD - S3458 345 kV has been out since 2024-9-24 09:28, and its outage is planned to end 2024-12-20 14:30.
- Takeaway capacity from Cooper (nuclear-fired, 801 MW) to St. Joseph, MO.
SPP line Cooper NPPD - St. Joe 345 kV has been out since 2024-11-18 08:00, and its outage is planned to end 2024-12-6 16:00.
- Takeaway capacity from Cooper (nuclear-fired, 801 MW) to Omaha, NE.

AECI line Creston - Maryville 161 kV has been out since 2024-10-21, and its outage is planned to end 2025-3-21. The standard flow bias is from Maryville to Creston (from the Southwest to the Northeast). With this line out, flows from White Cloud Wind Project, Clear Creek Wind Farm, and Conception Wind Farm put more pressure on the constraint.

**Generation:**
Sizable wind generation capacity pushes on this constraint.
- Clear Creek Wind Farm (230 MW)
- White Cloud Wind Project (236 MW)
- Adams (MidAmerican) Wind Farm (150 MW)
- Contrail Wind Farm (112 MW)
- Conception Wind Project (50 MW)

**Load:**
St. Joseph, MO, Lee's Summit, MO.

**Commentary:**
Lake Road (NG peaker, 231 MW) and Iatan (Subbituminous coal, 1.584 GW) are on the high side of the constraint.

---
#### Line Rating Notes
Historically, the post-contingent rating on Maryville - Midway 161 kV uprates on Oct. 1 from 180 MW to 192 MW and on Dec. 1 from 192 MW to 204 MW.

---
### Forward View
With the impactful outages listed above and the clear exposure to high wind generation, this constraint seems likely to bind in December, particularly in the first half of the month.

Historically, flows have occasionally reversed along Maryville - Midway 161 kV to flow Northward. When this is the case, the aforementioned transmission outages become bearish for the present constraint. However, with these Northward flows, the Eastowne - Iatan 345 kV outage (12/9 - 12/20) is bullish for the present constraint. This mutes the risk of a flow reversal.

---
### Related Constraints
Braddyville - Maryville 161 kV FLO Cooper - Fairport - St. Joe 345 kV and Fairport XF3. Braddyville - Maryville 161 kV is in series with Maryville - Midway 161 kV, closer to the Contrail Wind Farm bus (on which the MEC.CONTRAIL1 CPnode is defined).