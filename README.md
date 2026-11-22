<!--
SPDX-License-Identifier: AGPL-3.0-or-later
Commercial license available
© Concepts 1996–2026 Miroslav Šotek. All rights reserved.
© Code 2020–2026 Miroslav Šotek. All rights reserved.
ORCID: 0009-0009-3560-0851
Contact: www.anulum.li | protoscience@anulum.li
CIRCUIT-CORE — repository foundation
-->

# Circuit Core

Circuit Core is being built as the domain-free contract, admission, data-handling and approval kernel imported by every other circuit platform repository. It defines how entities, design views, operation profiles, execution requests, admission decisions, data compartments, autonomy envelopes, person-in-role approvals and hierarchical chip budgets are represented and checked. This checkout contains repository validation tooling and documentation only. Full foundation qualification is in progress. There is no installed contract-kernel package, admission runner, approval verifier or qualified record schema.

Circuit Core is part of the **SC Neuromorphic Computing Systems** group (SC-NEUROMORPHIC-COMPUTING-SYSTEMS). The [group and project map](https://github.com/anulum/sc-neurocore/blob/main/docs/ecosystem.md) shows the whole programme and where this repository sits in it.

**What does not exist yet:**
- an admission, envelope or approval validator package;
- a registered runtime record schema;
- a provider manifest registry or approval summary store.

## Boundary

**What this project owns:**

| Record | Scope |
|---|---|
| Common record envelope | Shared provenance, schema version, digest, data-class and licence wrapper carried by every platform record |
| Entity reference | Typed, digest-pinned cross-repository identifier for designs, runs, lots, equipment and evidence |
| Operation request and admission record | Requested operation, inputs, autonomy mode and the gate decision admitting or refusing execution |
| Data handling profile | Data classes, confidentiality compartments, non-sealed training versus sealed evaluation pools, export-control flags and off-premises egress ceilings |
| Design view | Immutable snapshot of a circuit hierarchy, netlist or specification pinned by source, file-list and elaboration digests |
| Operation profile | Executable tool contract, pinned container or Nix environment digest, two-stage cancellation, licence isolation mode and mandatory no-model baseline |
| Approval record | Distinction between an enrolled key-pinned person in a named role and an automated approver inside a bounded envelope, plus post-pilot audit hooks |
| Design-loop autonomy envelope | Per-operation capability level versus permitted operating level, budget caps and references to equipment input-surface clamps |
| System architecture and budget specification | Top-to-block area, power, latency, noise and thermal budgets plus compositional assume-guarantee interface contracts |

**Static imports:** none. Circuit Core sits at the root of the acyclic static import graph and is imported by the other seventeen circuit repositories.

**Records read without importing domain code:**

| Source | Records consumed |
|---|---|
| Circuit Technology | facility readiness and technology profile references |
| Circuit Flow | run plans |
| Circuit Acceptance | acceptance reports for release and slot-rights gates |
| Circuit Automation | equipment profiles, cell profiles, state observations and safety-clamp envelopes |
| Circuit Learning | process model inventory slot bindings |
| Circuit Manufacturing | hardware bill-of-materials and provenance records |
| Circuit Workbench | workspace sessions and review views |

**Capability registration and handoffs:** Hosts the provider-manifest protocol that domain and specialist circuit repositories register against, and exposes the bridge target that SC-NC Bridges registers with.

**Explicit non-claims and operating boundaries:**
- It contains no circuit simulator, synthesis tool, layout engine, design-space explorer, process design kit, workflow dispatcher, manufacturing execution logic, legal classifier or model trainer.
- Its system architecture and budget specification is solver-free: domain verifiers compute physical figures, never Circuit Core.
- Every operation profile declares a deterministic no-model execution path so the entire platform is complete without machine-learning models.
- Message bodies on the coordination channel never carry approval authority; only digest-pinned records checked against enrolled role policies count.

## Current tooling

Repository controls inspect:
- metadata and source attribution;
- workflows and dependency alignment;
- native documentation and repository inventory;
- preflight orchestration.

Metadata declares architecture-only maturity with empty implemented domain capability and claim inventories.

- Use the exact environment in [Contributing](CONTRIBUTING.md).
- Full CI and preflight belong in CI or in an explicitly admitted pre-push environment.
- See [Validation](VALIDATION.md) for the maintained validation scope.

## Intended evidence

Every future domain artefact will carry the platform's common provenance envelope, its source and environment digests, its confidentiality compartment and its explicit verification boundary. None of the planned record schemas is registered or qualified by this foundation.

## Documentation and support

Read [Architecture](ARCHITECTURE.md), [support](SUPPORT.md), [security reporting](SECURITY.md) and [citation metadata](CITATION.cff).

**Not claimed:**
- a hosted service, released package or DOI;
- a public CI status;
- a performed simulation, hardware measurement or sign-off verdict.

## Licence

Source is licensed under [AGPL-3.0-or-later](LICENSE). A commercial licence is available through the contact in [NOTICE](NOTICE.md).

![ANULUM](docs/assets/anulum_logo_company.jpg)

![Fortis Studio](docs/assets/fortis_studio_logo.jpg)

## Text and data mining reservation
The rightsholder, Miroslav Šotek (ANULUM), expressly reserves the use of the
works in this repository for text and data mining, including the collection of
this content for, and its use in, training, fine-tuning or evaluating machine
learning and artificial intelligence models, in accordance with Article 4(3) of
Directive (EU) 2019/790 and the national provisions transposing it.

No permission for such use has been granted beyond what the licence in
`LICENSE` grants. This reservation does not change that licence: uses the
licence permits remain permitted on its terms, including its attribution and
share-alike conditions.

Reservation made on 2026-11-22. Requests for permission: contact the
rightsholder through the contact listed in this repository.
