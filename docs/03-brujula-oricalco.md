# Brújula Oricalco

**Status: IN DEVELOPMENT.** Booted on physical hardware in a live session; not installed, not production validated.

Oricalco is the personal edition of [Brújula](02-brujula.md): a desktop image for an individual's own computer, with no listening network services, clear explanations and no hidden owner.

## Evidence

| Capability | Class | Date | Scope | Limits |
|---|---|---|---|---|
| Personal-edition image (version 0.5) booted from a USB drive on a physical Dell Inspiron 15, live, without touching the installed system. Wi-Fi worked, web pages loaded, and the menu items for status, black box and Wi-Fi worked | HARDWARE VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-26 | One physical computer. The USB checksum equals the image checksum recorded then, and the image file that exists today has the same checksum (9198f9ec...) | Live session only. Sound, screen details and the app store were not reported. No disk installation |
| The same image started in a virtual machine: Spanish interface, Brújula active, no listening network ports (file, print, discovery and remote-login services off) | LABORATORY VERIFIED, HISTORICALLY DOCUMENTED | 2026-10-26 | Virtual machine | |
| Defects found on the physical computer (two misleading messages) | Corrected in code the same day | 2026-10-26 | Will appear in the next image build | The corrections are not in the image above |
| Repository checks of the standalone Oricalco project | LABORATORY VERIFIED | 2026-11-11 | Isolated copy; code-level checks only | Virtual-machine and security-service parts not validated in that run |

## Not yet shown

- Installation to disk (the image runs live from USB).
- Boot on other computers, long-duration use, production use.
- A standalone Oricalco distribution separate from the Brújula image. Licensing and distribution terms are not decided.
