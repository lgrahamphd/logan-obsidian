Last updated: 2025-05-14
#### Summary Characterization
Transmission-outage driven.
### Basic Facts
**Monitored Element:** COCODR1 AUT1
- Common Name: Cocodrie - Coughlin XF 1
- Voltage: 230/138 kV
- Equipment Type: transformer
- From Bus: COCODR 6
- To Bus: COUGH 4
- From Zone: CLEC
- To Zone: CLEC
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Saint Landry, LA
**For loss of:** CLC13053
1. COCDR_COUGH_A2
    - Common Name: Coughlin-Coughlin
    - Voltage: 138 kV
	- Equipment Type: line
    - From Bus: COUGH 4
    - To Bus: COUGLN
2. COCDR1 AUT2
    - Common Name: Cocodrie - Coughlin XF 2
    - Voltage: 230/138 kV
	- Equipment Type: transformer
    - From Bus: COCODR 6
    - To Bus: COUGH 4
**Direction Bound:** Down the transformer from the 230 kV level to the 138 kV level.

---
### Ratings, Flows, Generation, and Load
**Branch Ratings:**
Static post-contingent branch rating of 425 MW. Note that transformer 2 has a post-contingent branch rating of 478 MW.

**Flow Bias:**
Down the transformer.

Whenever the Cocodrie - Ville Platte - West Fork 230 kV path has outages, there's risk that this binds.

**Low-Side Generation:**
- 470 MW of Coughlin capacity at the 230 kV level

**High-Side Generation:**
- Prairie Ronde Solar Farm (135 MW; online Nov. 2024)
- Elizabeth Solar Plant (143 MW; online Aug. 2024)
- 285 MW of Coughlin capacity at the 138 kV level

**Load:**
- Central Louisiana 138 kV system.

**Commentary:**
- Coughlin (923? MW, NG, CC)
	- 285 MW at the 138 kV level (COUGLN bus)
	- 470 MW at the 230 kV level (COCODR 6 bus)
	- Huh... these sum to 755 MW...
 
There are parallel 230/138 kV transformers and parallel Coughlin - Coughlin 138 kV lines in series with the transformers. The contingency takes out one of these two transformer-line paths.

---
### Binding Events and Drivers
**U23**
- Cocodrie - Ville Platte 230 kV outage (9/20-9/21/23 binding event).
- Ville Platte - West Fork 230 kV outage (9/11/23 binding event).

---
### Sibling/Related Constraints
