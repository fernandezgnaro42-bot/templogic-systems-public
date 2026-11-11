# Praecura

**Status: IN DEVELOPMENT**

Praecura classifies likely faults and detects anomalies in commercial HVAC and refrigeration equipment from operating readings. It is read-only: it never controls equipment.

## Design (IN DEVELOPMENT)

- A web service backed by a relational database, with customer data kept separate per customer.
- Anomaly detection (Isolation Forest) trained per equipment group.
- Risk and component models that refuse to train until enough real data exists.
- Search over previously reviewed cases.

## Verified (2026-11-11, laboratory software verification)

- Automated test suite: 115 tests pass, run in an isolated copy.
- Scope: software behaviour. No claim is made about diagnostic accuracy.

## Evidence

| Capability | Class | Date | Limits |
|---|---|---|---|
| A server instance with its database has run on our own infrastructure with test data only (one equipment record, two readings) | OPERATIONALLY OBSERVED, HISTORICALLY DOCUMENTED | 2026-10-21 | No customer data |

## Current honest position

- Models trained so far use synthetic data, and the service does not yet use them.
- We make **no accuracy claims**. Real labeled field data is scarce; see [research and technical results](10-research-and-technical-results.md).
- Practical limits come first: no production deployment with customers has been demonstrated.
