## Situation

The LIF defines edges as connections between nodes in a layout. An edge is a fundamental structure in the navigation graph that enables mobile robots to move from one location to another.

## Complication

In designing the LIF, there was a question about whether to support bidirectional edges. The issue is that such edges do not explicitly exist in VDA 5050; there is always a start node and an end node to every edge. The LIF could be changed to redefine the two nodes on an edge as a "terminalNodes" collection that is always of size 2. However, this would also cause a loss of precision in what could be defined.

For instance, it may be desirable to define different `reachOrientationBeforeEntering` values on the nodes or to have a corridor allowed for only one direction of an edge. If bidirectional edges were supported, these distinctions would become ambiguous or would require additional metadata to specify which direction the property applies to.

## Decision

Instead of allowing a combination of bidirectional and unidirectional edges, it was deemed simpler to have all edges be unidirectional. LIF shall support only unidirectional edges, with an explicit start node and end node for every edge. It was assumed that it should be relatively trivial for whichever design tool is being used to create the LIF to allow the user to define a bidirectional edge, which is then encoded as two separate unidirectional edges in the LIF. Likewise, the same design tool, if desired, could recombine these edges when it deems it necessary to do so for such a user. The burden of this encoding is appropriately placed on the tool layer, not on consumers of the LIF.

## Rationale

This is an intentional choice, reflecting the fact that such edges do not explicitly exist in VDA 5050. By restricting all edges to unidirectional form, different properties can be defined with full precision in each direction without ambiguity. All distinctions remain explicit and unambiguous.