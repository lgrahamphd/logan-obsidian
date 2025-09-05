Last updated: 2025-09-03
#### Summary Characterization
With Lisbon - Enderlin 115 kV out of service, Forman (OTP) - Forman (WAUE) 115 kV is a wind-transfer bottleneck from MISO to SPP in North Dakota. Note that Lisbon - Enderlin 115 kV is normally open; if it's in service, then Forman - Forman won't bind.

---
#### Necessary Conditions for Binding Events
- Moderate wind generation in ND
- Lisbon - Enderlin 115 kV OOS

---
### Basic Facts
**Monitored Element:** FORMAFORMN11_1 1
- Common Name: Forman - Forman
- From Bus: FORMN 7 115 kV
- To Bus: FORMAN 7 115 kV
- From Zone: [[Otter Tail Power Company|OTP]] (MISO)
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]] (SPP)
**For loss of:** OTP23100
1. WAHPEHANKS23_1 1
    - From Bus: WAHPETON XF4
    - To Bus: HANKSON4
2. WAHPEWAHPE23_1 S
	- From Bus: WAHPETN4
	- To Bus: WAHPETON XF4
3. WAHPETN  TR21
	- From Bus: WAHPETON XF4
	- To Bus: WAHPETN 9120
4. WAHPETN TR22
	- From Bus: WAHPETN7
	- To Bus: WAHPETN 9120
5. WAHPETN TR23
	- From Bus: WAHPETN 9120
	- To Bus: WAHPETN 9000
**Direction Bound:** from FORMN 7 (MISO) to FORMAN 7 (SPP)

---
### Ratings, Flows, Generation, and Load
**Branch Ratings:**
Forman (OTP) - Forman (WAUE) 115 kV has seasonal line ratings
- 125 MW from Apr. 1 - Nov. 1
- 169 MW from Nov. 1 - Apr. 1

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
**J25, V24**
- Lisbon - Enderlin 115 kV outage.
- Seasonal derate.
- High wind.
