To support *domain traversal* in the [[Generic Mapping Problem]], we organize data into network models.
### Approach
We have an abundance of data types -- scalars, arrays, text, images, videos, time series, csvs, PowerWorld, PSSE, and Dayzer case files, and more. These data sources are ever changing. As such, it's imperative that our design patterns accommodate an extensible class hierarchy.

A network structure -- along with auxiliary data associated with nodes, edges, and subgraphs -- is a natural candidate for representing our multi-domain data. Indeed, the relevant infrastructure calls for a network data model. The transmission system, natural gas pipelines, LNG shipping channels, etc. are all naturally modeled as flow networks. Since our work at the nodal (or sub-nodal) level of analytical granularity is so heavily dependent upon the infrastructure, it seems wise to prioritize a representation that is infrastructure-driven.

##### Auxiliary Data
Classically, a flow network is defined as a set of nodes and directed edges (with capacities and per-unit transportation costs), which are ordered two-tuples of nodes. In practice, much of the expressivity of flow networks is tied to the auxiliary data associated with nodes, edges, and subgraphs. These auxiliary data should be accessible via attributes and methods associated with classes we define to represent the network elements.

There exist datasets of interest that aren't inherently *network data*. Yet, our radical wager is that with a sufficiently open mind and with enough preserved flexibility in our design, that our decision to organize our data through flow networks will accommodate all different data types. After all, suppose that there exists a particular dataset for which it proves unnatural to find any level of network granularity and any network element with which to associate it. Then, we might associate this dataset with a subgraph (which could include the entire network). As an example, a dataset of macroeconomic variables (e.g., interest rates) might be treated in this manner.

##### Varying Levels of Granularity
As discussed in the example involving the [[Bus-Branch Model]] and the [[Node-Breaker Model]] in [[Generic Mapping Problem]], there are different levels of granularity of interest. It is imperative that our class hierarchy supports movement across granularity levels. We achieve this through our design by including multiple network models -- each capturing a different level of model granularity -- along with pointers linking the models and their elements to one another. We begin with the aforementioned [[Bus-Branch Model]] and [[Node-Breaker Model]].

### Implementation Sketches
- [[Bus-Branch Model Implementation Sketch]]
- [[Node-Breaker Model Implementation Sketch]]
