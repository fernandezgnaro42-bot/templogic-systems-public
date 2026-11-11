# Engineering milestones

Each row says what was checked, when, and the limits of the check. All are laboratory software verification unless stated.

| Date | Item | Result | Scope and limits | Label |
|---|---|---|---|---|
| 2026-11-11 | Brújula automated tests | 635 pass | Isolated copy, guarded runner. One timing-sensitive serial-port test failed once under heavy parallel load and passed 3 of 3 alone. | VERIFIED |
| 2026-11-11 | Brújula guardian (Rust) | 15 pass | Unit tests | VERIFIED |
| 2026-11-11 | Praecura automated tests | 115 pass | Isolated copy | VERIFIED |
| 2026-11-11 | Latenza automated tests | 109 pass | Isolated copy | VERIFIED |
| 2026-11-11 | Oricalco project checks | Pass | Code-level checks only; VM and security service not validated | VERIFIED |
| 2026-11-11 | ML laboratory tests | 80 pass | Data schema, validators, extractor | VERIFIED |
| Oct 2026 | Brújula images (Oricalco, Eudaimonia, Delta-T) | Built | Files exist. Real-hardware boot not demonstrated. | VERIFIED (build only) |

## Not milestones yet

Production use, customer deployments, field accuracy of any model, real-site building-system reads, radio firmware on hardware.

Earlier public statements of test counts on our website are out of date; this page is current as of its date.
