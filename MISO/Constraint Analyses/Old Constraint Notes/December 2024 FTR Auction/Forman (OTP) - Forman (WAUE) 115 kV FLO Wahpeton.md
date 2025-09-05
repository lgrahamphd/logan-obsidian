---
aliases:
  - FORMAN-FORMAN
---
Last updated: 2024-11-07
### Basic Facts
**Monitored Element:**
- Common Name: Forman (OTP) - Forman (WAUE)
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: FORMN 7 (MISO)
- To Bus: FORMAN 7 (SPP)
**ISO(s):** [[MISO]], [[SPP]]
- From Zone: [[Otter Tail Power Company|OTP]]
- To Zone: [[Western Area Power Administration, Upper Great Plains East|WAUE]]
**Nearby Landmarks:** Forman, ND; Wahpeton, ND
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
**Direction Bound:** Forward; from FORMN 7 (MISO) to FORMAN 7 (SPP)

#### Notes
The bus with unique ID `WAHPETN 9120` is the hub in a star bus meant to represent a 3-Winding Transformer. There is a second 3-Winding Transformer at the Wahpeton station as well.

##### Wahpeton 3WTR1
![[Wahpeton 3WTR1.png]]

##### Wahpeton 3WTR2
This three-winding transformer is associated with the bus WAHPTN 9120, which is featured in the above contingency definition.
![[Wahpeton 3WTR2.png]]

---
### History
Bound $227.9$ hours in RT from Oct. 1 - Nov. 6, 2024 at a $\$100.01/MWh$ average. Has bound a noteworthy amount since Sep. 9, 2024, suggesting a paradigm shift on that date.

---
### Drivers
**Topology:**
Lisbon - Enderlin 115 kV
- Out 2024-10-15 07:36 - ?
- Ross stated that this is a known switching solution. If Lisbon - Enderlin is closed, then another constraint will bind to an extreme degree.
- Bullish $12.6\%$ of Forman (OTP) - Forman (WAUE)'s line rating.

**Generation:**
Wind generation pushes on the constraint. The below are sorted in descending order by generation PTDF:
- [[Foxtail Wind Farm]] 150 MW
- [[Tatanka Wind Power]] 180 MW
- [[Merricourt Wind Project]] 150 MW
- [[Dakota Range Wind Project]] 1&2 300 MW
- [[Dakota Range Wind Project]] 3 154 MW
- [[Emmons-Logan Wind Farm]] 216 MW
- [[Crowned Ridge Wind Project]] 2 201 MW
- [[Crowned Ridge Wind Project]] 1 200 MW

**Load:**
[[Western Area Power Administration, Upper Great Plains East|WAUE]] load in SPP pulls on the constraint. PTDFs also suggest that SPC load and [[Otter Tail Power Company|OTP]] load also pull on the constraint (the constraint's sensitivity to these two load buckets is half that of its sensitivity to WAUE load).

**Commentary:**
Should Wahpeton - Hankinson 230 kV be lost, there is risk that wind generation overloads the monitored element. This includes wind generation West of the monitored element (Foxtail, Merricourt, Tatanka Wind Power, Emmons-Logan) as well as wind generation South of the constraint near [[Big Stone]] (Dakota Range, Crowned Ridge).

---
#### Line Rating Notes
Forman (OTP) - Forman (WAUE) 115 kV has seasonal line ratings. MISO and SPP state estimator data agree on the following:
- 126 MW from Apr. 1 - Oct. 31
- 131 MW from Nov. 1 - Mar. 31

---
### Forward View
From a topological perspective, the key question is if Lisbon - Enderlin 115 kV will remain on outage.

SPP's Fargo - Jamestown 230 kV Ckt 1 planned outage 2024-12-16 - 2024-12-20 is bearish by $4\%$ of the line rating. On 12/17, SPP's JAMESTN - BISMARK2 230 kV planned outage cancels out this bearish effect one-for-one.
