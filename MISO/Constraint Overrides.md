---
aliases:
  - TCDC
---
# From MISO BPM 002

## Section 8.2.6.4: Assign Transmission Constraints with TCDC Temporary Overrides

- MISO Operators can temporarily override MVL associated with a constraint.
- This happens when TCDC does not allow for reliable constraint management  
  - Related to resource cost/response available.
- Any overrides will be posted within two business days  
  - Available at [Real-Time Binding Constraint Overrides](https://www.misoenergy.org/markets-and-operations/real-time--market-data/market-reports/#nt=%2FMarketReportType%3AReal-Time%2FMarketReportName%3AReal-Time%20Binding%20Constraint%20Overrides%20(xls)&t=10&p=0&s=MarketReportPublished&sd=desc)  
  - From the reader guide:  
    - These two reports provide 5-minute binding constraints by constraint names and branch information (monitored elements), and the reasons for overriding the default TCDC curve if needed.

### Factors Affecting Overrides

- Economic and physical characteristics of resources that impact the constraint
- Local and system-wide product pricing
- Changing system conditions (current and projected flows across the constrained element, as well as nearby transmission elements)

## Examples of Situations and Response

### Temporary Overrides — Increasing the MVL

- If a System Operating Limit (SOL) condition is expected to persist and raises reliability concerns, the MVL values of the TCDC may be raised to reflect these heightened reliability concerns and mitigate the condition.
- Conditions that may lead to MVL increases include, but are not limited to:
  - Conflicting constraints
  - High system-wide LMPs  
- *Conflicting constraints* refers to system conditions where congestion management of one transmission constraint adversely impacts the reliable management of one or more other transmission constraints.

### Temporary Overrides — Lowering the MVL

- It may also be necessary to lower the MVL values of a TCDC for a particular constraint from the default values.
- The most common reason for doing so is to avoid conflicting constraints.
- In other situations, temporary operating guides or other action plans, which rely on post-contingency action to avoid SOL (System Operating Limit) events.
 - This may be what is happening with [[MRBN]] when it's binding below \$1000.

### Sub-Regional Power Balance Constraint Curves

- All constraints relating to applicable seams agreements, coordination agreements, or operating procedures (Sub-Regional Power Balance Constraints) have an MVL.
- For any Dispatch Interval where a Sub-Regional Power Balance Constraint cannot be managed within its limit, the Marginal Value (also known as the shadow price) will be set to the Marginal Value Limit.
 - This functions like a price cap, not a limit as seen with [[MRBN]].

---

## MISO Settings

Group 1 vs Group 2

> *Detailed TCDCs for Group 1 and 2 are available in Tariff Schedule 28A (From BPM 002).*
### Group 1

| Group 1   | [0, 100kV] | (100kV, 161kV) | [161kV, ] | IROL |
| --------- | ---------: | -------------: | --------: | ---: |
| >=102%    |        500 |           1000 |      2000 | 4000 |
| 100%-102% |        400 |            700 |      1000 | 3000 |
### Group 2

| Group 2   | [0, 100kV] | (100kV, 161kV) | [161kV, ] |
| --------- | ---------: | -------------: | --------: |
| >=102%    |       1000 |           2000 |      3000 |
| 100%-102% |        700 |           1000 |      2000 |