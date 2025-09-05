Last updated: 2024-12-09
### Basic Facts
**Monitored Element:**
- Common Name: Sailes - Ringgold
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: 3RINGGOLD_LA
- To Bus: SAILES
**ISO(s):** [[MISO]], [[SPP]]; the outage Sarepta - Longwood, which drives the constraint, is a MISO - SPP tie line.
- From Zone: EES
- To Zone: EES
**Nearby Landmarks:** Shreveport, LA
**For loss of:** CLC23039
1. LYFLD_CAROL A
    - Common Name: Layfield - Carroll
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: 6LAYFLD
    - To Bus: CARROLL6
**Direction Bound:** Backward; from Sailes to Ringgold
---
### History
Last 30 days: 2024-11-10 - 2024-12-09 bound for a total of 0.3 hours. The sibling constraint, with contigency EECSW16 (Mt. Olive - Layfield 500 kV) bound 0.6 hours.

---
### Drivers
**Topology:**
The MISO - SPP tie line Sarepta (MISO) - Longwood (SPP) 345 kV has been out (urgent priority) since 2024-9-23 10:16 - 2025-05-15 planned end. This line, together with the monitored element, Layfield - Carroll 230 kV, provides key East-to-West transmission capacity from the nearby 500 kV backbone transmission system. With Sarepta - Longwood 345 kV out, loss of Layfield - Carroll 230 kV leads to a bottleneck for East-to-West flows from higher voltages to lower voltages.

Note that flows along Sarepta - Longwood 345 kV can flip between East-to-West and West-to-East patterns. As such, the Sarepta - Longwood 345 kV outage has been *bearish* for the present constraint at times (though the outage has been bullish more often and to a greater degree).

*Outage deep dive:*
- SPP outage with CROW ID 1-00477210.
	- Since the ticket includes both the Longwood - Sarepta line and the Longwood disconnect switch (AEP in SPP), it stands to reason that this is an SPP project, not a MISO project.
- Actual start: 2024-09-23 08:55
- Planned end: 2025-05-15 16:00
	- MISO's listed planned end date -- 2024-12-31 -- appears to be incorrect.
- SPP named the facility (line) "Longwood - Sarepata 345kV," but the town is "Sarepta, LA" (without the "a" between the "p" and "t.")
- AEP refers to the line as "Longwood - El Dorado," but El Dorado is a separate bus adjacent to and to the Northeast of Sarepta.
- ![[NorthwestLouisiana_Factsheet_V6.pdf]]
---
### Forward View
In light of the persistent Sarepta - Longwood 345 kV line outage, we see opportunity to exploit the facts that Longwood - Sarepta 345 kV is not in the MISO ftr model (it's an SPP outage, and MISO has the wrong dates).

Note that Minden - Ada 115 kV is scheduled to be out from 2024-11-25 09:30 - 2025-01-10 18:00. This is upstream of Sailes - Ringgold 115 kV (the path is Minden - Ada - Sailes - Ringgold). With this line out, Sailes has degree two: Sailes - Texas Eastern 115 kV and Sailes - Ringgold 115 kV. Flows along Sailes - Ringgold have been observed in equal proportions in both Southward and Northward directions.

Moreover, Ada - Sailes 115 kV is schedule to be out from 2025-01-13 08:00 - 2025-01-31 18:00.

It's critical that we construct a path that still binds in the presence of the Ada - Minden and Ada - Sailes outages.

Note also that the monitored element, Layfield - Carroll 230 kV, is scheduled to be out 2025-01-06 10:00 - 2025-01-10 18:59.

---
### Highest Exposure Paths
Sources:
- EAI.ELDORA.ARR
Sinks:
- CLEC.DPS.ARR
- CLEC.CPWR_6.AZ