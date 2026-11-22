<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-CORE — repository foundation
-->

# Architecture

## Current executable surface

The checkout contains:
- repository validation tooling;
- dedicated tests;
- workflow definitions;
- native documentation.

No domain component of Circuit Core is implemented yet. The metadata keeps domain capabilities, claims and qualified record formats empty.

## Intended data flow

1. **Operation profiles** declare each tool's pinned execution environment, licence class, cancellation behaviour and deterministic no-model baseline (a deterministic tool, a generator or high-level synthesis flow, or a recorded human procedure).
2. **Design views and system budgets** pin design sources, elaboration digests and hierarchical block budgets before any domain tool executes.
3. **Admission** checks each incoming operation request against facility readiness, material state, driver qualification, data-handling ceilings and required approvals.
4. **Approvals and summaries** record enrolled key-pinned person-in-role decisions on an access-controlled, signed-frame hub, keeping exact evidence-summary bytes in application custody at the highest data class of the summarised material.
5. **Model slot admission** binds promoted model envelopes only after slot-rights and deterministic-baseline checks pass, while keeping every operation runnable with no model.

## Ownership

**This project owns** the planned Circuit Core records and boundary rules.

**Owned elsewhere:**

| Responsibility | Owner |
|---|---|
| technology, board and leaf-cell profiles | Circuit Technology |
| directed-acyclic-graph scheduling and learning-record emission | Circuit Flow |
| equipment input-surface clamps and cell control | Circuit Automation |
| sign-off verdicts and acceptance plans | Circuit Acceptance |
| coordination transport, role ACLs and signed frames | SYNAPSE-CHANNEL |
| model training and promotion mechanics | DIRECTOR-AI |
| sealed evaluation custody | REMANENTIA |

## Interpretation

- **Approvals.** Key-and-role verification is not hardware proof of human presence.
- **Release scans.** Measured recall on planted excerpts does not exclude human-missed paraphrase.
- **Budgets.** Algebraic budget closure is not physical or electrical sign-off.

Read [the documentation architecture](docs/ARCHITECTURE.md) for the planned records, domain rules and schema identifiers.
