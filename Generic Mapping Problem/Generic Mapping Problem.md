Wholesale power and gas markets are inherently tied to network models. The transmission system, natural gas pipelines, LNG shipping channels, etc. are all naturally modeled as flow networks. In such flow networks, auxiliary data associated with nodes, edges, and subgraphs encode these systems' numerous characteristics. Moreover, depending up on the setting, level of granularity, etc., there exist multiple network models per domain.

As an illustrative example, consider a bus-branch representation of the [[Eastern Interconnection]]. We might define a network model in which nodes represent buses and edges represent branches. Nodes might contain fields corresponding to generators and/or loads that might be associated with these buses. In turn, these generators and/or loads have fields associated with them, e.g., heat rates, fuel types, type of load (residential, commercial, or industrial), demand response capability, etc. Edges might contain fields corresponding to branch ratings, outage schedules, etc.

Production cost models take this approach. Consider Dayzer, Plexos, Promod, and UPlan. State estimator data is defined on network models as well (e.g., Panorama).

At a finer level of granularity, we are interested in bus-breaker representations, for there exist material topological properties that can be masked through aggregation to the bus-branch level.

Time series data are also critical. For example, a given bus might have associated with it a load, which is part of an ISO's zone for which we have load history, forecasts, and vintage forecasts.
##### Evolution
Data evolves over time as generators retire or enter service, pnodes are remapped, etc. That is, network models change over time.
### Problem Statement
Define a family of network models that achieves the following:
1. **Domain Traversal**: connect data from different domains
2. **Evolutionary Traversal**: explore how data evolves over time (both backwards and forwards).
### Domain Traversal
Consider a bus-branch network model as well as a generating unit. Suppose that this generating unit has a planned outage schedule, a heat rate, an estimated offer-curve history, etc. If we're looking at this unit's planned outage schedule, we might also want to explore its heat rate, etc. We refer to the act of looking at various features of the generating unit as *domain traversal*.

As a second example, consider a circuit breaker in a [[Node-Breaker Model]]. Our goal may be to find the bus with which this circuit breaker is associated in the corresponding [[Bus-Branch Model]]. In the opposite direction, consider a bus in a bus-branch model. Our goal may be to find the breakers associated with this bus in a corresponding bus-breaker model.
##### Implementation Sketch
Domains associated with a given object should be reachable via attributes and methods associated with classes or instances thereof. We are to lean on the tenets of object-oriented programming to support moving across domains.
### Evolutionary Traversal
Consider a bus-branch network model and a pnode therein. This pnode might be derived from other pnodes. For example, a prior pnode may have been renamed in its history. We might wish to access all previous names associated with this pnode. We refer to the act of looking at an element's historic and future representations as *evolutionary traversal*.

As another example, at some point in its history, a branch might have been split in two due to a transmission line being tapped. We might wish to access the branch's ancestor branch (which might no longer exist).

As a third example, consider a branch and its outage schedule. We may be interested in how this outage schedule changes over time. Since we view the branch's outage schedule as part of the network model, this is another instance of evolutionary traversal.

Note: we avoid the term "time traversal," for various domains may include time series data. Yet, moving from time series in one domain to another time series in another domain is still domain traversal. By "evolutionary traversal," we refer specifically to how the network model evolves over time.
##### Implementation Sketch
Network model evolution is to be represented via a directed graph in which nodes correspond to states, and directed edges correspond to state evolution. Along with each object, we associate such a directed graph. This reduces evolutionary traversal to graph traversal.

Refer to the `GenericRemapper` class in `ftr-core/src/ftr/mapping/` for an example implementation of evolutionary traversal.