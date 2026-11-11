# Brújula

**Status: IN DEVELOPMENT.** Working on physical computers; not production validated.

Brújula is a smart layer for Linux. It watches a machine, explains what it finds in plain language, and can take a small set of pre-approved actions. It comes in three editions: [Oricalco](03-brujula-oricalco.md) (personal), [Eudaimonia](04-brujula-eudaimonia.md) (general) and [Delta-T](05-brujula-delta-t.md) (technician).

## Architecture in three parts

| Part | Language | Role |
|---|---|---|
| Sensors | C | Collects readings from the system |
| Brain | Python | Applies rules, builds explanations, produces alerts |
| Guardian | Rust | The only part that acts. It performs only allow-listed actions and refuses everything else |

The part that can act is small, separate and restrictive.

## Capabilities (IN DEVELOPMENT)

- Rules written in plain language, with a rehearsal mode that shows what a rule would do before it is enabled.
- A local black-box record of recent readings and events. After an unclean stop it explains what happened.
- Access notices and file-integrity checks.
- Alerts that explain what happened and why.
- A Debian-based bootable image.

## Evidence

| Capability | Class | Date | Scope | Limits |
|---|---|---|---|---|
| Automated test suite: 635 tests, plus 15 for the Rust guardian | LABORATORY VERIFIED | 2026-11-11 | Current main branch, isolated copy, guarded runner. One timing-sensitive serial-port test failed once under heavy parallel load and passed 3 of 3 alone. | Software behavior in a controlled environment |
| Bootable image started from USB on a physical Dell computer, reaching the console and reporting a healthy status | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-09 | Technician-flavored image, an earlier build than the file that exists today | Found a defect on that machine (temperature unread); fixed and re-tested on the same machine the same night |
| Personal-edition image booted from USB on a physical Dell Inspiron 15 | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-26 | See [Oricalco](03-brujula-oricalco.md). The image file that exists today matches the recorded checksum | Live session; not installed to disk |
| Runs as a system service on two developer laptops, restarts itself after a forced kill, and the black box then reports the unclean stop | OPERATIONALLY OBSERVED, HISTORICALLY DOCUMENTED | From 2026-10-09 | Two laptops, own use | Service confirmed active on one of them on 2026-11-11. The other was not checked for this document |
| Phone notices: a temperature rule fired during real overheating of a laptop (94 to 99 degrees C), and the two laptops notified the same phone when the other stopped answering or came back | OPERATIONALLY OBSERVED, HISTORICALLY DOCUMENTED | 2026-10-09 | Own use; notices now name the sending computer | Not a safety system |
| Image started in a virtual machine with Secure Boot enabled | LABORATORY VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-09 | Virtual machine | Secure Boot on physical hardware is not recorded |

## Not yet shown

- Installation to a disk from an image (images run from USB).
- Long-duration runs and any customer use.
- Boot of every edition and every build on physical hardware. See each edition page.
- Production validation of any kind.
