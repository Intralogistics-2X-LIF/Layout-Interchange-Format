# Situation
LIF v1's goal is to provide all the information necessary to a traffic controller in order to send valid VDA5050 orders to vehicles under its control. The LIF is centered around defining navigation graphs in the context of a specific vehicle type. Station definitions may not be strictly requried to do this, since VDA5050 orders only contain `node` and `edge` objects.

# Rationale of LIF v1 Stations
There were two main motivations behind including a `station` collection in the LIF.

## StationType
The weaker of the two reasons, this one was becasue of the VDA5050 named action parameter stationType in VDA5050. If a 3rd party master control system was to know the stationType, it made a kind of sense to have it be represented in the LIF in some fashion. This could have been done with just a parameter on each action inside the LIF, however, which is why this is the weaker of the two points.

## Basic Practicality
LIF v1 was meant to be a one-way exchange up from a vehicle integrator to a master control system. While the master control and vehicle integrator would often of course need to share navigation graph geometry and/or consistent and unique identifiers for components of the graph in order to define what valid VDA500 commands would look like, these unique identifiers may not, and often are not, what the end-customer would recognize. For instance, the customer could know they have a bank of five conveyors, with their logical pick/drop point with mobile robots being named CONVEYOR_1 through CONVEYOR_5 in their ERP or WMS or WCS or whatever system. Maybe the LIF has a corresponding node with the same name, maybe it doesn't. It could be that multiple vehicle types need to interact with the same physical and logical location in the real world, and therefore need two nodes that link to the same place. It was (and still is) assumed that a vehicle integrator will almost always know what the end-customer's logical names are for stations, the places where, for example, loads will be tracked. As such, including these in the LIF to maintain alignment between vehicle integrator, mobile robot master control, and upper-level systems which may be issuing commands to the master control seemed like an absolute win in terms of usability.

This hard link between nodes and stations could have been done in other ways, such as relying on the master control to manually configure it on some kind of master data configuration, or just hoping the vehicle integrator provided a parallel bit of information about these links. This seemed like an inane solution when the links between nodes and stations could just be made explicit within the LIF itself.

## Logical Necessity
Finally, the strongest point: There are further, more complicated cases that simply necessitate stations' inclusion to avoid ambiguity, and to where a parallel configuration layer might be flatly impractical. While not expected to be super common, nodes and stations may be located on top of one another in various ways. Imagine a rotation point, where loads can be dropped and picked either short side leading or long side leading, potentially by different vehicle types with different `interactionNodeId`s for the same `station`, and the LIF team's argument was that there was no way to practically achieve this without including a `station` definition in the LIF itself.

# Stations in LIF v2, and Potentially Afterward
With LIF v2, one of the explicit goals is to remove the unidirecitonal nature of LIF transfers. (See Issue [#15](https://github.com/Intralogistics-2X-LIF/Layout-Interchange-Format/issues/15).) It still is the explicit goal of the LIF to restrict the scope only to what is necessary to exchange VDA5050 orders between vehicles and a master control system from different vendors. This is a superset of previous functionality, which means the same rationale for `station` definitions in LIF v1 is equally valid in LIV v2 (and presumably future versions).

It is not currently the intention to expand upon stations any further, other than their explanatory power to link nodes to stations.
