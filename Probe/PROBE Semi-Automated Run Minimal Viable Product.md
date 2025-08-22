## Workflow
1. Automated job that runs the `write_probe_input.py` script.
2. Ingest fuel price marks from somewhere (Britt?).
3. Manually run PROBE on the generated input. I'd recommend serial mode at first to keep things as simple as possible.
4. Use the dashboard tool to inspect the output `.db` file.

---
## Biggest Missing Pieces
1. Code that writes generator outages and derates. I can't seem to get derates to work via overrides, which is the method recommended by both Jim and the Probe documentation.
2. Automated approach for writing the monitored elements file.
3. Code that writes the loop flows file. I am unfamiliar with how we could generate this.
4. Revamp the commercial flowgate file writer. We have to use bus names to map, and this creates difficulties and dropped data (which my logger notes).
5. Custom reporting layer.

---
### Input Files
##### Network Model (i.e., Load Flow Case)
- The `.raw` file used to represent a commercial case.
- It defines the base topology before transmission outages are applied.
##### Zonal Factors
- Defines the participation factors of individual buses in aggregate definitions.
- For each aggregate, the sum over its component buses' participation factors is one.
#### Generator Data
- All non-demand bidder offer curves.
- Generators, energy storage, imports, exports, up-to-congestion transactions, HVDC scheduling.
#### Initial Unit Status
- Unit on/off status and MW output (if on) entering the simulation day.
#### Day Ahead LMPs
- Defines demand zones and aggregates which are pricing (i.e., bidding) points that need to be further defined because they are collections of individual nodes.
#### Demand Bids
- Hourly demand for all zones.
- Cross-references with the Day Ahead LMPs and Zonal Factors files to distribute the hourly demand (specified herein) to individual nodes.
- Also allows demand to be specified at an individual node, if desired.
#### Overrides
- A series of `%include` statements that allows the user to mutate previously defined data.
- Fuel prices, renewable generation, generation outages, generation derates, loop flows, etc.
---
### Overrides
##### Branch Overrides
- Models branch outages and derates
##### Hourly Profiles Overrides
- Regional solar and wind generation
##### Generation Outage Overrides
- Models generation outages
##### Generator Derate Overrides
- Models generator derates
##### Loop Flows Overrides
- Models load and generation in external areas
##### Fuel Prices Overrides
- Models fuel prices
##### Emission Allowance
- Currently blank/unused
##### Emission Region
- Currently blank/unused
##### External Areas
- Models external areas such as AECI, SPA, etc. to zero-out their line losses from the perspective of MISO's computations.
##### Fuel Emission Rate
- Models emission rates by each fuel type. Currently populated with reasonable numbers, but unused since the other emissions inputs are blank/unused.
##### Generation Emission Region File
- Models the plants (PROBE resources) that are affected by emissions prices.
##### Transmission Constraint Demand Curves (TCDC)
- Models the breakpoints and price levels associated with transmission constraint demand curves.
##### Flowgates Overrides
- Currently blank/unused
