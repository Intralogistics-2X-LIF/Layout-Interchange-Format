# History
LIF's development began as a "you know it when you see it" kind of effort with a very small team. The rational for Version 1.0 of the LIF was to have the minimum viable amount of information required for a traffic controller to know how to send VDA5050 orders to mobile robots. The intention was capture as many relevant use-cases as possible initially, but with the expectation of the release of a Version 2.0 covering any inadvertent or knowingly ommitted complicated functional gaps which Version 1.0 may have manifested.

As of late 2025, work on LIF Version 2.0 began. Nearly immediately the question of whether and how much to expand the LIF was brought up by multiple parties. See: [Issue #62](https://github.com/Intralogistics-2X-LIF/Layout-Interchange-Format/issues/62).

# Decision Options
_The following descriptions of the decision options were copied nearly verbatim from the one-pager attached to the above issue (#62)._

## Restricted / Original
"Exclusively the necessary information to define and create VDA5050 orders the robot is capable of executing."

### Pros
- Outlines a clear scope and design guideline for the core team to work with.
- Provides straightforward definition of responsibilities between LIF creator and LIF consumer.
- Constitutes a cleaner, simpler and more immediately approachable standard.

### Cons
-The concept of stations (their descriptor/height/position) already slightly violates this mandate, though
removing it would be problematic.
-Likely would require feature-rich design tools and traffic controllers to exchange additional information
parallel to the LIF.
-Only useful as a navigation graph description in the context of VDA5050, not extensible to other fleet control
<> mobile robot interface types.

### User Story
As a deployment engineer, I want to have a layout format where I can exclusively document all capabilities and
physical limitations of the mobile robot I want to deploy. I do not want to worry about any business logic or intended
or implied processes. All I want to do is document what my (or partner’s) mobile robot can or cannot execute. This
should be clearly defined for the hand-over to a fleet control software. Any additional information should be
communicated in a separate stream. After hand-over I take full responsibility for what is defined within the provided
layout-file and none for anything not covered within it.

## Expanded
"Comprehensive layout information interchange between all parties (e.g., mobile robot providers, fleet
controllers, design tools, ...)"

### Pros

### Cons

### User Story

# Final Decision
On 2026/02/27, the VDMA TAC (Technical Advisory Council) voted on which of the two options that LIF would pursue for Version 2.0 after having the implications of both options explained to them. The result: **Restricted**.

The immediate implications of this are as follows:
1. No new objects will be added to LIF Version 2.0 or subsequent minor releases unless they facilitate a more powerful description of `Nodes`, `Edges`, `Stations` or their subcomponents or associated concepts such as VDA5050 `Actions`.
2. No further expansions to the basic concept of Stations shall be made as part of the LIF 2.0 or subsequent minor releases. However, some legacy information concerning stations must be re-evaluated before the release of LIF 2.0. (E.g., stationHeight)

# Future Decisions

We may or may not re-evaluate the scope of LIF for a future major version (3.0 or later), depending on feedback from both the members of the VDMA as well as the general market. There is also the possibility of releasing an extended, separate partner format after the release of LIF 2.0 which may contain additional information. Any such decision favoring expansion shall require an explicit overturn, modification, or deprecation of this decision record.

As always, the LIF team welcomes feedback from anyone using the LIF. Do not hesitate to create a github issue and any potential associated pull request.
