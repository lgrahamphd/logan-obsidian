Last updated: 2025-05-14
#### Summary Characterization
With Lisbon - Enderlin 115 kV out of service, Forman (OTP) - Forman (WAUE) 115 kV is a wind-transfer bottleneck from MISO to SPP in North Dakota. Note that Lisbon - Enderlin 115 kV is nearly always out; if it's in service, then Forman - Forman won't bind.
### Basic Facts
**Monitored Element:** FORMAFORMN11_1 1
- Common Name: Forman - Forman
- Voltage: 115 kV
- Equipment Type: line
- From Bus: FORMN 7
- To Bus: FORMAN 7
- From Zone: [[Otter Tail Power Company|OTP]] (MISO)
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]] (SPP)
**ISO(s):** [[MISO]], [[SPP]]
**Nearby Landmarks:** Forman, ND
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
**Direction Bound:** from FORMN 7 (MISO) to FORMAN 7 (SPP)

---
### Ratings, Flows, Generation, and Load
**Branch Ratings:**
Forman (OTP) - Forman (WAUE) 115 kV has seasonal line ratings
- 125 MW from Apr. 1 - Oct. 31
- 169 MW from Nov. 1 - Mar. 31

**Flow Bias:**
From MISO (OTP) to SPP (WAUE).

**Low-Side Generation:**
- [[Foxtail Wind Farm]] 150 MW
- [[Tatanka Wind Power]] 180 MW
- [[Merricourt Wind Project]] 150 MW
- [[Dakota Range Wind Project]] 1&2 300 MW
- [[Dakota Range Wind Project]] 3 154 MW
- [[Emmons-Logan Wind Farm]] 216 MW
- [[Crowned Ridge Wind Project]] 2 201 MW
- [[Crowned Ridge Wind Project]] 1 200 MW

**High-Side Generation:**
- FPL Energy North Dakota Wind (61 MW)
- Groton Generating Station (216 MW, NG, GT)

**Load:**
- Forman, ND

---
### Binding Events and Drivers
**J25**
- Lisbon - Enderlin 115 kV outage.
- Seasonal derate.
- High wind.

---
### Other Notes
The bus with unique ID `WAHPETN 9120` is the hub in a star bus meant to represent a 3-Winding Transformer. There is a second 3-Winding Transformer at the Wahpeton station as well.

##### Wahpeton 3WTR1
![[Wahpeton 3WTR1.png]]

##### Wahpeton 3WTR2
This three-winding transformer is associated with the bus WAHPTN 9120, which is featured in the above contingency definition.
![[Wahpeton 3WTR2.png]]
