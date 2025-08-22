[MISO Presentation]("C:\Users\LoganGraham\OneDrive - Roscommon Analytics\Documents\Logan's Obsidian Vault\Library\MISO\2020-07-01 MISO 20210216 MISO Distributed Energy Resources (DER) Session 2 Operational Impacts.pdf.pdf")

##### Definition
A *distributed energy resource (DER)* is any resource located on the distribution system, and subsystem thereof, or behind a customer meter. These resources may include, but are not limited to, electric storage resources, distributed generation, demand response, energy efficiency, thermal storage, and electric vehicles and their supply equipment [FERC Order No. 2222].

##### Two-way Flow
A load node amalgamates all distribution system properties associated with its load footprint. "Within" a load node (i.e., behind the meter), there is load to be served via the distribution system. One might view generation units as *sources* and load nodes as *sinks* in the flow network (careful not to conflate this with the common use of the terms "source" and "sink" when referring to FTR paths).

Consider a load node $v$. Suppose that there are DERs associated with the $v$'s load footprint. Such DERs provide supply to the portion of the distribution system associated with $v$. As such, they reduce the (net) load that needs to flow to $v$ in the transmission system. Moreover, power can flow from DERs (on the distribution system) through step-up transformers and onto the transmission system. This is referred to as *two-way flow*.

##### Information Opacity
ISOs see DERs as if they are electrically connected at the transmission-distribution (*T-D*) substation. As such, the ISO can be unaware of important distribution system phenomena.

Concerns exist regarding lack of visibility and situational awareness about the locations, status, and output of DERs as well as their overall impact on power flows along distribution circuits.

![[T-D interface communication.png]]
