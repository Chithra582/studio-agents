# EXPLAINABILITY — Contains Studio AI Agents Roster

> **Admissibility & Transparency Report for OpenGAP / Agent Passport**  
> *Agent Name:* Contains Studio AI Agents Roster (`studio-agents`)  
> *Specification:* OpenGAP v0.1.0  
> *Domain:* Developer Tools / Rapid Prototyping & Studio Agent Teamwork  

---

## 1. Overview & Operational Purpose
The **Contains Studio AI Agents Roster** provides an orchestrated suite of specialized AI agents representing key roles in modern digital product studios. It spans design, engineering, marketing, product management, operations, and quality assurance to accelerate rapid software development cycles.

Its operational purpose is to act as an on-demand, multi-disciplinary product team that transforms nascent product concepts into functional prototypes, polished user experiences, and viable go-to-market strategies with minimum friction.

---

## 2. How the Agent Decides (Decision-Making Logic)
Contains Studio AI Agents Roster operates across a deterministic, multi-stage decision pipeline:

```
[Stage 1: Department Routing] ──> [Stage 2: Specialist Selection] ──> [Stage 3: Task Scoping]
                                                                                │
                                                                                ▼
[Stage 6: Delivery Handover] <── [Stage 5: Cross-Review & QA] <── [Stage 4: Autonomous Execution]
```

### 2.1 Department Routing & Objective Classification
- **Decision:** Classify incoming user requests into primary functional domains (e.g., Engineering, Design, Marketing, Product).
- **Rules:** Match request keywords against departmental taxonomy; if cross-functional, establish a lead coordinator agent.

### 2.2 Specialist Selection & Context Framing
- **Decision:** Assign the task to the exact sub-agent persona (e.g., `rapid-prototyper`, `whimsy-injector`, `tiktok-strategist`).
- **Rules:** Inject the specialist's system instructions, tool permissions, and domain examples into working context.

### 2.3 Autonomous Execution & Craftsmanship
- **Decision:** Execute domain actions—writing code, composing copy, drafting design tokens—while adhering to studio quality standards.
- **Rules:** Restrict scope to the 6-day cycle MVP model; prefer standard modern toolchains and modular component architecture.

### 2.4 Cross-Review, QA & Delivery Handover
- **Decision:** Validate deliverables against quality criteria (linting, accessibility, brand tone) and summarize handoff status.
- **Rules:** Require QA and accessibility checks before finalizing code deliverables; produce structured handover summaries for human review.

---

## 3. Data & Privacy
| Data Category | Retention Policy | Third-Party Sharing | Storage Mechanism |
|---|---|---|---|
| Project Code & Prototypes | User Project Lifecycle | None | Local Git Repository |
| Brand Guidelines & Design Tokens | Permanent Project State | None | Local Style Markdown Files |
| Marketing Copy & Social Drafts | Campaign Duration | None | Local Output Directories |
| User Review Sentiment Analytics | Ephemeral (Analysis Session) | None | In-Memory Data Structures |

Contains Studio AI Agents Roster complies with operational security and privacy standards:
- **No Cloud Data Exfiltration:** All agent instructions, generated codebases, brand collateral, and marketing strategies remain strictly within the user's local workspace.
- **Epistemic Isolation:** Specialist agents communicate via explicit context summaries, preventing unintended cross-talk between isolated client project workspaces.
- **Sanitized Model Payloads:** Prompts sent to language models contain only project requirements and technical specifications, devoid of private secrets and API credentials.
- **Data Minimization:** Only relevant project briefs and active component code are loaded into context during specialist agent turns.

---

## 4. Known Limitations & Failure Modes
Reviewers, auditors, and users should note the following operational constraints:
1. Scope Creep in Rapid Prototypes
   - *Limitation:* User requests often expand to full enterprise feature sets beyond rapid 6-day MVP scopes.
   - *Mitigation:* The agent actively enforces scope constraints, recommending phased rollouts and focusing on 3-5 core user flows.
2. Cross-Channel Tone Mismatches
   - *Limitation:* Marketing copy generated for professional platforms like LinkedIn can sometimes leak into casual platforms like TikTok.
   - *Mitigation:* The agent isolates channel specialist roles (e.g., `tiktok-strategist` vs `twitter-engager`) with strict platform-specific style rules.
3. Third-Party API Deprecations
   - *Limitation:* Rapidly evolving third-party SDKs (AI, payments, auth) may undergo breaking changes.
   - *Mitigation:* The agent verifies current API documentation and relies on stable, widely adopted client libraries.
4. Subjective Brand Aesthetics
   - *Limitation:* Design nuances such as whimsy or brand humor are subjective and may diverge from specific founder tastes.
   - *Mitigation:* The agent provides multiple creative options (e.g., subtle vs bold) and iterates based on user steering.

---

## 5. Verification, Safety & Human Oversight
Contains Studio AI Agents Roster integrates multi-layer safety rails to ensure full human accountability and system integrity:
- **Real-Time Human Approval Gate:** Direct production deployment, financial expenditures, and public social posting mandate explicit human confirmation.
- **Emergency Session Interrupt:** Any running code execution, project scaffolding, or marketing pipeline can be terminated immediately on operator command.
- **Step Quota Guardrails:** Strict execution limits prevent runaway generation loops during automated prototyping and testing.
- **Structured Audit Logging:** Every agent handover, generated asset, and architectural decision is documented in structured markdown sprint logs.
