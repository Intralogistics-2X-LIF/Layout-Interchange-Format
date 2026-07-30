# Situation
LIF 1.0's goal was to provide all the information necessary to a traffic controller in order to send valid VDA5050 orders to mobile robots under its control. The LIF is centered around defining navigation graphs in the context of a specific mobile robot type. Station definitions may not be strictly requried to do this, since VDA5050 orders only contain `node` and `edge` objects.

# Rationale of LIF v1 Stations
There were three motivations behind including a `station` collection in the LIF.

## StationType
The weakest of the three reasons, but due to the VDA5050 named action parameter stationType for the default VDA5050 actions of 'pick' and 'drop', this was deemed required to exist in some way. If a third party fleet control system was to know the stationType, it made a kind of sense to have it be represented in the LIF in some fashion. This could have been done with just a parameter on each action inside the LIF, however, which is why this is the weakest of the three points.

## Basic Practicality
LIF v1 was meant to be a one-way exchange up from a mobile robot integrator to a traffic control system. While the traffic control and mobile robot integrator would often of course need to share navigation graph geometry and/or consistent and unique identifiers for components of the graph in order to define what valid VDA5050 commands would look like, these unique identifiers may not, and often are not, what the end-customer would recognize. For instance, the customer could know they have a bank of five conveyors, with their logical pick/drop point to be used by mobile robots being named CONVEYOR_1 through CONVEYOR_5 in their ERP or WMS or WCS (or ...) system. Maybe the LIF and therefore VDA5050 commands have a corresponding node with these same names, but maybe it doesn't. It could be that multiple mobile robot types need to interact with the same physical and logical location in the real world, and therefore need two nodes that link to the same logical place/station, and then these nodes cannot have the same identifier, meaning one or more of them must differ from their associated station's name. It was (and still is) assumed that a mobile robot integrator will almost always know what the end-customer's logical names are for the stations themselves. As such, including these in the LIF to maintain alignment between mobile robot integrator, mobile robot traffic control, and upper-level systems which may be issuing commands to the fleet control seemed like an absolute win in terms of usability.

This hard link between nodes and stations could have been done in other ways, such as relying on the traffic control system to manually configure it on some kind of master data configuration layer, or just hoping the mobile robot integrator provided a parallel bit of information about these node<>station links in whatever arbitrary format. This seemed like an inane solution when the links between nodes and stations could instead be made explicit within the LIF itself.

## Logical Necessity
Finally, the strongest point: There are further, more complicated cases that simply necessitate stations' inclusion to avoid ambiguity, and to where a parallel configuration layer might be flatly impractical. While not expected to be extremely common, nodes and stations may be located on top of one another in various ways. Imagine a rotation point, where loads can be dropped and picked either short side leading or long side leading, potentially by different mobile robot types with different `interactionNodeId`s for the same `station`, and the LIF team's argument was that there was no way to practically achieve this without including a `station` definition in the LIF itself.

# Stations in LIF v2
With LIF v2, one of the explicit goals is to remove the uni-direcitonal nature of LIF transfers. (See Issue [#15](https://github.com/Intralogistics-2X-LIF/Layout-Interchange-Format/issues/15).) It still is the explicit goal of the LIF to restrict the scope only to what is necessary to exchange VDA5050 orders between mobile robots and a fleet control system from different vendors. The newly proposed (and likely to be implemented) omni-directionality is a superset of previous unidirectional functionality. This means the same rationale for `station` definitions in LIF v1 is equally valid in LIF v2 (and presumably future versions), basic [set theory](https://en.wikipedia.org/wiki/Set_theory) being a thing and all that...

It is not currently the intention to expand upon stations any further, other than the current explanatory power to link `node`s to `station`s. The LIF's goal is to be universally adopted, and keep its scope as limited as it can while still containing everything required to send valid VDA5050 orders. While there may be more information tied to station objects that might be useful to define in some particular mapping/design tool which goes on to export a LIF, these will vary from vendor to vendor. Attempting to include some of these additional things and not others is _likely_ a classic example of "feature creep", likely implies some logical implementations are more valid than others, and **definitely** introduces aspects of vendor-favoritism, which is strictly forbidden by the VDMA organization.

Because `station`s had position information in v1 (`stationPosition`), and we didn't wish to remove features that some providers already began to rely upon, despite it not technically being required information, it was begrudingly kept in LIF v2.

For similar reasons, `station`s' `stationHeight` was kept. This was _not_ a unanimous decision.

Because `stationType` is mentioned in VDA5050 as an `action` parameter expected for certain predefined `action`s (namely pick and drop), it, too, was added to LIF v2 on the `station` object. This was a reluctant yet necessary unanimous decision.

# Expanded Definitions of a Station or Other Objects in Versions of the LIF after 2.0

This decision record pertains to LIV v2, and does not preclude discussing this topic in any future version of LIF or a companion standard (such as VDA5050).
