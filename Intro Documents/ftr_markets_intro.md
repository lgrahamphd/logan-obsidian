# A Gentle Introduction To FTR Markets

FTR markets are a niche market focused on trading the price spreads of electricity between locations within a given grid operator's authority.  To understand these markets, it helps to understand three things: 

1. [Basic power engineering](#basic-power-engineering)
2. [Day Ahead (DA) markets and economic dispatch](#day-ahead-and-economic-dispatch)
3. [Financial Transmission Rights](#financial-transmission-rights)

## Basic Power Engineering

An introduction to powerflow from an advanced undergraduate course may be found [here](https://web.engr.oregonstate.edu/~webbky/ESE470_files/Section%205%20Power%20Flow.pdf) from Oregon State. The link covers (static) power flow analysis in depth, and introduces several methods of solving the power flow analysis, all of which should be familiar to you already. Importantly, the link points out the role that Jacobian matrices play in solving the system.

Also unsurprisingly, Taylor's Theorem implies that we can use the Jacobian matrix calculated at the steady state solution to linearize and calculate approximate solutions to perturbations of the system. Another advanced undergraduate introduction can be found [here](https://users.ece.utexas.edu/~baldick/classes/394V/Power.pdf) and introduces the concept of "shift factors" (see: slide 87, see also [this link](https://www.powerworld.com/files/TrainingI11LinearAnalysis.pdf)) and can be understood to represent the approximate (linearized) solution to how electricity will flow over different lines when MW are injected into a system at certain points and removed from the same system at other points. 

Note too that linearization implies inaccuracy of the perturbation (on order $O(\mathbf{p}^2)$ for the Peano form, where $\mathbf{p}$ is the perturbation). In addition, solving by linearization (almost always) assume "fixed angles" (thus creating a "Direct Current" circuit instead of an "Alternating Current" circuit), adding another layer of approximation error. 

Additionally, there are several related distribution and shift factors that one ought understand the relations between:

1. Power Transfer Distribution Factor (the normal "shift factor")
2. The Line Outage (Closure) Distribution Factor
3. The Outage Transfer Distribution Factor.

The PTDF is the "shift factor" introduced in the earlier links; the LODF is a linearization of how electricity would subsequently flow through the lines of a system per MW flowing on a line from A to B once the line from A to B is opened (outaged), with the LCDF being the natural converse of that operation (*closing* in this context means to bring a line back into service). The OTDF is a PTDF given some set of outages. [Here are a couple paragraphs from the PowerWorld Corporation describing these concepts.](https://www.powerworld.com/WebHelp/Content/MainDocumentation_HTML/Line_Outage_Distribution_Factors_LODFs.htm).

The reason why we want to calculate LODFs and OTDFs (versus just the PTDFs) is because, as mentioned in the next section, we will frequently want to perform **contingency analysis**, i.e. we will care what could happen in a variety of different scenarios. 

n.b. OTDFs and PTDFs are usually just called "shift factors" with no differentiation. 

#### Optional Topics:

The following presentations come from the Pennsylvania-Jersey-Maryland (PJM) Interconnection, the largest electricity market in the US (despite it's name, it covers more than just those three states). The material here will be less important than shift factors, but can provide a helpful background. _These require a PJM login from a registered market participant. We will send a copy of the materials until you can officially register._

1. [Electrical Theory - Power Principles and Phase Angle](https://www.pjm.com/training/-/media/058EBC749290483FA0C8BAC7EBBB6AD1.ashx)
2. [Electrical Theory - Transformer Theory](https://www.pjm.com/training/-/media/CAE323135F5642B499FBB2772EC77BC6.ashx)
3. [Electrical Theory - Power Flow on AC Transmission Lines](https://www.pjm.com/training/-/media/A8460A0F104444D3972577B3D0481E2A.ashx)
4. [Electrical Theory - Generator Theory](https://www.pjm.com/training/-/media/C416E9891B7C43E1A4F0AAE764C830F3.ashx)
5. [Power System Elements - System Loads](https://www.pjm.com/training/-/media/14575436FEE64D12888945E55E36E43B.ashx)
6. [Power System Elements - Transmission Facilities](https://www.pjm.com/training/-/media/830DC19C87B8408E993232FB00650940.ashx)
7. [Power System Elements - Generating Unit Basics](https://www.pjm.com/training/-/media/1A80A10071C24B8F94DE5794E7554AF4.ashx)
8. [Power System Elements - Relays](https://www.pjm.com/training/-/media/41BE1FF7B8B542D78986AC889E7BC3D1.ashx)



## Day Ahead and Economic Dispatch

Given these basic concepts, we are ready to build up the concept of *economic dispatch*, and from there, *security constrained economic dispatch*, which are intuitive concepts. The basic optimization problem we will seek to solve is the cheapest way to supply the necessary amount of electricity to the system, which is a deceptively complicated problem, from several perspectives. The standard model in the US grid operators involves a double auction, with both generation and load serving entities bidding into the market (so both supply and demand are both endogenously determined).

In a world with no transmission constraints, this is trivial; we would construct the supply curve simply by deploying generators in order of their bid curves/individual supply curves, not unlike the exercise of an introductory microeconomics course. However, with transmission constraints, the supply curve becomes substantially more complicated. The supply curve then depends on how much is *already* going to flow/is flowing over transmission lines (as well as other secondary constraining factors).

[The PJM training slides on LMPs has a worked example with a five bus transmission grid](https://www.pjm.com/-/media/training/core-curriculum/ip-lmp-101/lmp-training.ashx) beginning on slide 62 that is worth a look. 

As might be obvious, the obvious solution would then is to give heterogenous pricing based on location; it turns out that when we solve the (DC linearization) of the system, dispatching resources as is economic and respecting constraints on flow over constraints, we get a vector of *shadow prices* (or the value of the Lagrangians ${\lambda}$), which has the economic interpretation of the instantaneous cost savings per MW relaxed over individual constraining elements (transmission lines). When multiplied by the shift factors mentioned earlier, we actually find the *congestion* component of the optimal noding price (a variable solved in the optimization pricing). This has the economic interpretation then of being the impact on the price of electricity at a given location based on constrained transmission. 

William Hogan, an early advocate of locational marginal pricing, [has a working paper submitted to FERC that gives a rigorous treatment to this process](https://scholar.harvard.edu/whogan/files/hogan_ferc_041002.pdf). 

The "security constrained" portion of *security constrained economic dispatch* refers to the above process but monitoring not just PTDFs but also OTDFs as well for a given set of monitored/contingency pairs (the monitored is the constraint for which the OTDF is being calculated, and the contingency is the hypothetical outage). The reasoning here is to ensure robustness of grid operations even if lines were to fail unexpectedly. 

There are two primary types of markets where we see SCED: *Day Ahead* markets and *Real Time* markets. Day Ahead markets have supply and demand bids for one hour increments submitted one day ahead of time and subsequently solved one day ahead of time (hence the name), with dispatch being for these one hour increments. *Real Time markets*, like California ISO's 15 minute and 5 minute markets, often open for bids the day before and are ultimately solved close to delivery (e.g. CAISO's 15 minute market is solved 45 minutes ahead of delivery). In principle, the optimization between DA and RT markets is very similar and in an ideal world they would mirror each other- market issues or unexpected developments can cause deviation (note: pressure to converge in prices between these two markets comes from financial participants performing what is called "convergence bidding" or "virtual bidding", which is beyond the scope of this document). 

## Financial Transmission Rights

Financial tranmission rights evolved as a form of a hedge against uncertainty in the day ahead markets. As explained in PJM's trainings on FTRs [here](https://www.pjm.com/-/media/training/core-curriculum/ip-arr-ftr-annual/arr-and-ftr-basics.ashx) and [here](https://www.pjm.com/-/media/training/core-curriculum/ip-arr-ftr-annual/arr-ftr-advanced.ashx), FTRs are meant to:

1. hedge against _locational_ energy price uncertainty
2. be *simultaneously feasible* to ensure revenue adequacy of the hedging market, and
3. allow for trading of transmission entitlements

These FTRs are then constructed from bids placed into regular auctions for contracted paths flowing from point A to point B (where each bid specifies the source and the sink), and it turns out that the simultaneous feasibility test is ensuring that the net "flow" over a set of lines does not violate limits, very similarly to the DA markets, meaning that shift factors are again an important part of the process. Unlike DA markets, however, this flow is purely fictional, as these are financial products, not physical products. Also unlike the DA markets, the objective function is not about maximizing auction revenue for the auctioneer (the ISO). The Advanced FTR training from PJM covers an example annual auction clear starting on slide 94; the working paper from William Hogan also contains a formal definition and analysis of the problem.

Once an FTR has been acquired, it entitles the holder of the FTR to the congestion revenue of the sink node less the congestion revenue of the source node for some period and time of use (e.g. the month of Feb 2024 during the business day between a location in Arlington, VA and a location near Fredricksburg, VA).

Another useful source is the Master's thesis of Dimitra Apostolopoulou entitled [Optimized FTR Portfolio Construction: The Speculator's Problem](https://gross.ece.illinois.edu/files/2015/06/Thesis_submitted_Apostolopoulou_Dimitra.pdf) which discusses the above material in a formal manner and mentions a common methodology for how many FTR traders go about constructing portfolios, namely by:
1. Forecasting a subset of constraint shadow prices in the Day Ahead market for some period of time
2. Determining risk tolerance and thus ideal exposures
3. Constructing targeted paths to get those exposures and bidding appropriately in the auction.

There are many ways by which people do each of those three, but it's worth a read to further understand the problems a bit more. 

