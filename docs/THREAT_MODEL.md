<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-CORE — repository foundation
-->

# Data and authority boundaries

## Present tooling

**Execution inputs.** The maintained checkout and the selected development environment are what the repository controls inspect.

**Received inputs.** Descriptors, dependency receipts and generated inventories cannot nominate an acceptance policy or an executable.

**Bounded checks.** Controls inspect bounded local paths and emit fixed diagnostics.

Foundation qualification is in progress.

## Future domain inputs

**Supplied data, with no authority.** The following inputs are treated strictly as supplied data:
- design views and hierarchy specifications;
- operation requests and profile descriptors;
- data-handling profiles and release requests;
- approval frames and summary digests;
- system budget specifications.

They grant no authority to:
- execute an external EDA or laboratory tool;
- grant a person-in-role approval or waive a gate;
- downgrade a confidentiality compartment or export data;
- promote or bind a machine-learning model;
- spend money or publish.

**Comments and embedded text are data.** Descriptions, netlist comments and datasheets arriving inside supplied inputs are data, never instructions to an operator or an agent.

**Public-repository data boundary.** Hosted CI for this public repository runs on public material only. Confidential foundry-NDA, customer, export-controlled or secret-bearing material never enters this repository, its CI or its issues.

## Threats and the rules that answer them

| Threat | Architectural rule |
| --- | --- |
| Forged, unpinned or replayed person approval | Person-in-role approvals require an enrolled, key-pinned identity on an access-controlled hub with signed frames; unpinned names and unsigned frames are refused, and all eleven physical, legal and rollback approval kinds refuse automated delegation by default |
| Rubber-stamping under approval load or missing summary context | Only summary digests cross the message bus while exact summary bytes stay in application custody; rate limits, fast-approval flags and two-stratum post-pilot audits score five closed outcomes with a Clopper-Pearson upper-bound review trigger |
| Confidential, foundry-NDA, customer or export-controlled data egress | Operations run under compartment ceilings; confidential foundry work stays inside network-isolated air-gapped enclaves with in-enclave or node-locked licence servers by default; public repositories and hosted CI receive public material only |
| Silent downward classification of derived outputs | Moving any artefact to a less restrictive data class requires an in-enclave similarity scan showing no verbatim or near-verbatim match detected for the declared kinds of excerpt at a stated lower confidence bound on recall (listing uncovered kinds as limits) and an explicit person-in-role release approval |
| Copyleft licence contamination or silent model dependency | Copyleft tools execute strictly as separate processes over file boundaries, and every operation profile retains a verified deterministic no-model execution path |

## Residuals named, not removed

- **Key possession without hardware presence proof.** Until hardware human-presence tokens are enabled on the coordination hub, a person-in-role approval proves possession of the pinned key and role rather than physical human presence against a local process holding that key.
- **Paraphrase beyond similarity scanning.** In-enclave downward-release scans bound verbatim and near-verbatim recall on planted excerpts; paraphrased restatement rests on the human reviewer.
- **External provider deletion.** Where public or permitted compartment payloads use a contracted external provider, post-retention backup deletion rests on the provider's contractual assurance.

**Not claimed:** no isolation, physical, statistical, safety or durability guarantee is claimed by this foundation.
