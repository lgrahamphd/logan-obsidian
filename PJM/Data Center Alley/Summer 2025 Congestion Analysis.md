## Objectives
- Understand the drivers behind the congestion in Data Center Alley during the MQ25 strip.
- Compare the MQ25 and MQ24 congestion environments.

---
### Questions
- What are the top constraints in the area in MQ24 and MQ25?
- What is difference in area load, heat index-normalized load in MQ24 vs. MQ25?
- Which transmission outages contributed to congestion in MQ24 and MQ25?
- Which generation outages contributed to congestion in MQ24 and MQ25?
- Which data centers have come online since September 1, 2024?
- Which data centers are due to come online before June 1, 2026? What are their expected online dates and sizes in terms of load?
### Approach
- [x] Produce constraint history statistics for MQ24, MQ25 using Panorama API.
    - `constraintdb.get_binding_constraints_summary`; top constraints in each period
	- Manually select the top ~6 relevant constraints in MQ24 and MQ25. Take the union of these constraint sets. We want 10-12 total constraints to compare in MQ24 and MQ25.
	- `constraintdb.get_constraint_history`; binding history for each of the selected constraints
- [x] Get constraint flows, ratings data using Panorama API.
    - `reflow.get_constraint_flows`: constraint flow time series
	- `constraintdb.get_constraint_ratings`: constraint ratings time series
- [ ] Get Dominion load data
    - YES Snowflake query
    - [ ] Organize into a Jinja template directory (as a clean-up task after the code works)
- [ ] Get Dominion weather proxy
	- Blend Richmond and Dulles station data
- [ ] Compute heat index-normalized load
    - Heat index cooling degree hours
- [ ] Join the above so that we have one Pandas dataframe with datetime, constraint flow, constraint rating, shadow price, heat index-normalized Dominion load
- [ ] Create Plotly overlaid time series plots for (1) Dominion load, (2) heat index-normalized Dominion load.
    - 2024 heat index-normalized Dominion load in blue, 2025 heat index-normalized Dominion load in red
	- Time axis from June 1 - August 31 without stating year
- [ ] Create Plotly scatterplot of heat index-normalized Dominion load vs. constraint flow.
    - Map shadow price to dot size, with a default dot size when the constraint did not bind
	- Map color to constraint
	- Marginal violin plots
	- Tooltips stating (1) constraint name, (2), datetime, (3) constraint flow, (4) shadow price
- [ ] Make notes on the data centers that have come online since September 1, 2024 and those due to come online before June 1, 2026.
	- Excel file with columns: data center name, size in terms of MW, commercial online date