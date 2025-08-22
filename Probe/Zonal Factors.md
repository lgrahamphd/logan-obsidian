### Background
Probe takes as input a file `zonal_factors.csv`. This file provides definitions for bus aggregates. As an example, for each [[MISO LRZs|LRZ]], `zonal_factors.csv` contains the set of buses in the LRZ along with a weight for each bus. The sum of all bus weights in a given LRZ equals one. In this case, the *bus aggregate* is the LRZ. In addition to LRZs, `zonal_factors.csv` also provides definitions for hubs and various balancing authorities.

---
### Mapping between buses in Zonal Factors file and those in EMS model
The column `pnodeid` in `zonal_factors.csv` corresponds to the column `EMS Export PSS/E BUS #` in the `EPNodes` tab of the `MISO Commercial Model Posting Sep2024_final.csv` file (arbitrary month, year chosen).

---
### 18CHARGE example
#### EMS model
- 5 loads are incident to the 18CHARGE bus.
- Neither KETCHUM TB1 nor KETCHUM TB2 exist.

![[EMS_18CHARGE.png]]

#### IDC model
- A switched shunt is incident to the 18CHARGE bus.
- The buses KETCHUM TB1 and KETCHUM TB2 are adjacent to 18CHARGE. There is one load incident to each KETCHUM bus.

![[IDC_18CHARGE.png]]

#### MTEP model
- A switched shunt is incident to the 18CHARGE bus.
- The buses KETCHUM TB1 (260112), KETCHUM TB1 (260114), and KETCHUM TB2 (260113) are adjacent to 18CHARGE. There is one load incident to each KETCHUM bus.

![[MTEP_18CHARGE.png]]

#### Notes
- The `EMS to IDC Mapping Reference.csv` file has tabs for `Lines`, `Transformers`, `3-winding transformers`, and `Units`. There are no tabs for loads or buses. Moreover, if a given bus is in the IDC case but not the EMS case (e.g., one of the KETCHUM buses), then the corresponding equipment is omitted from the `EMS to IDC Mapping Reference.csv` file.