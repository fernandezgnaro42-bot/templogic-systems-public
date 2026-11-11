# Research and technical results

**Label: EXPERIMENTAL.** These are laboratory results about our data, not about field performance.

## Data recovery and validation (completed 2026-11-11)

We reviewed a collection of 2,341 written HVAC and refrigeration service case records to see how much of it could support model training.

| Finding | Result |
|---|---|
| Records with all four required readings (suction pressure, discharge pressure, compressor current, ambient temperature) plus a refrigerant, taken from labeled lines | 19 |
| Of those, with no physical-consistency warning | 14 |
| Numbers written inside sentences that a manual audit found clearly correct | 45 percent of 40 sampled |
| Sentence-level numbers kept as review candidates, not as measurements | 478 rows over 272 cases |

What this means:

- Written cases are useful for review and testing, not for training on their own.
- Ambient temperature is the most important missing variable.
- No record has documented instrument readings, and no fault label has been reviewed by a technician yet.
- Pressure-temperature tables used in checks agree with an independent thermodynamic library within 0.03 K for five refrigerants and 0.8 K for R-410A. Both derive from published equations of state, so this checks transcription, not independent physics.

Ten automated quality checks (duplicates, missing features, units, pressure-temperature, refrigerant and equipment classification, fault labels, implausible values, leakage, provenance) are covered by 80 tests.

## Earlier model training (October 2026, HISTORICALLY DOCUMENTED)

Models were trained on synthetic data produced by a physical model of equipment behavior, across 11 equipment groups (44 models), and labeled synthetic. Real-data evaluation has not been done, so this is not evidence of field accuracy.

## What we do not claim

- No diagnostic accuracy for any model.
- No field performance.
- Synthetic, rule-based and narrative data are never mixed in one model.

## Next

Physics-based simulated telemetry is PLANNED, not started. See [roadmap](11-roadmap.md).
