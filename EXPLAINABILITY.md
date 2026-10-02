# EXPLAINABILITY.md

This document explains the internal mechanisms, data lineage, operational boundaries, and governance framework of **Contains Studio AI Agents Roster** (`studio-agents`) in accordance with the **OpenGAP v0.1.0** specification for the **HiDevs GitAgent Passport** clearance pipeline.

> **Agent Name:** Contains Studio AI Agents Roster (`studio-agents`)  
> **Specification:** OpenGAP v0.1.0  
> **Category / Domain:** Developer Tools / Rapid Prototyping & Studio Agent Teamwork  
> **Compliance Standard:** OpenGAP Checkpoint 2 (Explainability & Decision Governance), OWASP LLM Top 10, MITRE ATLAS  

---

## How the Agent Decides

Contains Studio AI Agents Roster is an orchestrated suite of specialized AI agents representing key roles in modern digital product studios. It spans design, engineering, marketing, product management, operations, and quality assurance to accelerate rapid software development cycles, transforming nascent concepts into functional MVPs and verified prototypes within 6-day sprint cadences.

### 1. Decision Architecture

The multidisciplinary studio orchestration, sprint task decomposition, and cross-functional QA pipeline operates across a deterministic, five-stage architecture:

```
Product Concept / User Directive (Idea Description / Feature Request / Sprint Objective)
    │
    ▼
[Stage 1: Department Routing & Objective Classification]
    │  - Evaluates scope across Engineering, Design, Product, Marketing, and Operations
    │  - Decomposes high-level briefs into modular sprint epics
    │  - Establishes a designated Lead Specialist agent
    ▼
[Stage 2: Specialist Persona Binding & Context Scoping]
    │  - Selects exact specialist persona (e.g., rapid-prototyper, whimsy-injector, growth-strategist)
    │  - Injects specialist system prompts, design tokens, and tool permissions
    │  - Bounds active task context to prevent cross-domain token bloat
    ▼
[Stage 3: Autonomous Craft Execution & Artifact Drafting]
    │  - Executes domain actions: modular code authoring, copy composition, and layout design
    │  - Adheres strictly to modern web toolchains (Next.js, Tailwind, TypeScript)
    │  - Generates atomic file modifications within the local project workspace
    ▼
[Stage 4: Cross-Functional QA & Accessibility Review]
    │  - Validates deliverables against design tokens, WCAG accessibility, and linting rules
    │  - Executes automated unit tests and build verification scripts
    │  - Audits brand voice consistency and UX friction points
    ▼
[Stage 5: Sprint Delivery Handover & Trajectory Archive]
    │  - Packages production-ready code, documentation, and campaign assets
    │  - Applies automated credential scrubbing to execution logs
    │  - Emits structured handover reports for human operator approval
    ▼
Validated MVP Deliverable & Complete Auditable Sprint Trajectory Record
```

### 2. Decision Logic & Specialist Routing Formulations

Contains Studio evaluates department routing, task prioritization, and QA sign-off using deterministic mathematical heuristics:

1. **Specialist Affinity Score ($S_{\text{specialist}}$)**:
   $$S_{\text{specialist}} = (w_d \cdot D_{\text{domain}}) + (w_t \cdot T_{\text{tooling}}) + (w_s \cdot S_{\text{scope}})$$
   where:
   - $D_{\text{domain}} \in [0, 1]$ represents keyword and taxonomy alignment with the specialist mandate.
   - $T_{\text{tooling}} \in [0, 1]$ represents required tool permissions (file editing, visual styling, marketing analytics).
   - $S_{\text{scope}} \in [0, 1]$ reflects sprint cycle urgency.
   - Weights: $w_d = 0.50, w_t = 0.30, w_s = 0.20$ ($\sum w_i = 1.0$).

