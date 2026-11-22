<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-CORE — repository foundation
-->

# Repository architecture

## Current executable tooling

**What it contains:** the repository's metadata, source-provenance, workflow, dependency-alignment, documentation, inventory and preflight controls.

**What each control does:** it inspects its fixed, declared local scope.

**What received metadata cannot do:** select another acceptance policy or grant domain authority.

Foundation qualification is in progress.

## Intended domain boundaries

| Record | Responsibility | Required evidence |
| --- | --- | --- |
| Common record envelope | Shared provenance, schema version, digest, data-class and licence wrapper carried by every platform record | Strict structural validation and deterministic canonical digesting |
| Entity reference | Typed, digest-pinned cross-repository identifier for designs, runs, lots, equipment and evidence | Unambiguous resolution without ambient mutable paths |
| Operation request and admission record | Requested operation, inputs, autonomy mode and the gate decision admitting or refusing execution | Verified facility readiness, licence admission, data-class ceiling and required approvals before any tool runs |
| Data handling profile | Data classes, confidentiality compartments, non-sealed training versus sealed evaluation pools, export-control flags and off-premises egress ceilings | Enclave network isolation for foundry-confidential material and human-reviewed in-enclave similarity scans before any downward release |
| Design view | Immutable snapshot of a circuit hierarchy, netlist or specification pinned by source, file-list and elaboration digests | Byte-exact digest agreement across every downstream consumer |
| Operation profile | Executable tool contract, pinned container or Nix environment digest, two-stage cancellation, licence isolation mode and mandatory no-model baseline | Separate-process isolation for copyleft tools and deterministic fallback when no model is promoted |
| Approval record | Distinction between an enrolled key-pinned person in a named role and an automated approver inside a bounded envelope, plus post-pilot audit hooks | Access-controlled signed-frame verification, digest-bound evidence summaries in application custody and five-outcome independent audit strata |
| Design-loop autonomy envelope | Per-operation capability level versus permitted operating level, budget caps and references to equipment input-surface clamps | Operating level never exceeding demonstrated capability level; paid runs, model training and pilot launch kept human-only |
| System architecture and budget specification | Top-to-block area, power, latency, noise and thermal budgets plus compositional assume-guarantee interface contracts | Solver-free algebraic budget structure checked by downstream sign-off |

## Licence isolation and air-gapped enclaves

- **Copyleft isolation.** Every `GPL`, `LGPL` or `AGPL` tool — including `OpenSTA`, `OpenROAD`, `KLayout`, `openEMS`, `Elmer`, `Netgen` and `ngspice` — runs strictly as a separate child process over file boundaries, never linked in-process.
- **Air-gapped confidential enclaves.** Foundry-NDA and secret-bearing operations execute inside network-isolated namespaces (`CLONE_NEWNET`) with zero outbound sockets, read-only process-design-kit mounts, enclave-confined encrypted scratch and an in-enclave or node-locked licence server by default. Any remote licence server requires an explicit owner exception restricted to the pinned daemon ports and logged with its metadata-channel residual.
- **Off-premises egress.** Payloads permitted up to an operation's egress ceiling go only to a named provider, account and region whose contract terms forbid training and retention, with deletion requests and responses logged.

## Person approvals and post-pilot approval auditing

- **Enrolled person-in-role identity.** A person approval counts only from an enrolled, key-pinned identity on an access-controlled hub requiring signed frames. All eleven physical, legal and rollback approval kinds default to automated delegation refused.
- **Load controls and digest-only summaries.** Opt-in per-role rate limits refuse excess new requests cleanly; approvals faster than a minimum review time or above a batch-size threshold carry attention-only flags (retroactive burst flags on earlier runs are labelled `approximation` and never enter the uniform sample). Only the summary digest crosses the coordination bus; exact summary bytes remain in application custody.
- **Two-stratum independent audit.** Starting after the first approved AI-driven pilot, an independent auditor evaluates two non-pooled strata per period with pre-declared seed and tolerance: (a) a uniform sample across approvals and rejections whose seed is revealed after period close, keeping every drawn item without redraw, and (b) every flagged item. Each audited item receives one of five closed outcomes — `supported`, `unsupported`, `insufficient_evidence`, `summary_missing` or `not_auditable`. The review trigger uses the Clopper-Pearson upper bound on stratum (a) counting all four non-supported outcomes, reported beside the approver-attributable bound (`unsupported` plus `insufficient_evidence`). Confidential enclave items are audited inside the enclave by an independent person, or by a local model whose agreement with a person auditor has been measured on a declared calibration set and reported (reported separately when that agreement is not established).

## Planned record schemas

- `circuit_core.envelope.v1`
- `circuit_core.entity_reference.v1`
- `circuit_core.operation_request.v1`
- `circuit_core.admission_record.v1`
- `circuit_core.data_handling_profile.v1`
- `circuit_core.design_view.v1`
- `circuit_core.operation_profile.v1`
- `circuit_core.approval_record.v1`
- `circuit_core.design_loop_autonomy_envelope.v1`
- `circuit_core.system_architecture_and_budget_spec.v1`

These are planned identifiers. None of them is registered or qualified here.

Read [validation tooling](validation-tooling.md) for the executable repository interfaces.
