# CIFM Changelog

All notable changes to the Converged Infrastructure Forensics Model (CIFM) are documented in this file.

This project follows a structured versioning approach to preserve transparency, traceability, and evidentiary defensibility.

---

v1.5RC - June 2026
-----------------

### Added

* Added Section 9.3.3 (Shadow Systems, Shadow AI, and Reconstruction Debt), formalizing CIFM's treatment of ungoverned systems, shadow AI deployments, orphaned automation, non-human identity ownership gaps, blast radius drift, and investigative archaeology of ungoverned access.
* Added Design Principle 8.8 (Shadow Environment Awareness).
* Extended Section 9.1.1, Section 9.2, Section 12, and Section 13 with shadow environment and NHI investigative guidance.
* Added glossary entries for Non-Human Identity, Shadow AI, Shadow IT, and Shadow Processing.
* Added reference and acknowledgment for Niemi (2026).
* Added future work items for practitioner implementation worksheets and a minimum viable training lab.
* External review by Prof. Charlie Niemi (University of Tulsa / OCII) confirmed attribution and placement; no doctrinal revisions required.

---

v1.4RC - May 2026
-----------------

### Added

* Added Operational Observability and AI-Agent Telemetry guidance.
* Expanded Phase 3 telemetry correlation, UEM mapping, forensic readiness, investigative anti-patterns, Appendix B AI-driven incident handling, glossary, and references to clarify how OpenTelemetry-compatible and other AI-agent telemetry sources may inform reconstruction without being treated as self-authenticating proof.
* Added a taxonomy for agent traces, tool execution records, system logs, collector/backend records, and validated events, along with preservation and corroboration requirements for collector configuration, sampling, redaction, context propagation, timestamp provenance, downstream system-of-record validation, and provenance/integrity weighting.

---

v1.3RC — May 2026
-----------------

### Added

*   **Appendix B — Applying CIFM to AI-Driven Operational Incidents**
    
    *   Formalizes how CIFM applies when AI systems become part of the:
        
        *   initiating mechanism            
        *   propagation vector            
        *   decision-layer amplifier            
        *   authority or workflow intermediary            
        *   evidence chain            
        *   investigative risk surface
            
    *   Extends CIFM to incidents involving:
        
        *   autonomous agents            
        *   RAG pipelines            
        *   model-connected tools            
        *   AI-connected workflows            
        *   MCP servers, plugins, and connectors            
        *   AI-connected business systems
            
*   **AI-Driven Operational Incident UEM Extension**
    
    *   Adds optional AI-specific evidence fields to the UEM for:
        
        *   prompts and input context            
        *   model outputs            
        *   tool-call arguments and results            
        *   retrieval context and vector-store evidence            
        *   model metadata and configuration state            
        *   agentic workflow traces            
        *   delegated identities and approval paths            
        *   downstream business-system effects            
        *   visibility and reproducibility metadata
            
*   **Appendix B-1 — GTG-1002 Walkthrough Using CIFM v1.3RC**
    
    *   Provides a phase-by-phase CIFM walkthrough of a publicly reported AI-orchestrated campaign.
        
    *   Demonstrates application of CIFM across:
        
        *   infrastructure context assessment            
        *   identity and control-plane analysis            
        *   telemetry normalization            
        *   behavioral reconstruction            
        *   HITL-governed hybrid analysis            
        *   narrative reconstruction            
        *   attribution handoff
            
*   **Appendix B-2 — CIFM-AI Evidence Schema (UEM Extensions)**
    
    *   Defines structured AI-specific evidence categories for:
        
        *   prompt and session context            
        *   model output and tool invocation            
        *   model metadata            
        *   RAG and retrieval evidence            
        *   agentic workflow evidence            
        *   identity and delegation evidence            
        *   ephemeral workload evidence            
        *   downstream system impact            
        *   confidence and visibility metadata
            
*   **New glossary terms**
    
    *   **AI-Driven Operational Incident**
        
    *   **Actor-Adjacent Control Surface**
        
    *   **AI Evidence Chain**
        
*   **Expanded AI forensic-readiness requirements**
    
    *   Adds explicit preservation guidance for:
        
        *   prompts and inputs            
        *   model outputs            
        *   retrieval context            
        *   tool-call logs            
        *   delegated identity records            
        *   approval paths            
        *   downstream system-of-record changes
            
### Changed

*   **Section 6 — Related Work and Prior Art**
    
    *   Expanded the treatment of AI-enabled systems as evidence sources.
        
    *   Added explicit reference to Appendix B as operational guidance for AI-driven operational incidents.
        
*   **Section 9.3.1 — Unified Evidence Manifest (UEM)**
    
    *   Updated to include the **AI-Driven Operational Incident UEM Extension** alongside the existing Ephemeral Workload Extension.
        
*   **Section 13 — Forensic Readiness in Converged Environments**
    
    *   Strengthened AI-related readiness guidance beyond model metadata alone.
        
    *   Clarified that operational AI evidence must include prompts, outputs, retrieval context, tool activity, delegated authority, approval paths, and downstream effects where available.
        
*   **Section 16.5 — Hybrid Intelligence Risks**
    
    *   Expanded to address incidents where AI systems are both:
        
        *   part of the evidence chain            
        *   and part of the investigative workflow
            
    *   Extended HITL constraints to AI-linked evidence sources, retrieval pipelines, tool invocations, and AI-assisted reconstruction.
        
*   **Visibility and confidence handling**
    
    *   Extended CIFM’s visibility-bounded confidence logic to AI-driven incidents involving:
        
        *   provider-side opacity            
        *   missing retrieval logs            
        *   unavailable model internals            
        *   incomplete orchestration traces            
        *   non-reproducible outputs
            
*   **Identity and control-plane analysis for AI-mediated activity**
    
    *   Reinforced that AI-driven incidents should still be anchored in:
        
        *   delegated authority chains            
        *   service accounts and temporary credentials            
        *   approval and override state            
        *   authorization scope            
        *   downstream system-of-record actions
            
### Fixed

*   Reduced ambiguity around how CIFM applies to AI-driven operational incidents without creating a separate forensic doctrine.
    
*   Clarified that prompts alone are insufficient to establish causality.
    
*   Clarified that the relevant AI evidentiary chain is:
    
    *   input
    *   model/retrieval context
    *   output
    *   tool/action path
    *   identity authority
    *   downstream effect
    *   corroborating telemetry
        
*   Clarified that AI systems should be treated as **actor-adjacent control surfaces** rather than presumed independent actors.
    
*   Clarified that AI-generated summaries cannot substitute for primary evidence.
    
*   Clarified that when provider-side telemetry, retrieval state, model internals, or tool-execution traces are unavailable, those gaps must be documented and carried forward as confidence impacts.
    
*   Clarified evidence weighting expectations by prioritizing:
    
    *   server-side logs
    *   signed audit trails
    *   preserved API records
        
    *   authoritative workflow recordsover:
        
    *   screenshots
    *   copied text
    *   recollections
    *   AI-generated summaries
    *   reconstructed transcripts

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
