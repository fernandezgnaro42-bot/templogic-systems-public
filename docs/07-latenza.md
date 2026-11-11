# Latenza

**Status: IN DEVELOPMENT**

Latenza is a small, self-hosted monitor for systems that must keep reporting in.

## Capabilities (IN DEVELOPMENT)

- Heartbeats: a job or device checks in; silence raises an alert.
- Uptime checks and certificate-expiry checks.
- Alerts through ntfy, Discord, Slack and email.
- A public status page and a private dashboard.
- A small command-line wrapper for jobs, and an embeddable widget.
- SQLite storage; Python 3.11 or newer.

## Verified (2026-11-11, laboratory software verification)

- Automated test suite: 109 tests pass, run in an isolated copy.
- Scope: software behaviour in a controlled environment.

## Not yet proven

Long-duration operation under customer load. No customer use is claimed.
