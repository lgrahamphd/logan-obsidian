[[MISO]] has two different types of pricing nodes in its commercial model.
1. Elemental Pricing Nodes (EPNodes)
2. Commercial Pricing Nodes (CPNodes)
### EPNodes
*Elemental Pricing Nodes (EPNodes)* link the Commercial Model to the physical representation within the Network Model.

#### Types
EPNodes are grouped into three types:
1. Generation
2. Load
3. Non-Injection Non-Withdrawal (NINW)
### CPNodes
*Commercial Pricing Nodes (CPNodes)* are the financial settlement points for market participants.

#### Types
CPNodes represent aggregates of EPNodes. They are used to clear and settle MISO's energy market transactions. CPNodes are grouped into 13 types:
1. Generation Resource
2. DRR-Type I
3. DRR-Type II
4. Combined Cycle or Cross Compound Collection
5. Load Zone
6. External Interface
7. External Storage Resource (ESR)
8. Hub (ARR Zones are defined as the Hub type)
9. External Asynchronous Resource (EAR)
10. External Pseudo-Tied Generator (PSG)
11. External Pseudo-Tied Load (PSL)
12. AAR Zones
13. Storage as a Transmission-Only Asset (SATOA)

#### Naming Conventions
- At most 14 characters
- Includes the following information in order:
	1. NERC Registered Balancing Authority or Local Balancing Authority acronym
	2. A period "."
	3. Asset name of MP's choosing
		- CPNodes ending in ".AZ" are used exclusively by the FTR Market process.

---
### Model Relationships

![[MISO Network Model Relationships.png]]

---
### Commercial Model Hierarchy

![[MISO Commercial Model Hierarchy.png]]
---
### MISO Presentation
![[Introduction to EPNodes and CPNodes.pdf]]