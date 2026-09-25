## Situation

LIF is a standardized interchange format for layout definitions.

## Complication

Different integrators have different proprietary needs. During LIF v2.0 design, there were proposals to allow integrator-specific extensions through additional fields or generic "extensions" objects.

## Decision

The LIF's intention is to be parsed as automatically as possible while being consistent across all mobile robot integrators. No mobile robot supplier or integrator specific fields should be added, and there are no poorly defined "magic fields" in which to place arbitrary information to achieve this purpose. If any such information is required for a particular combination of mobile robot and fleet control provider, a parallel document shall be required.