# Brújula

**Status: IN DEVELOPMENT**

Brújula is a smart layer for Linux. It watches a machine, explains what it finds in plain language, and can take a small set of pre-approved actions. It comes in three editions: [Oricalco](03-brujula-oricalco.md) (personal), [Eudaimonia](04-brujula-eudaimonia.md) (general) and [Delta-T](05-brujula-delta-t.md) (technician).

## Architecture in three parts

| Part | Language | Role |
|---|---|---|
| Sensors | C | Collects readings from the system |
| Brain | Python | Applies rules, builds explanations, produces alerts |
| Guardian | Rust | The only part that acts. It performs only allow-listed actions and refuses everything else |

The design principle is that the part that can act is small, separate and restrictive.

## Capabilities (IN DEVELOPMENT)

- Rules written in plain language, with a rehearsal mode that shows what a rule would do before it is enabled.
- A local black-box record of events, built to make tampering evident.
- Access notices and file-integrity checks.
- Alerts that explain what happened and why, rather than only reporting a code.
- A Debian-based installable image.

## Verified (2026-11-11, laboratory software verification)

- Automated test suite: 635 tests pass, run in an isolated copy with a guard that blocks system-changing commands.
- Guardian (Rust): 15 tests pass.
- Scope: this is software verification in a controlled environment. It is not evidence of performance in production.

## Not yet proven

Operation on production hardware, long-duration runs and any customer use. Images have been built; real-hardware boot is not demonstrated.
