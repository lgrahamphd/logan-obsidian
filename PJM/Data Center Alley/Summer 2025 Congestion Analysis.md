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
- [x] Get Dominion weather proxy
	- Blend Richmond and Dulles station data
## Plots
- [ ] YoY Dominion load, heat index
- [ ] Heat index vs. load
    - Map year to color
	- Marginal violin plots
	- Tooltips including datetime, Dominion load, heat index
- [ ] Grouped/paired violin plots of constraint flow distributions
    - Side-by-side violin plots for each constraint for which we have constraint flow data
- [ ] Constraint flows vs. Dominion load scatterplots
    - Not all constraints will have flow data. Use a try-except pattern.
## Statistics
- [ ] 
## Notes
- [ ] Make notes on the data centers that have come online since September 1, 2024 and those due to come online before June 1, 2026.
	- Excel file with columns: data center name, size in terms of MW, commercial online date