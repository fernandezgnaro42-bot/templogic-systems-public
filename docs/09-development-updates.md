# Development updates

Short, dated notes on what changed. Longer entries are in the [development journal](../journal/).

## 2026-11-11 (correction)

- Corrected this documentation after a review of our engineering records. It had understated demonstrated work: Brújula images have booted on physical Dell computers (2026-10-09 technician image, 2026-10-26 personal image), Brújula runs as a service on development laptops, and Latenza has been operating on our own infrastructure with recorded events and phone notifications. See [milestones](08-engineering-milestones.md).
- Introduced evidence classes (laboratory verified, hardware verified, operationally observed, production validated). See [status labels](status-labels.md).
- Re-ran the test suites of Brújula, Praecura, Latenza and the ML laboratory in isolated copies.
- Completed the data recovery and validation stage of the ML laboratory ([results](10-research-and-technical-results.md)).
- Began publishing documentation in this repository.

## October 2026

- 2026-10-09: first Brújula image booted on a physical computer; Brújula running as a service on two laptops.
- 2026-10-12: Latenza running as a service on our own infrastructure.
- 2026-10-20 and 2026-10-26: images built for the three editions; the personal edition booted on a physical Dell Inspiron 15.
- Brújula Delta-T gained a connector to Praecura, a read-only building-system reader and a LoRa sensor protocol (all IN DEVELOPMENT).
