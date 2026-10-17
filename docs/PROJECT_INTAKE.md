# Project Intake Registry — AIB Ecosystem

**Purpose:** Turn idea-and-prompt projects into scoped, verifiable work without pretending that a prompt is already a working product.

**Last inspected:** 2026-10-17  
**Repository for this registry:** `MrDoctorAIB/Aib-perplexity`  
**Rule:** This file records the visible repository state only. It does not claim access to private workspaces, external accounts, credentials, or unlinked agents.

## Operating contract

For every project, the coordinator must:

1. Inspect the supplied GitHub URL, repository metadata, default branch, files, issues, pull requests, and available automation.
2. Record the goal, target platform, user-facing behavior, constraints, acceptance criteria, and unresolved questions.
3. Classify the project as **idea-only**, **scaffolded**, **implementation in progress**, **needs verification**, or **verified**.
4. Create a small implementation plan and scoped issue(s). Do not label an idea or prompt as source code.
5. Implement on a dedicated branch, keeping changes minimal and reviewable.
6. Run the available tests, builds, linting, and security checks. Record exact commands and results; never invent evidence.
7. Open a pull request for review. Do not merge or change account security/billing settings without explicit approval.
8. Report blockers clearly, especially missing permissions, API keys, paid-plan requirements, or unavailable services.

## Initial repository inventory

The following is a first-pass inventory based on public repository metadata and root contents inspected on 2026-10-17. It is not a full code audit.

| Project | Repository | Observed starting state | Initial next step |
|---|---|---|---|
| AIB Core / Android Intelligence Bridge | https://github.com/Aib-core/AIB-core | Profile README only at repository root; no implementation verified | Define scope, architecture, and acceptance criteria |
| AI Browser | https://github.com/Aib-core/Ai-Browser | GitHub reports repository empty | Capture requirements, then scaffold a minimal app |
| PerVpn | https://github.com/Aib-core/PerVpn | README contains only project title | Define platform, threat model, and safe MVP |
| Telegram Qai | https://github.com/Aib-core/Telegram-Qai | GitHub reports repository empty | Define bot flows and required Telegram credentials |
| AIB NEXUS | https://github.com/MrDoctorAIB/Aib-perplexity | Documentation-first bootstrap; includes agent instructions and architecture docs; production implementation not verified | Maintain this registry and define the first verifiable milestone |
| MrEsfahan Voice | https://github.com/MrDoctorAIB/MrEsfahanvoice | GitHub reports repository empty | Define target platform, languages, and voice features |
| MrEsfahan Keyboard | https://github.com/MrDoctorAIB/MrEsfahan-keyboard | GitHub reports repository empty | Define input methods, language support, and Android requirements |

## External assistants and platforms

Potential tools named in the project brief: Canva, ScholarGPT, ChatGPT, Codex, Qwen, Perplexity, Manus, Copilot, Gemini, and others.

Treat these as **potential collaborators**, not as already connected or authorized. For each integration, record:
- official product and URL;
- whether a connector or account connection is actually available;
- required permissions and secrets (never store secrets in this repository);
- free-tier limits and any billing requirement;
- specific role, permitted actions, and verification method.

An assistant cannot complete an external account's profile, accept terms, enable billing, or grant itself permissions unless the user completes the required authorization flow.

## Project completion standard

A project is **verified** only when its acceptance criteria are met and the repository contains reproducible evidence appropriate to the project: source files, build/test results, security checks where applicable, and a reviewable change history.

**IDEA → SPECIFIED → IMPLEMENTED → TESTED → REVIEWED → VERIFIED**

No stage may be skipped by changing the status label alone.
