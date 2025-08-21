Last updated: 2024-12-09
### Basic Facts
**Monitored Element:** HIBRDMER_P11_1 1
- Common Name: High Bridge - Merriam Park
- Voltage: 115 kV
- Equipment Type: Transmission line
- From Bus: HIBRDGE7
- To Bus: MERIMPK7
- From Zone: [[Northern States Power Company|NSP]]
- To Zone: [[Northern States Power Company|NSP]]
**ISO(s):** [[MISO]]
**Nearby Landmarks:** Saint Paul, MN
**For loss of:** NSP11125
1. ROGRSHIBRD11_1 1
    - Common Name: Rogers Lake - High Bridge
    - Voltage: 115 kV
	- Equipment Type: Transmission line
    - From Bus: ROGRSLK7
    - To Bus: HIBRDGE7
	- *This is part of a 115 kV double circuit between Rogers Lake and High Bridge.*
**Direction Bound:** from High Bridge to Merriam Park
---
### History
Last 30 days: 2024-11-10 - 2024-12-09
- RT Peak shadow price: $6.63/MWh; 63.8 hours bound
- RT Off-Peak shadow price: $2.18/MWh; 39.4 hours bound

---
### Drivers
**Topology:**
ROGRSHIBRD11_2 1, which is the other line forming a double circuit with the contingency, was out 2024-11-18 08:21 - 2024-11-27 14:43.

**Generation:**
High Bridge (647 MW NG CC) pushes on the constraint.

**Load:**
Local load in Saint Paul, MN.

**Line Ratings:**
Post-contingent line ratings are uprated from 239 MW to 271 MW Dec. 1-2.

**Commentary:**
This constraint clearly bound as a result of the outage on the contingency's parallel circuit.

---
### Forward View
With the contingency's parallel circuit outage complete and only bearish planned outages present in January, there is minute risk that this constraint binds.

---
### Highest Exposure Paths
Sources:
- NSP.CC.HIBRDG1
Sinks:
- NSP.MERPK1

Latest MCPs are weak: $0.73/MWh for F25, $0.64/MWh for G25, $1.54/MWh for H25. It's unclear whether or not a short is worthwhile at these values.