# Status labels and evidence classes

Every claim in this repository carries two things: a **maturity label** (how finished the work is) and, where it describes something that was run, an **evidence class** (how it was shown to work). They are not interchangeable.

## Maturity labels

| Label | Meaning |
|---|---|
| **IN DEVELOPMENT** | Being built. Parts exist and work; the whole is not finished. |
| **EXPERIMENTAL** | Tried on partial data or in a laboratory. Results are not evidence of field performance. |
| **PLANNED** | Intended. Not started, or not yet working. |

## Evidence classes

| Class | Meaning |
|---|---|
| **LABORATORY VERIFIED** | Confirmed by automated or controlled laboratory tests, on a stated date, version and scope. |
| **HARDWARE VERIFIED** | Installed, booted or executed on a physical computer. |
| **OPERATIONALLY OBSERVED** | Seen working during real operation, supported by logs, events, notifications or similar records. |
| **PRODUCTION VALIDATED** | Met defined requirements for sustained, reliable operation in its intended production environment. Nothing here has reached this class. |

Two qualifiers may be added:

- **HISTORICALLY DOCUMENTED**: shown in an earlier session and recorded in our engineering notes. It was not repeated for this document, and it is not presented as a new test.
- **NOT YET VERIFIED**: no evidence yet.

## Rules we follow

- Hardware verification does not establish production readiness. A successful boot of one edition or one build does not validate another edition or build.
- Laboratory testing is not the only valid evidence. A capability shown on physical hardware or in real operation is recorded as such.
- We do not claim what we have not shown, and we do not understate what we have.
- Every claim has a date and a scope. A test count describes software verification in a controlled environment, not accuracy in the field.
- Unknown means unsaid.
