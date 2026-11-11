# Engineering milestones

Each row says what was shown, when, how, and the limits. Evidence classes are defined in [status labels](status-labels.md). Rows marked HISTORICALLY DOCUMENTED come from our dated engineering records and were not repeated for this page.

## Current verification (2026-11-11, isolated copies)

| Item | Result | Class | Limits |
|---|---|---|---|
| Brújula automated tests | 635 pass | LABORATORY VERIFIED | One timing-sensitive serial-port test failed once under heavy parallel load and passed 3 of 3 alone |
| Brújula guardian (Rust) | 15 pass | LABORATORY VERIFIED | Unit tests |
| Praecura automated tests | 115 pass | LABORATORY VERIFIED | |
| Latenza automated tests | 109 pass | LABORATORY VERIFIED | |
| Oricalco project checks | Pass | LABORATORY VERIFIED | Code-level only |
| ML laboratory tests | 80 pass | LABORATORY VERIFIED | |
| Brújula and Latenza services active on the development laptop | Active | OPERATIONALLY OBSERVED | Checked 2026-11-11 |
| Current personal-edition image file matches its recorded checksum | Match | LABORATORY VERIFIED | Links the file to the 2026-10-26 hardware boot below |

## Earlier results

| Date | Item | Class | Limits |
|---|---|---|---|
| 2026-10-09 | Brújula running as a self-restarting service on two laptops; real phone notices including a temperature rule during real overheating | OPERATIONALLY OBSERVED, HISTORICALLY DOCUMENTED | Own use |
| 2026-10-09 | Technician image (v0.5) booted from USB on a physical Dell; sensor defect found and fixed; new image booted the same night and read temperature | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | Earlier build; not installed to disk |
| 2026-10-09 | Image booted in virtual machines in BIOS and UEFI modes, including with Secure Boot on | LABORATORY VERIFIED, HISTORICALLY DOCUMENTED | |
| 2026-10-12 onward | Latenza running as a service, with recurring phone notifications and recorded heartbeat and uptime events | OPERATIONALLY OBSERVED | Own use; known defects on [Latenza](07-latenza.md) |
| 2026-10-20 | General-edition image built and tested in virtual machines | LABORATORY VERIFIED, HISTORICALLY DOCUMENTED | No physical boot recorded |
| 2026-10-26 | Personal-edition image booted from USB on a physical Dell Inspiron 15; Wi-Fi, web and menu worked | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | Live session only |
| 2026-10-26 | Technician and personal images rebuilt | LABORATORY VERIFIED (build) | Physical boot of the rebuilt technician image not recorded |

## Not milestones yet

Production validation of any product, customer deployments, field accuracy of any model, real-site building-system reads, radio firmware on hardware, installation of an image to disk, a physical boot of the general-edition image.

## Corrections

An earlier version of this page said real-hardware booting had not been demonstrated. That was wrong: see the 2026-10-09 and 2026-10-26 rows. It also described verification as laboratory-only and Latenza as unproven in operation. This page now separates the evidence classes. Test counts on our website are out of date; this page is current as of its date.
