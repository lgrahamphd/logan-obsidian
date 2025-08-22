## Contingency-on-Outage Reporter
**Input:** Branch outages from Panorama's API. Time interval of interest.
**Output:** For each outage over the time interval, return a list of constraints that have a history of binding and have a sibling constraint with that branch as a contingency. Sort intelligently.
#### Use Cases
When a constraint's contingency is OOS and a sibling constraint has a history of binding, then this sibling constraint is a prime candidate for a binding event. Such siblings should be reported.
#### Approach
Plotly Dash application. Interactivity to support time interval selection.

## Low-Side/High-Side Generation Characterizer
**Input:** Specified constraint, generator shift factors, and generator output from Panorama's API.
**Output:** A time series representation of the key low-side and high-side generators for the given constraint.

#### Use Cases
When analyzing a constraint, a key piece of the workflow is identifying which generators push on the constraint and which generators relieve the constraint. It's critical to know the most impactful dimensions in generator shift factor space and in generator impact space for each constraint. We define this below.

Define *generator shift factor space* as the vector space in which each generator has its own dimension. Then, for a given state estimator case, each constraint is a point in this space. Consider a constraint $C$ and a generator $G$. Then, $C$'s coordinate in dimension $G$ is $G$'s generator shift factor on $C$. It's often the case that a constraint's representation in generator shift factor space has a handful of components of relatively large magnitude while the remainder of components have values that vanish. We're interested in finding these material components and understanding how they trend over time.

Analogously, define *generator impact space* such that $C$'s coordinate in dimension $G$ is the product of $G$'s generator shift factor and its (real) generator output (Panorama calls this product *Impact MW*).

It's imperative to note that with each topological change between state estimator cases, each constraint's generator shift factor coordinates (and its generator impact coordinates) can change. As such, we must employ a time series approach.

#### Approach

## Low-Side/High-Side Renewable Loading Characterizer
**Input:** Specified constraint, generator shift factors, and generator output from Panorama's API.
**Output:** A time series representation of low-side and high-side wind generation and solar generation impacts.

#### Use Cases
This is a special case of the Low-Side/High-Side Generation Characterizer. We view each constraint as a vector in two-dimensional space which is reminiscent of generator impact space, but where the only two "generators" are *wind loading* and *solar loading*. One dimension corresponds to the impact of wind generation on the constraint. If wind generation is primarily on the low side of the constraint, then the constraint's wind-loading coordinate will be negative. Symmetrically, if wind generation is primarily on the high side of the constraint, then its wind-loading coordinate will be positive. The solar-loading dimension is analogous.

#### Approach

## Outage Time Window Visualizer
**Input:** Transmission outage facility history, IIR generation outages from Panorama's API.
**Output:** A visualization tool that helps one quickly identify contemporaneous outages of high importance in the same region.

#### Use Cases
This tool will help us keep track of outage schedules and interactions between outages.

#### Approach
Plotly Dash application. Gantt chart.
