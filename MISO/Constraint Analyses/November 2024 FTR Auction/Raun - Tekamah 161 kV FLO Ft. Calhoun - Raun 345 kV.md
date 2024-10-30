Last updated: 2024-10-15
### Basic Facts
**Monitored Element:** RAUN 161KV - TEKAMHO 161KV
- Common Name: Raun - Tekamah
- Voltage: 161 kV
- Equipment Type: Transmission line
- From Bus: RAUN 5
- To Bus: TEKAMAH5
**ISO(s):** [[MISO]], [[SPP]]; MEC is in MISO; OPPD is in SPP; monitored element is from MISO bus to SPP bus; contingency is from SPP bus to MISO bus
- From Zone: MEC (MISO)
- To Zone: OPPD (SPP)
**Nearby Landmarks:** Sioux City, IA
**For loss of:**
1. MECOPP1
    - Common Name: Fort Calhoun - Raun (from SPP to MISO)
    - Voltage: 345 kV
	- Equipment Type: Transmission Line
    - From Bus: FT_CAL
    - To Bus: RAUN
**Direction Bound:** Backwards; from Raun to Tekamah
---
### History
Bound for 91.3 hours in RT from Sep. 15 - Oct. 15, 2024 at a $\$58.54/MWh$ average. This was the #3 RT constraint over this period. Pleasant Lake - Leeds was the top RT constraint at $\$101.23/MWh$.

---
### Drivers
**Topology:**
- Tekamah - Oakland 115 kV outage (SPP equipment)
	- 2024-09-26 09:51 actual start, 2024-11-27 16:00 planned end
Tekamah - Oakland 115 kV provides the only East-to-West flow capacity along the 115 kV path from Raun to Northern Omaha. With Tekamah - Oakland 115 kV out, if Fort Calhoun - Raun 345 kV were to be lost to outage, the Raun - Tekamah5 - S1226 5 115 kV path would overload.

**Generation:**
George Neal North, George Neal South

---
#### Related Constraints
[[Tekamah - Substation 1226 161 kV FLO Ft. Calhoun - Raun 345 kV]]

---
#### Bearish Risks
Flows along the monitored element can reverse. Typically, flows are from North-to-South from Souix City, IA to Omaha, NE. As such, there does exist counterflow risk. See the 9/27/2024-9/28/2024 period, for example.

---
### Forward View
When flows are in their standard North-to-South pattern from Sioux City, IA to Omaha, NE, there is significant risk that Raun - Tekamah 161 kV FLO Ft. Calhoun - Raun 345 kV binds in November, 2024. The Tekamah - Oakland 115 kV outage is the key driver. Note also Tekamah - Substation 1226 161 kV FLO Fort Calhoun - Raun 345 kV and Tekamah - Oakland are in series.