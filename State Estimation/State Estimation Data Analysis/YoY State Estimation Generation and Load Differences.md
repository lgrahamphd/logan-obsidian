### Objective
Using our codebase and state estimator data, sketch an approach for analyzing year-on-year changes in generation and load.
### Relevant functions in our codebase
- `ftr.ext.panorama.reflow`'s `get_case_generators` function takes as input a Panorama collection (e.g., "miso-se") and a datetime associated with a state estimator case. It returns as output a pandas dataframe representing generator output at the unit level (i.e., ungrouped) at the timestamp corresponding to the state estimator case.
### Brainstorming functions to add to our codebase
- Function that takes as input a start timestamp and an end timestamp and returns as output a pandas dataframe representing a time series of generator output. This function would wrap `get_case_generators`, looping over multiple state estimator cases.
- Function that takes as input a start timestamp and an end timestamp and returns as output a pandas dataframe representing generation outage intervals that intersect the input start/end interval. Note that there are those generation outages covered by IIR and those that IIR misses. IIR's coverage is far from perfect (it's a tough job). Perhaps we start with only those generation outages reported by IIR.
---
### Questions and approaches for answering them
##### Which new generation has been running at impactful levels? Which generation that used to run at impactful levels has retired?
EIA data report estimates for new builds' and retirements' statuses, online dates, and retirement dates. However, there is a difference between a generator being "online" according to the EIA and that generator actually outputting meaningful supply. Likewise, there is also a difference in the impact of the retirement of a generator that recently output meaningful supply and the retirement of a generator that has run at muted capacity factors before retirement.

State estimator data show the observed generator output which we can use to identify which recently-completed new builds and recent retirements are most impactful to supply.

**Sketch:** compute total generation output by generator in May, 2024 and in May, 2025. Identify largest increases and largest decreases in generation output. Cross-check with IIR data to disregard deltas that were driven by generation outages and thus not indicative of new generation or retirements.

*LG notes to self:* outer join, fill na's with 0. Compute deltas. Sort by largest positive (negative) deltas.

##### How have load profiles changed by area?
**Sketch:** use Yes Energy's Snowflake database. Join `RT_LOADS` and `LOAD_ZONES`. Load data are reported at various levels of granularity: regionally (i.e., North, Central, South, MISO-wide) and at the Local Resource Zone grouping level (i.e., LRZ 1, LRZ 2 + LRZ 7, LRZ 3 + LRZ 5, LRZ 4, LRZ 6, LRZ 8 + LRZ 9 + LRZ 10).

Need to consider load relative to other regions/resource zones. We can tailor our analyses depending upon the level of depth and precision desired. A simple visualization of load time series grouped by region/resource zone could do the trick. A deeper diver could feature a MSTL decomposition to analyze trends and to understand seasonal effects.

**Example SQL query:**
```
select LZ.OBJECTID, LZ.ISO, LZ.ZONENAME, LZ.ZONETYPE, RTL.DATETIME, RTL.TIMEZONE, RTL.VALUE
from TS_LOAD as RTL
left join LOAD_ZONES as LZ on RTL.OBJECTID = LZ.OBJECTID
where 1=1
    and LZ.ISO = 'MISO'
    and LZ.ZONETYPE = 'Local Resource'
    and DATETIME >= DATE('2024-05-01')
    and DATETIME < DATE('2025-06-10')
order by
    DATETIME asc,
    ZONENAME asc;
```