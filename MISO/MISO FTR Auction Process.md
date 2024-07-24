Refer to Section 4.10 in [[BPM-004-r26_FTR_and_ARR_BPM_CLEAN.pdf]].

[[MISO]]
### Frequency
Annual, monthly

### Bids
An FTR Bid for a specified MW quantity $q$ of FTRs constitutes a bid to purchase at most $q$ MW. It's possible that fewer than $q$ MW clear, but it is impossible for more than $q$ MW to clear.

#### Bids must specify each of the following:
- Type of FTR (always "Obligation" in MISO)
- Receipt Point (i.e., *source*) and Delivery Point (i.e., *sink*), which must be distinct buses
- Maximum MW quantity desired
- Maximum acceptable price, in $/MW
	+ Can be positive or negative
	+ Within interval $[-\$150k/MW, \$150k/MW]$
- *Time-of-Use*
	- "Peak" or "Off-Peak"
- *Period*
	- Season or month
### Bid Curve
- Think of this as a demand curve.
- Comprised of up to 10 (MW, Price) pairs
- MW of the first (MW, Price) pair must be 0 MW
- (MW, Price) pairs must be non-increasing (in the standard, Euclidean Pareto sense).
	- Non-decreasing in MW.
	- Non-increasing in Price.
- (MW, Price) pairs are not cumulative. See the below examples for clarification.
#### Example 1 (Valid Bid Curve)
0 MW @ $2.00, 40 MW @ $2.00, 50 MW @ $2.00.
- Scenario 1: auction clears at $1.75.
	- 50 MW clear (not 90 MW; pairs are not cumulative)
- Scenario 2: auction clears at $2.25.
	- 0 MW clear (*market clearing price (MCP)* is greater than the bid price)

#### Example 2 (Invalid Bid Curve)
0 MW @ $2.00, 40 MW @ $2.00, 50 MW @ $2.50
- Invalid because (MW, Price) pairs are increasing in Price

#### Example 3 (Invalid Bid Curve)
0 MW @ $2.00, 40 MW @ $2.00, 30 MW @ $2.00
- Invalid because (MW, Price) pairs are decreasing in MW

### Offers
An FTR Offer for a specified MW quantity $q$ of FTRs constitutes an offer to sell at most $q$ MW. It's possible that fewer than $q$ MW clear, but it is impossible for more than $q$ MW to clear.

#### Offers must specify each of the following:
- Type of FTR (always "Obligation" in MISO)
- ID number of FTR offered
- Maximum MW quantity offered
- Minimum acceptable price, in $/MW
	+ Can be positive or negative
	+ Within interval $[-\$150k/MW, \$150k/MW]$
- *Time-of-Use*
	- "Peak" or "Off-Peak"
- *Period*
	- Season or month

### Offer Curve
- Think of this as a supply curve.
- Comprised of up to 10 (MW, Price) pairs
- MW of the first (MW, Price) pair must be 0 MW
- (MW, Price) pairs must be non-decreasing (in the standard, Euclidean Pareto sense).
	- Non-increasing in MW.
	- Non-decreasing in Price.
- (MW, Price) pairs are not cumulative. See the below examples for clarification.

### FTR Market Clearing Price (MCP)
The MCP is calculated from the shadow prices of the transmission constraints in the FTR auction linear programming problem. The shadow price of a transmission constraint is the rate of change in the objective function value for an infinitesimal increment or decrement in the capacity of the constraint. The MCP is the sum over all transmission constraints of the product of the *power transfer distribution factor (PTDF)* (or *outage transfer distribution factor (OTDF*) on the constraint times the shadow price of the constraint limit in the direction of the corresponding PTDF (or OTDF).