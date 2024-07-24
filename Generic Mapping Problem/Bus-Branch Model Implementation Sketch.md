### `BusBranchModel` class
- Inherit from [NetworkX MultiDiGraph](https://networkx.org/documentation/stable/reference/classes/multidigraph.html)
- Nodes are `Bus` objects
- Edges are `Branch` objects
- `get_state_estimator_case` class method that returns an `SEBusBranchModel`, which inherits from `BusBranchModel`
---
### `Bus` class
- dataclass
##### Panorama Data
- Name
- Bus ID
	- Which? There are likely multiple bus IDs
- Base kV
- `SubStation`
- Unique ID
- `Generator` objects associated with the bus
- `Load` objects associated with the bus
- Pnode ID
- `ISO`
- `Zone`
- Area Name
- Zone Name
- Bus Type
---
### `Branch` class
- dataclass
##### Panorama Data
- Branch ID
	- Which? There are likely multiple branch IDs
- From Bus ID
- To Bus ID
- From Bus Name
- To Bus Name
- `Line` objects associated with the branch
- `Transformer` objects associated with the branch
- Status
- Outage Kind
- Memo
- Circuit
---
### `Substation` class
- dataclass
- `CircuitBreakers` associated with the substation
##### Panorama Data
- Station -- this is just a label
---
### `Line` class
- dataclass
- Inherits from `Branch`
##### Panorama Data
- r
- x
- b
- Rating A
- Rating B
- Rating C
---
### `Transformer` class
- dataclass
- Inherits from `Branch`
##### Panorama Data
- Transformer name
- x
- Windv1
- Nomv1
- Ang1
- Windv2
- Nomv2
---
### `Generator` class
- dataclass
##### Panorama Data
- Name
- Bus ID
- Memo
- Status
- Fuel
- pmin
- pmax
- qmin
- qmax
- Base MVA
---
