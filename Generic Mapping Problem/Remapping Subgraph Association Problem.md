Network models are constantly evolving as a result of topological changes, renaming elements, equipment upgrades, etc. Therefore, a core task in maintaining an accurate network model is to *map* network elements' old values to their new values. Moreover, elements enter and exit the network model as elements are added to or removed from the network model.
##### Definitions
Let $A$ and $B$ denote two different snapshots (i.e., states) of a graph, where $A$ is an earlier version than $B$. In general, $A$ and $B$ will have some nodes and edges in common, there will exist nodes (edges) that are in $A$ but not in $B$, and there will exist nodes (edges) that are in $B$ but not in $A$. 

Given a single connected component $G = (V, E)$, an *edge cut* is a set of edges that, upon removal, disconnects $G$, resulting in more than one connected component. Likewise, a *vertex cut* is a set of vertices that, upon removal, disconnects $G$.

If $G$ is a connected component and $G' := G[V']$ is a subgraph of $G$ induced by the vertices $V' \subseteq V$, then $G'$'s *edge boundary* $\partial_e G'$ is the edge cut that creates a component identical to $G'$ (with no additional edges or vertices). Informally, $\partial_e G'$ is the set of edges in $G$ that encircles $G'$. Upon removing from $G$ the edges $\partial_e G'$, $G$ is disconnected into $G'$ and the induced subgraph $G[V - V']$ (this is the subgraph induced by the set of vertices that are in $V - V'$ (i.e., those that are in $G$ but not $G'$).

Analogously, $G'$'s *vertex boundary* $\partial_v G'$ is the vertex cut that creates a component identical to $G'$ (with no additional edges or vertices). These are, casually speaking, the set of vertices in $G$ that encircles $G'$. Similarly to the edge boundary case discussed above, after removing from $G$ the vertices $\partial_v G'$, $G$ is disconnected into $G'$, $\partial_v G'$, and the induced subgraph $G[V - V']$.

---
The primary difficulty associated with the Remapping Subgraph Association Problem is its definition (e.g., how do we define *boundary*?). With the definitions in hand, and once we know our objective, the algorithm design task is straightforward.
### Remapping Subgraph Association Problem (Edge Cut Version) 
**Input:** Graphs $A$ and $B$.
**Output:** Pairs $(A_1', B_1'), \dots, (A_k', B_k')$ of subgraphs $A_i' \subseteq A, B_i' \subseteq B$ such that $A_i'$'s edges are in $A$ but not in $B$, $B_i'$'s edges are in $B$, but not in $A$, and $\partial_e A_i' = \partial_e B_i'$ for all $i=1, \dots, k$ .
##### Solution
1. Compute the set of edges that are in $A$, but not in $B$. Call these *$A$-only edges*.
2. Compute the set of edges that are in $B$, but not in $A$. Call these *$B$-only edges*.
3. Run breadth-first search in graph $A$ from each node that is an endpoint in the $A$-only edges. The termination condition for each breadth-first search is when no more incident $A$-only edges can be found. Store each $A$-only component $A'$ along with its boundary $\partial_e A'$.
5. Run breadth-first search in graph $B$ from each node that is an endpoint in the $B$-only edges, with the analogous termination condition to the preceding step. Store each $B$-only component $B'$ along with its boundary $\partial_e B'$.
6. For each $A$-only component $A'$, search through the $B$-only components' boundaries. If a boundary $\partial_e B'$ is found such that $\partial_e B' = \partial_e A'$, then store the subgraph pair $(A', B')$.
7. Return the subgraph pairs $(A_1', B_1'), \dots, (A_k', B_k')$.
### Remapping Subgraph Association Problem (Vertex Cut Version)
**Input:** Graphs $A$ and $B$, along with known .
**Output:** Pairs $(A_1', B_1'), \dots, (A_k', B_k')$ of subgraphs $A_i' \subseteq A, B_i' \subseteq B$ such that $A_i'$'s edges are in $A$ but not in $B$, $B_i'$'s edges are in $B$, but not in $A$, and $\partial_v A_i' = \partial_v B_i'$ for all $i=1, \dots, k$ .
##### Solution
1. Compute the set of edges that are in $A$, but not in $B$. Call these *$A$-only edges*.
2. Compute the set of edges that are in $B$, but not in $A$. Call these *$B$-only edges*.
3. Run breadth-first search in graph $A$ from each node that is an endpoint in the $A$-only edges. The termination condition for each breadth-first search is when no more incident $A$-only edges can be found. Store each $A$-only component $A'$ along with its boundary $\partial_e A'$.
5. Run breadth-first search in graph $B$ from each node that is an endpoint in the $B$-only edges, with the analogous termination condition to the preceding step. Store each $B$-only component $B'$ along with its boundary $\partial_e B'$.
6. For each $A$-only component $A'$, search through the $B$-only components' boundaries. If a boundary $\partial_e B'$ is found such that $\partial_e B' = \partial_e A'$, then store the subgraph pair $(A', B')$.
7. Return the subgraph pairs $(A_1', B_1'), \dots, (A_k', B_k')$.