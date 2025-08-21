### Wilmarth XF9, XF10
**Approach:** long; blanket with paths and try to clear.
**Period:** GH25

With CB 8S24 at Wilmarth Substation out until 2025-03-31 17:59, Wilmarth XF9 FLO Crandal-Wilmarth and Wilmarth XF10 FLO Crandal-Wilmarth will bind.

This masks Helena-Scott County.

XF9 FLO Crandal-Wilmarth sends the 115 kV bus high and the 345 kV system to the Southeast low. 

With the 8S24 CB out, the steamer is sent low for either constraint.

**Sources:**
- NSP.MANKATST31
- Wind farms to the Southeast (e.g., Odell, Trimont)
- NSP.ODELL.WND, GRE.TRIMTTRIM (wind farms)
- NSP.NOBLES.WND <- also gives exposure to Nobles XF
**Sinks:**
- Sinking at NSP.KASOTA gives good exposure
- NSP.ST_PETER, NSP.NULM.7GT
### Fort Thompson XF
**Approach:** short
**Period:** GH25

Chapelle - Leland Olds outage ends 1/23. After this is complete, the constraint loses substantial binding probability.

**Sources:**
- Source at NSP.PROSE, NSP.MMPA.WWF, NSP.COYOTE (wind farms)
**Sinks:**
- SPA, AECI
- Don't sink at MEC.FARMER or CWLD.BLRG which are wind farms

---
### Maurine XF, Hettinger - Centipede
**Approach:** long, targeting South-to-North flow bottleneck
**Period:** GJ25

Consider both Maurine XF and Hettinger-Centipede simultaneously due to interaction effects, CPNode sparsity, and seam effects with SPP.

MDU.TSWF1 is a wind farm. It's on the high side of Maurine XF and on the low side of Hettinger-Centipede.

*Look at Rhame breaker outages*
- Rhame 382, 782 out 2024-09-30 - 2025-05-01

Glenham-Whitlock outage is a key driver.

April looks particularly attractive. Lel. Olds XF, Oahe-Sully, Sully-Whit. outages.

Need to be clever with paths.
Maurine XF has historically done 10x of Hettinger-Centipede.

---
### Eau Claire - King
**Approach:** form a portfolio of paths that have long exposure on constraints to bind as a result of Eau Claire - King outage.
**Period:** GJ25

##### Wabash County-Alma
**Sources:**
- SMP.OWEF
- SMP.RPU
- SMP.TEA_1.AZ
**Sinks:**
- DPC.JPM
- NSP.HATFIHAT1
- DPC.EKM1 (NG CT)
- NSP.WHEATO1 (NG, Oil CT)
##### Briggs Road XF
**Sources:**
- NSP.BRGSRD.MVP (also gives long exposure to Briggs Road XF)
**Sinks:**
- NSP.FRENCH1 (Oil, biomass)
- DPC.GENOA3 (Coal, also gives long exposure to Harmony-Genoa)

---
### Port Washington - Saukville
**Approach:** short, taking advantage of the operations directives on Port Washington while the line outages (include one HLW outage) are in place.
**Period:** GH25

**Sources:**
- WPS.FORWARD, WEC.BUTRIDGE1 (wind farms)
**Sinks:**
- WEC.CC.PORTW1

---
### Magic City - Souris
**Approach:** short; seems overvalued.
**Period:** FG25

**Sources:**
- GRE.NSPP_1.AZ
**Sinks:**
- NSP.VELVAVELV

It seems like there's at least $4/MWh of value in this path (both peak and off-peak) for FG25. The market is still scared off from X24. This constraint has serious risk of binding just before it is uprated in mid-November. The Lel. Olds-Chap., Lel. Olds-Lel. Olds, Lel. Olds-Antelope outages were also drivers.

At the winter rating, this constraint needs at least a moderately bullish outage to bind.

---
### Forman - Forman, Hankinson - Wahpeton, Fergus Falls - Hoot Lake, Edge Tap - Pelican Rapids, Tamarac - Cormorant
**Approach:** long
**Period:** FG25

Messy area. Lots of interrelated constraints. Need Ross' perspective regarding sources and sinks. Forman - Forman is at its winter rating (169 MW) through 2025-03-31. On 2025-04-01, then line is derated to 125 MW. 

MDU.FOXTL.WND -> OTP.MRES?
- Long exposure to Forman - Forman, Hankinson - Wahpeton, Fergus - Hoot Lake, Edge Tap - Pelican Rapids, and Tamarac - Cormorant.