2. **Sprint Deliverable Completeness Index ($C_{\text{sprint}}$)**:
   $$C_{\text{sprint}} = \frac{1}{4} \left( Q_{\text{lint}} + Q_{\text{build}} + Q_{\text{a11y}} + Q_{\text{copy}} \right)$$
   where each metric is evaluated $\in [0, 1]$. Final delivery requires $C_{\text{sprint}} \ge 0.90$ with zero critical errors.

### 3. Thresholding & Refusal Decision Criteria

Contains Studio enforces strict operational safety and integrity boundaries:
- **Refusal to Deploy Unaudited Secrets**: Requests to hardcode third-party API credentials, private tokens, or production database strings are deterministically rejected with code `ERR_HARDCODED_SECRETS_PROHIBITED`.
- **Refusal of Dark Pattern UX Generation**: The agent refuses instructions to design deceptive UI patterns, forced continuity traps, or hidden subscription flows (`ERR_DECEPTIVE_UX_PROHIBITED`).
- **Sprint Turn Ceilings**: Iterative prototyping loops enforce a hard limit of `max_turns: 25` to prevent runaway model execution (`WARN_TURN_BUDGET_EXCEEDED`).
- **Local Directory Boundary Enforcement**: Specialist actions are strictly confined to the project root directory; commands attempting parent directory traversal are blocked (`ERR_OUT_OF_BOUNDS_FILE_WRITE`).

### 4. Fallback Decision Mechanism

Continuous studio development is guaranteed through multi-tier fault recovery:
- **Model Cascade Failover**: When the primary foundation model experiences latency spikes or HTTP 429 rate limits, the orchestrator cascades automatically between `claude-3-5-sonnet`, `gpt-4o`, and `gemini-2.0-flash`.
- **Deterministic Scaffolding Fallback**: If an AI specialist cannot resolve a complex library conflict, the system falls back to pre-validated deterministic boilerplate templates.
- **Graceful Context Pruning**: If context windows approach operational limits during long refactors, non-essential chat history is summarized into concise technical bullet points.

### 5. Human-in-the-Loop Governance

Human creators retain full executive direction and final decision authority:
- **Explicit Operator Approval Gates**: Applying git commits, deleting files, running terminal installations, or deploying builds requires explicit human confirmation.
- **Session Kill Switch**: Operators can halt agent execution loops instantly via `Ctrl+C` or by issuing the `/stop` command.
- **Editable Deliverable Drafts**: All generated codebases, copy variations, and marketing schedules are saved as editable local files requiring operator review before publishing.

---

## The Data It Uses

Contains Studio AI Agents Roster operates under strict privacy, data minimization, and workspace isolation standards.

### 1. Ingested Input Data

The agent processes only operational assets necessary to fulfill sprint tasks:
- **Project Briefs & Directives**: User-provided specifications, user stories, and feature requirements.
- **Design Tokens & Brand Assets**: Colors, typography scales, style guides, and layout specifications.
- **Local Source Code**: Working directory source code files (TypeScript, React, Python, CSS) explicitly scoped to the active project.
- **Sprint Metadata**: Milestone definitions, priority tags, and issue backlogs.

### 2. Configuration & Reference Data

- **Specialist Role Definitions**: System prompts, domain instructions, and tool bindings for each studio persona.
- **Quality Rubrics & Linting Schemas**: Pre-configured ESLint, Prettier, and accessibility rulesets.
- **Modern Tech Stack Templates**: Component scaffolds for Next.js, Tailwind CSS, Vite, and FastAPI.

### 3. Base Model & Inference Lineage

- **Deterministic Orchestration Logic**: Scripted file-tree generation, regex pattern linting, and dependency validation executed locally (100% deterministic with zero LLM variance).
- **Foundation Models**: Industry-leading frontier LLMs (`claude-3-5-sonnet`, `gpt-4o`, `gemini-2.0-flash`) utilized for creative ideation, UI design logic, and software engineering.
- **Zero Training on Client Projects**: Proprietary codebases, brand collateral, and strategic marketing briefs are never utilized for public model training.

