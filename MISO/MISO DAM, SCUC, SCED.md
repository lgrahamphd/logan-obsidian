[[MISO]] solves an optimization problem to clear its Day-Ahead Energy Market and its Operating Reserve Market over the 24-hour dispatch horizon.

**Objective:** minimize costs of energy and operating reserve procurement.
**Constraints:** meeting load, transmission capacity, generation capacity, generation ramping.
**Robustness:** constraints must be satisfied subject to $N-1$ contingencies. That is, upon shocking the network with pre-defined outage sets, load must still be met, transmission constraints, and generation constraints must still be satisfied.

---
### Procurement Costs
- Start-Up Offers and No-Load Offers for Generation Resources and Demand Response Resources (DRRs)-Type II  committed by SCUC
- Shut-Down Offers and Hourly Curtailment Offers for DRRs-Type I committed by SCUC.
- Energy Offers, Regulating Reserve Offers, Spinning Reserve Offers, and Supplemental Reserve Offers of all Generation Resources, DRRs-Type II, and External Asynchronous Resources selected by SCED for Day-Ahead Schedules.
- Regulating Reserve Offers of all Stored Energy Resources selected by SCED for Day-Ahead Schedules.
- Dispatchable Import Daily Offers selected by SCED for Day-Ahead Schedules.
- Spinning Reserve Offers, Supplemental Reserve Offers, or Off-Line Short-Term Reserve Offers for DRRs-Type I selected by SCED for Day-Ahead Schedules that were not committed for Energy by SCUC.
- Off-Line Short-Term Reserve Offers for all Generation Resources, DRRs-Type II selected by SCED for Day-Ahead Schedules.
- Price adjustments for the cost of committing Fast Start Resources, the Energy cost of Fast Start Resources dispatched at limits, Up-Ramp Capability and Down-Ramp Capability by SCED-Pricing, Short-Term Reserve by SCED-Pricing.
- Virtual Supply Offers.
---
### SCUC
- MISO co-optimizes Energy and Ancillary Services.
- Commit offered resources at least-offer price using the SCUC algorithm to meet the Energy, Operating Reserve, other reserve products, transmission constraint, and Sub-Regional Power Balance Constraints.
- Clear Offers and Import Schedules to meet Demand Bids, Operating Reserves, and other reserve requirements for each hour of the upcoming Operating Day using the SCED and SCED-Pricing algorithm to yield Day-Ahead Schedules, Day-Ahead [[Ex-Ante LMP]], Day-Ahead [[Ex-Post LMP]], Day-Ahead Ex Ante MCPs, and Day-Ahead Ex Post MCPs
---
### SCED
RT SCED produces:
- Dispatch Targets
- Ex-Ante LMPs - informational only
- Ex-Ante MCPs - informational only, prices for ancillary services
RT SCED-Pricing produces:
- Real-Time Ex Post LMPs
	- *The Real-Time Ex-Post formulation allows Fast Start Resources, Emergency Operations Resources, Emergency Demand Response, Load Modifying Resources, Emergency Energy purchases, as well as Emergency Resources and Emergency ranges to set prices.*
- Real-Time Ex Post MCPs