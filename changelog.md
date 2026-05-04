# CIFM Changelog

All notable changes to the Converged Infrastructure Forensics Model (CIFM) are documented in this file.

This project follows a structured versioning approach to preserve transparency, traceability, and evidentiary defensibility.

---

## v1.2.1RC — May 2026
### Added
- **Runtime-Spawned Workloads and Undeclared Execution Paths**
  - Clarifies how CIFM handles ephemeral workloads dynamically created by:
    - parent containers
    - CI/CD runners
    - job runners
    - entrypoint scripts
    - automation frameworks
    - privileged workloads
    - compromised workloads
  - Establishes that runtime-spawned workloads sometimes may not appear in the original compose file, deployment manifest, task definition, or declared orchestration configuration.

- Explicit distinction between:
  - **Declared State** — what the environment was intended to run
  - **Observed State** — what preserved telemetry proves actually ran
  - **Initiating Mechanism** — the process, identity, workload, or automation path that created the workload
  - **Origin Chain Confidence** — the degree to which the initiating mechanism can be corroborated

- Additional optional fields in the **UEM Ephemeral Workload Extension**:
  - Declared State Source
  - Observed State Source
  - Initiating Mechanism
  - Parent Workload / Job
  - Origin Chain Confidence

### Changed
- Clarified that behavioral reconstruction may proceed even when the orchestrator lacks a durable record of the initiating event.
- Clarified that reconstruction may rely on preserved runtime, node-level, registry, CI/CD, identity, and network telemetry rather than declared orchestration state alone.
- Clarified that the orchestrator may represent declared state or partial lifecycle state rather than a complete record of actual execution.
- Expanded visibility-gap handling for runtime-spawned workloads.

### Fixed
- Reduced ambiguity around workload provenance claims.
- Clarified that when an initiating mechanism cannot be corroborated, the origin chain must be marked as a visibility gap.
- Clarified that confidence in workload provenance must be reduced when the origin chain cannot be supported by preserved telemetry.

---

## v1.2RC — May 2026
### Added
- **Section 14: Ephemeral Workload Handling**
  - Formal treatment of ephemeral compute, including containers, serverless functions, CI/CD runners, transient workloads, and short-lived compute resources.
  - Definition of *ephemeral workload event* as the investigative unit.
- Explicit distinction between:
  - **Recovery** — artifact acquisition from persistent hosts
  - **Reconstruction** — telemetry-derived analysis when direct artifacts are unavailable
- **UEM Ephemeral Workload Extension**
  - Fields for container, serverless, task-level, and transient workload investigations.
  - Preservation status, visibility impact, and confidence impact tracking.
- Ephemeral workload integration across:
  - Visibility & Trust Boundary Matrix
  - Investigative Anti-Patterns
  - Forensic Readiness
  - Appendix A Field Guide
- Glossary entries:
  - Ephemeral Workload
  - Ephemeral Workload Event
  - Reconstruction

### Changed
- Strengthened language around evidentiary limits:
  - Reconstruction is bounded by preserved telemetry.
  - Visibility gaps must propagate into confidence and final narrative.
- Clarified that ephemeral workloads are **reconstructed, not recovered**.
- Refined UEM structure for ephemeral workload context, including resource hierarchy, identity, telemetry sources, and preservation status.

### Fixed
- Removed ambiguity in anti-pattern language regarding ephemeral artifact recovery.
- Standardized terminology across sections involving workload, event, reconstruction, telemetry, and confidence impact.

---

## v1.1RC — April 2026
### Added
- Integration of **Henriques et al. (2023)** and the Forensics and Compliance Auditing (FCA) framework.
- Formal positioning of CIFM as an investigative reconstruction layer above evidence collection infrastructure.
- Expanded forensic readiness discussion for IACS-adjacent environments.

### Changed
- Clarified the relationship between CIFM and FCA frameworks as complementary rather than competitive.
- Strengthened language around pre-incident evidence dependency and forensic-by-design infrastructure.

---

## v1.0RC — April 2026
### Added
- First structured Release Candidate.
- Core CIFM architecture:
  - identity-centric investigative model
  - telemetry-first evidence model
  - iterative reconstruction workflow
  - human-validated reasoning constraints
- **Unified Evidence Manifest (UEM)**
  - Canonical schema for cross-domain evidence normalization.
- **Human-in-the-Loop (HITL) Validation Tiers**
  - Tiered constraints on AI-assisted investigative analysis.
- **Visibility & Trust Boundary Matrix**
  - Pre-investigation assessment of telemetry availability, trust boundaries, and investigative confidence.
- Appendix A:
  - CIFM Incident Response Field Guide.

### Defined
- CIFM’s scope boundary:
  - reconstruction, not attribution
- Complementary relationship to:
  - MITRE ATT&CK
  - Diamond Model
  - Cyber Kill Chain
  - FACT

---

## v0.32 — March 2026
### Added
- Final pre-release draft prior to v1.0RC.
- Expanded workflow clarity and structure.
- Initial integration of:
  - UEM schema concepts
  - Visibility modeling
  - HITL constraints
  - attribution boundary framing

### Changed
- Refined investigative phases into a non-linear workflow.
- Improved alignment between narrative reconstruction and evidence normalization.

---

## v0.27 — March 2026
### Added
- Appendix A early field guide concepts.
- Initial references to UEM-Lite.

### Changed
- Improved structural coherence across sections.
- Early refinement of attribution boundary language.

---

## v0.20–v0.26 — March 2026
### Added
- Claim of Contribution section.
- Expanded Introduction and Abstract alignment.
- Early articulation of:
  - identity as investigative pivot
  - telemetry as primary evidence
  - iterative workflow model
  - investigative limitations and confidence constraints

### Changed
- Section restructuring and numbering consistency.
- Expansion of limitations and investigative constraints.

---

## v0.1–v0.19 — March 2026
### Initial Development Phase
- Core CIFM concept formation.
- Early drafts focused on:
  - converged infrastructure definition
  - cross-domain investigative challenges
  - limitations of host-centric forensics
  - need for identity-centric and telemetry-driven reconstruction
- Iterative expansion based on:
  - teaching environments
  - workshop feedback
  - practical reconstruction exercises
  - reviewer feedback

---

## Notes

CIFM is an evolving investigative framework refined through practitioner feedback, operational validation, peer review, and applied testing.

Version history is maintained to support:

- transparency in design decisions
- reproducibility of framework evolution
- traceability of major conceptual changes
- alignment with CIFM’s emphasis on evidentiary integrity
