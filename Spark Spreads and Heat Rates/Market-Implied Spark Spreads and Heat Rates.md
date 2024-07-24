##### Definitions
Consider a power hub, gas hub, contract period (i.e., *strip*) triple for which we have prices. The *market-implied heat rate* associated with this (power hub, gas hub, contract period) triple is defined as $\frac{\text{Gas Price }(\$/MMBtu)}{\text{Power Price }(\$/MWh)}$. This is analogous to the notion of a generation unit's [heat rate][Heat Rate].

Due to technological properties associated with the generation fleet, specific heat rates are common. For example, modern combined cycle units have heat rates of roughly 7 (or slightly less). A *gas peaker* (e.g., a combustion turbine) would have a heat rate of roughly 10. Fix a heat rate $HR$. Then, the *$HR$-spark spread* is defined as $\$/MWh - HR \cdot \$/MMBtu$. Specifically, this is the *dirty* spark spread. Since generating units must procure $CO_2$ and $NO_x$ emissions credits (depending upon the state in which they are located and the season), it is helpful to consider these costs as well when determining whether or not it is profitable for a given unit to run.

##### Use Cases
Market-implied heat rates and market-implied spark spreads are useful summary statistics for market tightness. Units' heat rates, fuel inputs and their sources, emissions factors, etc. are common knowledge (see, e.g., Velocity Suite/Energy Velocity). Therefore, given market-implied heat rates and/or market-implied spark spreads, one may ascertain which generation units are *in-the-money* (a generation operator essentially owns a call option on the spark/dark/etc. spread defined by its fuel input and its LMP).

When we have better awareness around which units are in-the-money, we can consider more reasonable scenarios (i.e., cases) in our analyses. In turn, this leads to more representative distributional forecasts for fair value and better quantification of risk.

##### Power Hub, Gas Hub pairs
For a given power hub, one might consider different gas hubs with which to compute market-implied heat rates and market-implied spark spreads. The decision of which gas hubs to consider depends upon which gas hubs' prices are relevant for the gas-fired generation units that either have nodes within the power hub or that supply the load nodes in the power hub.

The following are useful pairs (Power Hub, Gas Hub):
- (PJM West Hub, Transco Zone 6 Non-NY)
- (PJM West Hub, Tetco M3)
- (PJM West Hub, Transco Zone 5)
- (PJM NI Hub, Chicago Citygates)
- (PJM AD Hub, Dominion South); Note: Dominion South is now called "Eastern Gas South."
- (MISO Indy Hub, REX Zone 3)