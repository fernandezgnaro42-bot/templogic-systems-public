# Brújula Delta-T

**Status: IN DEVELOPMENT.** The technician image booted on physical hardware in an earlier build; the current build has not been recorded on hardware.

Delta-T is the technician edition of [Brújula](02-brujula.md), for commercial HVAC and refrigeration work.

## Capabilities (IN DEVELOPMENT)

- Pressure-temperature lookup and a refrigeration diagnostic that run offline, with no internet.
- Temperature logging with slow-leak detection. Thresholds are starting values to be tuned, not validated limits.
- Refrigerant charge log with an annualized leak-rate calculation.
- Disk-health monitoring.
- A read-only reader for building management systems (Modbus TCP read functions and BACnet ReadProperty). Writes are refused by design.
- A sensor protocol over LoRa with authenticated encryption, uplink only.
- A connector to Praecura (see [Praecura](06-praecura.md)).

## Evidence

| Capability | Class | Date | Scope | Limits |
|---|---|---|---|---|
| Technician image (version 0.5) booted from USB on a physical Dell computer; menu and console reached; status command reported a healthy guardian, CPU, memory and, after a fix, temperature (41 degrees C) | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-09 | An earlier build. On first boot the temperature read was unavailable because that machine's sensor layout was not recognized; the sensor code was fixed and a new image was booted on the same machine that night | The image file that exists today is a later rebuild (2026-10-26); its boot on hardware is not recorded |
| Offline pressure-temperature lookup (R-404A) gives the same result in the image as on the laptops | LABORATORY VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-09 | Virtual machine | |
| Temperature rule fired on a real laptop during sustained heavy load | OPERATIONALLY OBSERVED, HISTORICALLY DOCUMENTED | 2026-10-09 | Rule of 85 degrees C | Laptop, not refrigeration equipment |

## Limits, stated plainly

- Event sensors produce notices. Delta-T is **not** a listed fire alarm, and does not claim to prevent loss.
- It does not control equipment and is not a building management system.
- The building-system reader has not been tried on a real customer site.
- Sensor firmware for the radio nodes and receiver has not been compiled or tested on hardware.
- No installation to disk from the image; no customer use.

Common test results: see [Brújula](02-brujula.md).
