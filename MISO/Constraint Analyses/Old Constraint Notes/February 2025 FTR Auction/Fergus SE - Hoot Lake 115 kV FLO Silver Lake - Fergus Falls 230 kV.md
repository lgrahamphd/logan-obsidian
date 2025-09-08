Last updated: 2025-01-09
### Basic Facts
**Monitored Element:** HOOT_FERS11_1 1
- Common Name: Hoot Lake - Fergus SE
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: HOOT_LK
- To Bus: FERGSFL7
- From Zone: [[Otter Tail Power Company|OTP]]
- To Zone: [[Otter Tail Power Company|OTP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Fergus Falls, MN
**For loss of:** OTP23016
1. SILVRFERGS23_1 1
    - Common Name: Silver Lake - Fergus Falls
    - Voltage: 230 kV
	- Equipment Type: Transmission line
    - From Bus: GRE-SILVRLK4
    - To Bus: FERGSFL4
**Direction Bound:** from Fergus SE to Hoot Lake

---
### Drivers
**Topology:**
During binding events in March-April, 2025, the MORRIGRANT11_1 1 and FRONTWAHPE23_1 1 outages were significantly bullish.
During the 2025-01-09 binding event, the Bison - Alexandria 345 kV outage was bullish.

**Generation:**
Hoot Lake Solar (50 MW) is on the high side.
Wind generation in OTP, WAUE, MDU is the key driver (along with the derates).

**Line Ratings:**
Derated from 132 MW to 112 MW on 2024-12-13. Uprated from 112 MW to 132 MW on 2024-12-17. Derated from 132 to 119 MW to 2024-12-18. Something odd is going on here.

**Flow Bias:**
From Fergus Falls to Hoot Lake.

**Commentary:**
At the 132 MW post-contingent line rating, a strongly bullish outage coupled with high wind generation seems to be necessary for the constraint to bind.

---
### Fair Value Modeling Notes
The Merricourt - Wishek 230 kV outage (2025-01-20 10:00 - 2025-03-14 14:00) looks to make bullish scenarios slightly more bullish.

Buffalo - Alice 115 kV (weekdays until end of February) is mildly bullish.
Ellendale - Ellendale Data 230 kV outage (2025-01-07 14:00 - 2025-06-06 02:00) is mildly bullish.

Wind generation is key -- particularly in OTP, WAUE, MDU.

---
### Highest Exposure Paths
This constraint is closely related to Hankinson - Wahpeton 230 kV. While the present constraint has bound at a higher run rate in recent history, there could be risk of Hankinson - Wahpeton 230 kV masking the present constraint. This needs to be taken into account when selecting paths.

OTP.OTPW_11.AZ -> OTP.HLSOLAR is cheap (-$0.44 Peak, $0.09 Off-Peak MCP for G25 as of the F25 auction). However, OTP.OTPW_11.AZ is on the high side of the Hankinson - Wahpeton 230 kV constraint, so we need to be careful of a scenario in which Hankinson - Wahpeton 230 kV masks Fergus SE - Hoot Lake. These MCPs seem somewhat undervalued; however, we need to keep costs low.

The Buffalo - Alice 115 kV outages (weekdays through end of G25) are bullish. So is the BIson - Alexandria 345 kV outage 2025-03-17 08:00 - 2025-03-26 23:59.

OTP.BEPC1 -> OTP.HLSOLAR is long both Fergus SE - Hoot Lake and Hankinson - Wahpeton. This comes at a (still potentially attractive) price: as of the F25 auction, the MCPs for G25 were $3.37 Peak, $3.58 Off-Peak.