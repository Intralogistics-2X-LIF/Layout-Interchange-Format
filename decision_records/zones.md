# Situation
VDA 5050 version 3.0 introduced the concept of zones, which represent polygons with logical implications.

# Complication
Zones are a separate concept from a map in VDA 5050, represented by a mobile robot's current zoneSet. zoneSets can be updated indepedently of mobile robot's map and/or navigation graph.

Furthermore, some mobile robots are "layoutless", meaning they have no onboard map at runtime, and merely respect **any** nodes and edges and their associated geometries at runtime. Even these "layoutless" mobile robots must independently store at least one zoneSet and its geometry if zones are to be used. Such a provider of a "layoutless" mobile robot may do this once and be done with it, or expose and respect downloadZoneSet functionality.

The LIF up to this point has been entirely focused on how to define a navigation graph, and only that graph, and how a mobile robot or traffic control system may understand it, and what information a traffic control system would need to send a VDA 5050 order to a mobile robot.

# Decision
LIF version 2.0 will not attempt to incorporate zones.

# Rationale
It is a good thing to keep the graph definition separate from the zone definition, especially since each can be updated or changed independently from one another, conceivably at any time.

VDA 5050 version 3.0 already defines the zoneSet topic for a complete definition of zones, unlike with navigation graphs. While it may be the case that a mobile robot provider would wish to configure a single or limited set of zoneSet objects to supply to a traffic control provider that the traffic control must define and set at runtime, the JSON structure of such a zoneSet is already heavily implied by VDA 5050. The added benefit of including these into the LIF, or perhaps a sister standard, is minimal.

# Future Decisions
While for LIF version 2.0 zones were not included, if it is requested that the workgroup addresses them, they could potentialy be added to a parallel standard (such as a "ZIF" (Zone Interchange Format)). Adding them into the LIF itself seems to violate the decoupling of zoneSets from maps in VDA 5050 3.0 as it currently exists.
