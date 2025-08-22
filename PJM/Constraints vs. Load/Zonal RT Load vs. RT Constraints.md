*Note: in the present study, we've prioritized RT load vs. RT constraints. We intend to extend these analyses to the DA market.*
### Yorkana 230 kV CB, Conastone 500/230 kV XF outages
Yorkana 230 kV CB outage from 14:15 on 5/8/2024 - 7/31/2024 (target).
Conastone 500/230 kV XF outage from 15:00 on 7/2/2024 - 12/31/2024 (uncertain target).
### Monitored Elements
YORKANA B43 CB 230 KV
- 230 kV circuit breaker
JACK ME 115KV - BAIR 115KV (BAIR 115 KV BAI-JAC)
 - 115 kV line
CONASTON 500KV - CONASTON 230KV (CONASTON 500 KV 500-4)
 - 500/230 kV transformer
 CONASTON 230KV - NRTHWES2 230KV
- 230 kV line
##### YORKANA B43 CB 230 KV
Constraints with monitored element YORKANA B43 CB 230 KV first bound in RT at 23:45 on 7/3/2024. $136/MWh in DA, $122/MWh in RT for July 1 - 16, 2024.
##### JACK ME 115KV - BAIR 115KV
Constraints with monitored element JACK ME 115KV - BAIR 115KV have bound in RT and DA (less so) after the Conastone 500/230 kV XF outage.

We observed that constraints with the JACK ME 115KV - BAIR 115KV monitored element bound only when load was high. They also bound at a discrete set of shadow prices (see purple marks in the below).
##### CONASTON 500KV - CONASTON 230KV
Constraints with monitored element CONASTON 500KV - CONASTON 230KV have bound 

We observed a bimodal distribution with respect to BGE and PEPCO load. Low load, high load in these zones has led to constraints over the CONASTON 500KV - CONASTON 230KV monitored element binding more often than when moderate load was present in these zones. Yet, we observed a unimodal distribution with respect to other zones.

---
### Core Takeaways
When only the Yorkana CB was out, we saw Conastone-Northwest binding, particularly in cases where Mid-Atl load was heavier than Western load. Once the Conastone XF outage joined the Yorkana CB outage, Conastone-Northwest stopped binding, and Yorkana B43 took its place. Regional load imbalances with Mid-Atl load heavier than Western load have continued to lead to the considered constraints binding in RT. MetEd vs. BGE load imbalances also correlate with these constraints binding.

**Details:**

- RT 5-minute zonal load vs. RT 5-minute shadow prices (one dot for every 5 minute interval in which a constraint bound)
- Constraints grouped by monitored element (one color per monitored element)
- Dot size corresponds to shadow price magnitude
- Two time periods considered: (1) Yorkana 230 kV CB out only [14:15 on 5/8/2024-15:00 on 7/2/2024), (2) both Yorkana CB and Conastone 500/230 kV XF out [15:00 on 7/2/2024, morning of 7/17/2024)

When the Yorkana CB was out, but before the Conastone XF was out, constraints associated with CONASTON 230KV-NRTHWES2 230KV bound more often and at larger shadow price magnitudes when Pepco load was greater than Penelec load on a normalized basis (imagine a 45 degree line in the below plot). See the cluster of large red dots in the Northwest of this plot:

![[Penelec load vs Pepco load vs shadows Yorkana only.png]]
_After the Conastone XF started its outage, a regime change occurred. CONASTON 230KV-NRTHWES2 230KV has not bound in RT since the Conastone XF outage, and YORKANA B43 CB 230KV has bound much more often._ Notice in the below that whenever JACK ME 115KV-BAIR 115KV bound in RT, both Penelec and Pepco loads were high. Constraints involving both CONASTON 500KV-CONASTON 230KV and JACK ME 115KV-BAIR 115KV had higher shadow prices when Pepco loads higher than Penelec (loads on a normalized basis).

![[Penelec load vs Pepco load vs shadows Yorkana Conastone.png]]
All of the above commentary applies to Penelec vs. BGE.

Similar analyses hold for MetEd vs. BGE loads.

Yorkana CB outage only:

![[MetEd load vs BGE load vs shadows Yorkana only.png]]
Yorkana CB and Conastone XF both on outage:

![[MetEd load vs BGE load vs shadows Yorkana Conastone.png]]
The last plot shows that CONASTON 500KV-CONASTON 230KV, YORKANA B43 CB 230KV, and JACK ME 115KV-BAIR 115KV have all bound at higher shadow prices when BGE load was higher than MetEd load (on a normalized basis).

---
### Day Ahead Market
##### YORKANA 230KV - OTTCRKPL 230KV (OTTCRKPL 230 KV OTT-YOR)
FLO 500/230 kV Conastone 500-4 transformer
- Has bound in the day ahead market at $16.77/MWh in July 1-16, but not in the real time market

