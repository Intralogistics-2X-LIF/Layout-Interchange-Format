# History / Context
VDA5050 3.0 added the concept of [zones](https://github.com/VDA5050/VDA5050/blob/release/3.0.0/VDA5050_EN.md#64-zones), two dimensional polygons which can have various kinds of specific behaviors tied to them. 

These zones are defined as runtime dependent, and can change, with an expected frequency of change higher than that of the navigation graphs currently defined by the LIF. The LIF workgroup evaluated whether their inclusion into the LIF was practical and effective.

# Decision Options
1. Attempt to include zones in the LIF itself.
2. Attempt to include zones in a separate, similar-to-LIF definition file which explicitly shares origin/spatial information with a LIF.
3. Don't attempt to incorporate the zone concept at all into LIF.

# Final Decision
Option #3 above was selected.

The LIF 2.0 is meant to be an omni-directional transfer of navigation graph information. While zome zones might be defined by a mobile robot provider and sent to the traffic control system once at configuration time, many zones might be decided by the traffic controller at runtime and sent to the vehicle. Due to this potential ambiguity, and LIF 2.0's new clean and restricted mandate, the workgroup decided to decline from including zones into the LIF.

# Future Decisions
This decision affects only LIF 2.0. Zone definitions as part of the LIF can be added in a future minor version if the market is asking for it, and likely rather quickly, once we get more information about how they tend to be used.
