Last updated: 2024-11-10
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
Bound $24.9$ hours in RT from Oct. 1 - Nov. 9, 2024 at a $\$33.71/MWh$ average.

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
We see risk of this constraint continuing to bind in December in light of the persistent Sarepta - Longwood 345 kV line outage. This merits a close look for the purposes of the Dec. 24 auction.

Note that Minden - Ada 115 kV is scheduled to be out from 2024-11-25 09:30 - 2025-01-10 18:00. This is upstream of Sailes - Ringgold 115 kV (the path is Minden - Ada - Sailes - Ringgold). With this line out, Sailes has degree two: Sailes - Texas Eastern 115 kV and Sailes - Ringgold 115 kV. Flows along Sailes - Ringgold have been observed in equal proportions in both Southward and Northward directions.