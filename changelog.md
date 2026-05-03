# CIFM Changelog

All notable changes to the Converged Infrastructure Forensics Model (CIFM) are documented in this file.

This project adheres to a structured versioning approach for transparency, traceability, and evidentiary defensibility.

---

## v1.2RC — May 2026
### Added
- **Section 14: Ephemeral Workload Handling**
  - Formal treatment of ephemeral compute (containers, serverless, CI/CD runners, transient workloads)
  - Definition of *ephemeral workload event* as the investigative unit
- Explicit distinction between:
  - **Recovery** (artifact acquisition)
  - **Reconstruction** (telemetry-derived analysis)
- **UEM Ephemeral Workload Extension**
  - Fields for container/serverless/task-level investigations
  - Preservation status, visibility impact, and confidence impact tracking
- Ephemeral workload integration across:
  - Visibility & Trust Boundary Matrix (Section 9.1.1 reference)
  - Investigative Anti-Patterns (Section 12)
  - Forensic Readiness (Section 13)
  - Appendix A (Field Guide updates)
- Glossary entries:
  - Ephemeral Workload
  - Ephemeral Workload Event
  - Reconstruction

### Changed
- Strengthened language around evidentiary limits:
  - Reconstruction bounded by preserved telemetry
  - Visibility gaps must propagate into confidence and narrative
- Clarified that ephemeral workloads are **reconstructed, not recovered**
- Refined UEM structure for ephemeral context (resource hierarchy, identity, telemetry sources)

### Fixed
- Removed ambiguity in anti-pattern language regarding ephemeral artifact recovery
- Standardized terminology across sections (workload, event, reconstruction, telemetry)

---

## v1.1RC — April 2026
### Added
- Integration of **Henriques et al. (2023)** (FCA framework)
- Formal positioning of CIFM as:
  - Reconstruction layer above evidence collection infrastructure
- Expanded **Forensic Readiness (Section 13)**:
  - IACS evidence collection considerations
  - Cloud-native telemetry persistence alignment

### Changed
- Clarified relationship between CIFM and FCA frameworks (complementary, not competitive)
- Strengthened language around pre-incident evidence dependency

---

## v1.0RC — April 2026
### Added
- First structured Release Candidate
- Core CIFM architecture:
  - Identity-centric investigative model
  - Telemetry-first evidence model
  - Iterative reconstruction workflow
- **Unified Evidence Manifest (UEM)**
  - Canonical schema for cross-domain normalization
- **Human-in-the-Loop (HITL) Validation Tiers**
  - Tiered constraints on AI-assisted analysis
- **Visibility & Trust Boundary Matrix**
  - Pre-investigation confidence and telemetry assessment
- Appendix A:
  - CIFM Incident Response Field Guide

### Defined
- CIFM scope boundary:
  - Reconstruction, not attribution
- Explicit separation from:
  - MITRE ATT&CK
  - Diamond Model
  - Cyber Kill Chain
  - FACT (complementary relationship)

---

## v0.32 — March 2026
### Added
- Final pre-release draft prior to v1.0RC
- Expanded workflow clarity and structure
- Initial integration of:
  - UEM schema concepts
  - Visibility modeling
  - HITL constraints

### Changed
- Refined investigative phases into non-linear workflow
- Improved alignment between narrative reconstruction and evidence normalization

---

## v0.27 — March 2026
### Added
- Appendix A (early field guide concepts)
- Initial references to UEM-Lite

### Changed
- Improved structural coherence across sections
- Early refinement of attribution boundary language

---

## v0.20–v0.26 — March 2026
### Added
- Claim of Contribution section
- Expanded Introduction and Abstract alignment
- Early articulation of:
  - Identity as investigative pivot
  - Telemetry as primary evidence
  - Iterative workflow model

### Changed
- Section restructuring and numbering consistency
- Expansion of limitations and investigative constraints

---

## v0.1–v0.19 — March 2026
### Initial Development Phase
- Core concept formation of CIFM
- Early drafts focused on:
  - Converged infrastructure definition
  - Cross-domain investigative challenges
  - Limitations of host-centric forensics
- Iterative expansion based on:
  - Teaching environments
  - Workshop feedback
  - Practical reconstruction exercises

---

## Notes

- CIFM is an evolving framework and is refined through:
  - Practitioner feedback
  - Real-world validation
  - Cross-domain investigative use

- Version history is maintained to ensure:
  - Transparency in design decisions
  - Reproducibility of framework evolution
  - Alignment with CIFM’s emphasis on evidentiary integrity
