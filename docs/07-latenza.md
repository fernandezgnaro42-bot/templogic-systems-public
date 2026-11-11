# Latenza

**Status: IN DEVELOPMENT.** Operating continuously on the developer's own infrastructure; not offered for sale and not production validated for customers.

Latenza is a small, self-hosted monitor for systems that must keep reporting in.

## Capabilities

- Heartbeats: a job or device checks in; silence raises an alert.
- Uptime checks and certificate-expiry checks.
- Alerts through ntfy (in use), and webhook (Discord, Slack) and email (implemented; email not verified against a real server).
- A public status page and a private dashboard.
- A small command-line wrapper for jobs, and an embeddable widget.
- SQLite storage; Python 3.11 or newer.

## Evidence

| Capability | Class | Date | Scope | Limits |
|---|---|---|---|---|
| Running as a service since at least 2026-10-12, watching a local server application, a phone app endpoint, a web page and its certificate, a remote server, and four scheduled jobs through heartbeats | OPERATIONALLY OBSERVED | 2026-10-12 to date | Developer's own infrastructure. Service confirmed active on 2026-11-11. Further instances run on separate servers, as recorded in our notes | Own use only. No customer use |
| Recurring phone notifications delivered | OPERATIONALLY OBSERVED | From 2026-10-09 | ntfy to the developer's phone | Delivery is not retried when the network is down (known defect) |
| Recorded events: scheduled-job heartbeats reporting down and recovering (including a job exit code and later recovery), and an uptime check timing out on 2026-10-17 and recovering in 4 minutes 41 seconds | OPERATIONALLY OBSERVED | Oct to Nov 2026 | Event history in the service database, reviewed in an internal audit on 2026-11-06 | |
| Automated test suite: 109 tests | LABORATORY VERIFIED | 2026-11-11 | Isolated copy | 106 tests at the 2026-11-06 audit |

## Known defects (from our 2026-11-06 audit; status checked against later work where recorded)

- Alert delivery has no retry: an alert can be lost if the network is down at that moment.
- After a laptop wakes from sleep, uptime checks can briefly report false "down" before the network returns.

## Not yet shown

Sustained operation under customer load, email delivery against a real mail server, any production validation.
