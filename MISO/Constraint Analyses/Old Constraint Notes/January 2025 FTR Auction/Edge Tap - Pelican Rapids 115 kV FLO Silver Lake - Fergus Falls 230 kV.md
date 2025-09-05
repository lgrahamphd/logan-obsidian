Last updated: 2024-12-06
### Basic Facts
**Monitored Element:** PEL_REDGET11_1 1
- Common Name: Edge Tap - Pelican Rapids
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: PELICN N T7
- To Bus: EDGETAP7
- From Zone: OTP
- To Zone: OTP
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Pelican Rapids, MN
**For loss of:** OTP23016
1. SILVRFERGS23_1 1
    - Common Name: Silver Lake - Fergus Falls
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: GRE-SILVRLK4
    - To Bus: FERGSFL4
**Direction Bound:** Backwards; from Edge Tap to Pelican Rapids
---
### History
Last 30 days: 11/3/2024-12/2/2024
- RT Peak shadow price: $57.04/MWh; 14.8 hours bound
- RT Off-Peak shadow price: $86.48/MWh; 44.9 hours bound

---
### Drivers
**Topology:**
The Sheyenne - Lake Park 230 kV outage (2024-11-11 10:00 - 2024-12-13 17:00) is a key driver, accounting for increased flows over Edge Tap - Pelican Rapids 115 kV amounting to 20%+ of the line rating. Both Sheyenne - Lake Park 230 kV and Sheyenne TR6 are listed on the same outage ticket, Request ID: 1-27375411.

**Generation:**
Wind generation
Solar generation
- Hoot Lake Solar (50 MW) has a 23% generator shift factor on the monitored element.

**Load:**
Detroit Lakes, MN and Eastward; Brainerd, MN.

**Line Ratings:**
SE data indicate that line ratings appear to be static throughout the year.

**Commentary:**
Pelican Rapids - Tamarac 115 kV was on (unplanned) outage 2024-11-28 15:11 - 2024-11-29 09:56. With this out, the monitored element, Edge Tap - Pelican Rapids 115 kV becomes radial, and the constraint does not bind. It is out again (unplanned) at the time of this writing: 2024-12-02 04:41 - present.
12/6/2024 update: Pelican Rapids - Tamarac 115 kV was out 2024-12-02 04:41 - 2024-12-02 22:41 and 2024-12-03 05:11 - 2024-12-05 20:11.

Lakeswind (wind farm; 52 MW) has a -39% generator shift factor for the monitored element. Historically, the present constraint has bound even when Lakeswind was ran at pmax.

---
### Forward View
Merricourt - Wishek 230 kV is planned to be out 2025-01-06 10:00 - 2025-03-14 14:00. See Request ID: 1-27390590, whose status is currently marked as "Study." This line provides takeaway transmission capacity from [[Merricourt Wind Project]] (150 MW), [[Foxtail Wind Farm]] (150 MW), and [[Tatanka Wind Power]] (180 MW). When Merricourt - Wishek 230 kV is out and the three aforementioned wind farms are generating, we envision increased flows along the Twin Brooks - Oakes - Forman - Hankson - Wahpeton 230 kV path. A portion of this will push on the present constraint.

The Merricourt - Wishek 230 kV outage will change flow patterns in the region, likely bullish the present constraint. However, with Sheyenne - Lake Park 230 kV scheduled to return to service, the present constraint becomes less attractive. Our view is that there exists risk for the constraint to bind in January, but only a minimal amount of value should be assigned to it.

It's important to watch the Pelican Rapids - Tamarac 115 kV unplanned outage as well. Should this require a lengthy repair of some sort, then the present constraint cannot bind, but another constraint in the area likely would as a result.

---
### Highest Exposure Paths
Sources:
- OTP.OTPW_8.AZ
- OTP.HLSOLAR
Sinks:
- OTP.LAKESWIND
