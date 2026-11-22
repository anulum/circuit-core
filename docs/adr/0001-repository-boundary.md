<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-CORE — repository foundation
-->

# Decision: isolate a domain-free contract, admission and approval kernel at the root of the import graph

## Context

Seventeen circuit design, specialist, laboratory, manufacturing and workbench repositories share one model of identity, data classification, tool licensing, autonomy envelopes and human approvals. Embedding any solver, process design kit or workflow runner in that shared root would create cyclic dependencies and couple authority checks to domain toolchains.

## Decision

**What Circuit Core owns:**
- common record envelope;
- entity reference;
- operation request and admission record;
- data handling profile;
- design view;
- operation profile;
- approval record;
- design-loop autonomy envelope;
- system architecture and budget specification;

**What it imports:** none. Circuit Core sits at the root of the acyclic static import graph and is imported by the other seventeen circuit repositories.

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

## Consequences

**What can be qualified now:** repository governance and validation tooling, before domain code exists.

**What it cannot qualify:** unimplemented schemas, solvers, hardware or sign-off verdicts.

**Architectural consequences:**
- every circuit repository imports one small, acyclic, solver-free contract kernel;
- every operation profile carries a deterministic no-model path and explicit separate-process isolation for copyleft tools;
- confidentiality compartments, air-gapped enclaves and enrolled person-in-role approvals follow one uniform rule set before any domain code runs.