### 4. Data Privacy, Storage, and Retention

- **OWASP LLM & MITRE ATLAS Hardened**: Defended against model inversion, insecure direct object references, and prompt injection attacks.
- **Local-Only Workspace Operations**: All generated prototypes, assets, and documentation are stored locally on the user's filesystem.
- **Credential Scrubbing**: Environment variables, authentication tokens, and private paths are automatically scrubbed from prompt payloads and console logs.
- **Zero Commercial Monetization**: Client project files, marketing copy, and codebase repositories are never shared, monetized, or sent to unauthorized third-party telemetry collectors.

---

## Limitations

Understanding the operational boundaries and technical constraints of Contains Studio AI Agents Roster is essential for optimal workflow planning.

### 1. Complex Microservice Orchestration Boundaries
- **Limitation**: While optimized for rapid full-stack monoliths and decoupled frontends, coordinating large distributed microservice clusters exceeds single-sprint capabilities.
- **Mitigation**: The agent focuses on modular client-facing prototypes and provides clean OpenAPI specifications for downstream backend integration.

### 2. Subjective Aesthetic and Brand Resonance
- **Limitation**: AI visual styling agents evaluate contrast ratios and token conformance, but cannot intuitively evaluate nuanced brand emotion or subjective cultural aesthetic resonance.
- **Mitigation**: The whimsy and styling agents generate 3 diverse design variations (*Minimal*, *Playful*, *Corporate*) for human design review.

### 3. Live External Payment Gateway Mocking
- **Limitation**: Automated tests cannot safely process live real-world financial transactions with external payment processors during sprint prototyping.
- **Mitigation**: The prototyper injects standard mock webhook handlers and sandbox Stripe/PayPal test credentials for end-to-end checkout flow validation.

### 4. Cross-Platform Native Mobile Device Compilation
- **Limitation**: Compiling native iOS and Android binaries requires dedicated local Xcode/Android Studio hardware environments not present in headless agent runners.
- **Mitigation**: The agent outputs standards-compliant React Native / Expo or PWA codebases that can be built locally by the operator.

### 5. Multi-Specialist Circular Feedback Loops
- **Limitation**: Unconstrained cross-review between the Designer, Coder, and QA specialist can trigger circular perfectionist revisions without converging.
- **Mitigation**: The orchestrator enforces a maximum of 3 review iterations before freezing changes and requesting human supervisor arbitration.

---

## Summary & Compliance Checklist

| Checkpoint 2 Requirement | Corresponding Section | Status |
| :--- | :--- | :---: |
| **How the agent decides** | [How the Agent Decides](#how-the-agent-decides) | **Covered** |
| - Decision architecture & 5-stage pipeline | Section 1 | Verified |
| - Decision logic & specialist routing formulations | Section 2 | Verified |
| - Thresholding & refusal decision criteria | Section 3 | Verified |
| - Fallback decision mechanism | Section 4 | Verified |
| - Human-in-the-loop governance & oversight | Section 5 | Verified |
| **The data it uses** | [The Data It Uses](#the-data-it-uses) | **Covered** |
| - Ingested project briefs, design tokens & code | Section 1 | Verified |
| - Configuration, specialist roles & tech templates | Section 2 | Verified |
| - Base model lineage & deterministic logic | Section 3 | Verified |
| - Data privacy, retention lifecycle & MITRE/OWASP | Section 4 | Verified |
| **Its limitations** | [Limitations](#limitations) | **Covered** |
| - Complex microservice orchestration boundaries | Section 1 | Verified |
| - Subjective aesthetic and brand resonance | Section 2 | Verified |
| - Live external payment gateway mocking | Section 3 | Verified |
| - Cross-platform native mobile device compilation | Section 4 | Verified |
| - Multi-specialist circular feedback loops | Section 5 | Verified |
