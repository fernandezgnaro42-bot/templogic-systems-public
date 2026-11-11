# Brújula Delta-T

**Status: IN DEVELOPMENT**

Delta-T is the technician edition of [Brújula](02-brujula.md), for commercial HVAC and refrigeration work.

## Capabilities (IN DEVELOPMENT)

- Temperature logging with slow-leak detection. Thresholds are starting values to be tuned, not validated limits.
- Refrigerant charge log with an annualized leak-rate calculation.
- Disk-health monitoring.
- A read-only reader for building management systems (Modbus TCP read functions and BACnet ReadProperty). Writes are refused by design. It has not been tried on a real customer site.
- A sensor protocol over LoRa with authenticated encryption (ChaCha20-Poly1305), uplink only.
- A connector to Praecura (see [Praecura](06-praecura.md)).

## Limits, stated plainly

- Event sensors produce notices. Delta-T is **not** a listed fire alarm, and does not claim to prevent loss.
- It does not control equipment and is not a building management system.
- Sensor firmware for the radio nodes and receiver has not been compiled or tested on hardware.
- A technician-edition image has been built (October 2026); real-hardware operation is not demonstrated.

## Verified

Common Brújula tests: see [Brújula](02-brujula.md).
