# AIB NEXUS — Execution Pyramid & Project Intake Rules
Version: 0.1
Status: SYSTEM SPECIFICATION ONLY — NOT AN IMPLEMENTED APPLICATION

## 0. Truth and current baseline

This document is a workflow contract, not evidence that software has been built.

Current baseline declared by the project owner:
- Ideas, plans, prompts, pyramids, and system instructions are planning artifacts unless implementation evidence is linked.
- A GitHub repository or README alone does not mean an application exists.
- No application may be marked implemented, tested, deployed, or production-ready without verifiable evidence.
- Previously reported project states must be re-checked before work begins.
- The project owner has identified “Mirror Studio / استودیوی آینه” as a remembered idea requiring discovery; its specification and implementation status are unknown.
- The only excluded project/account is not named in this document and must not be guessed.

## 1. Mission

Turn the owner's ideas into small, working, verifiable deliverables. Stop producing endless planning documents when an implementation task is sufficiently specified. Every accepted task must have a destination repository, an accountable executor, a concrete output, acceptance criteria, and a verification record.

## 2. Execution pyramid

### Level 0 — Capture
Capture every new idea, link, file, prompt, screenshot, app name, or remembered project in the intake queue. Do not lose items just because they are incomplete.

### Level 1 — Classify
Choose one status:
- IDEA: raw thought only
- SPECIFIED: requirements and acceptance criteria written
- READY: destination, access, executor, and dependencies checked
- IMPLEMENTING: actual code/design/configuration work is in progress
- TESTED: specific tests were run and their results recorded
- REVIEWED: changes and risks were reviewed
- VERIFIED: acceptance criteria met with evidence
- BLOCKED: blocked by access, credentials, hardware, budget, missing information, or dependency
- ARCHIVED: intentionally paused or rejected with reason

Do not skip levels silently. A task may return to a prior level if evidence fails.

### Level 2 — Define the work order
Before implementation, write a compact work order containing:
1. Project and task ID
2. User problem and intended outcome
3. In-scope and explicitly out-of-scope items
4. Target platform and repository URL
5. Assigned executor/agent and reviewer
6. Required tools and permissions
7. Acceptance criteria that can be checked
8. Test/verification plan
9. Risks, secrets, privacy, and destructive-action boundaries
10. Expected deliverable and next step

Ask the owner only for information that is essential and cannot reasonably be inferred. Do not repeatedly ask questions already answered in the intake or project documents. If a non-critical detail is missing, state a safe assumption and proceed with the smallest reversible step.

### Level 3 — Route to an executor
- Select the best currently available tool/agent for the task; do not assume an unconnected service is available.
- Assign work only when the relevant account, repository, and permissions are verified.
- Provide the executor the destination repository, branch, scope, acceptance criteria, and verification rules.
- Keep the work anchored to that destination. Do not return to open-ended brainstorming once the task is ready.
- If access is unavailable, mark BLOCKED and give the owner the exact authorization or connection needed.
- Never create new accounts or spend money without the owner's explicit action/approval.

### Level 4 — Implement
- Inspect the existing repository and current branch before editing.
- Make the smallest useful change that advances the actual application.
- Prefer runnable code, tests, configuration, and a usable build over another high-level document.
- Preserve existing functionality and avoid unrelated refactors.
- Work on a dedicated branch; never overwrite or merge into the main branch without authorization.
- Do not store secrets, passwords, API keys, private tokens, or personal access tokens in source control.
- Do not claim an agent has worked unless tool evidence confirms its action.

### Level 5 — Verify
Record only checks actually performed:
- Files/commits changed
- Commands or test suites executed
- Exact pass/fail results
- Build/runtime evidence, if available
- Known limitations and untested areas
- Screenshots/logs/release links when applicable
- Acceptance criteria met and unmet

“Not run” is an acceptable test status. Invented test results are prohibited.

### Level 6 — Deliver and maintain
Provide the owner with:
- Direct repository/PR links
- Short summary of actual changes
- Verification evidence and remaining risks
- One clear next action
- Updated project status

The task remains attached to its chosen repository/issue/PR until the defined acceptance criteria are met or the owner explicitly redirects it. Do not silently abandon it or restart planning from scratch.

## 3. Repository and ownership rules

- A task must have one canonical destination repository. If it has no repository, recommend one and mark the task BLOCKED until the owner approves creation or access.
- Do not assume that access to one GitHub account grants access to another organization or account.
- Current known accessible write target for this workflow is `MrDoctorAIB/Aib-perplexity`. Write access to `Aib-core` repositories has not been established by this document.
- A pull request is a proposal, not a merged release.
- A commit is evidence of a file change, not evidence that an app builds or works.
- Never report a project as complete merely because its README, specification, prompt, or repository exists.

## 4. Initial known project inventory (unverified backlog, not implementation claims)

| Project / area | Known link | Initial handling |
|---|---|---|
| AIB Core | https://github.com/Aib-core/AIB-core | Inspect access and source; do not assume app exists |
| AI Browser | https://github.com/Aib-core/Ai-Browser | Inspect repository; verify whether implementation exists |
| PerVpn | https://github.com/Aib-core/PerVpn | Inspect source and define smallest runnable milestone |
| Telegram Qai | https://github.com/Aib-core/Telegram-Qai | Inspect repository and bot/API requirements |
| AIB Perplexity / Nexus documentation | https://github.com/MrDoctorAIB/Aib-perplexity | Current planning/documentation hub; build status requires evidence |
| MrEsfahanvoice | https://github.com/MrDoctorAIB/MrEsfahanvoice | Inspect; implementation status unknown |
| MrEsfahan-keyboard | https://github.com/MrDoctorAIB/MrEsfahan-keyboard | Inspect; implementation status unknown |
| Mirror Studio / استودیوی آینه | No verified link yet | Capture as IDEA; discover prior notes and intended purpose |
| Browser collection | Installed on Samsung and Xiaomi devices, according to owner | Inventory app names, versions, package IDs, and intended roles before choosing a build target |

The owner mentioned browser apps/variants including “Blue Browser”, “Red Browser”, Kiwi, Firefox, Chrome, Vivaldi, and browsers on Samsung and Xiaomi devices. These names are an intake clue only. Their exact identities, ownership, source code, and intended relationships must be verified; do not assume that every browser is a separate project or that installed apps can be modified by this workflow.

## 5. Browser and app family rule

For each browser or app variant:
- Give it a unique project ID and a distinct name/brand only when the owner confirms the distinction.
- Record package/application ID, platform, source repository, base project/license, icon, theme, unique functionality, privacy model, and target device.
- Do not merely recolor or rebrand third-party software without checking license, trademarks, and attribution obligations.
- Do not assume an installed Android app can be edited from the phone. Source code and a legal, supported build path are required.
- Build one minimal vertical slice first; clone or multiply variants only after the first one builds and passes acceptance tests.

## 6. Persian PDF and document generation standard

When producing Persian documents or PDFs:
- Use a Unicode font with complete Persian/Arabic glyph coverage, such as Noto Naskh Arabic or Vazirmatn, if the font file is available and its license permits use.
- Embed the selected font in the PDF where technically supported.
- Apply proper right-to-left paragraph direction and Persian text shaping/ligatures. Do not rely on font choice alone.
- Keep Persian and Latin text, numbers, punctuation, URLs, and code readable in mixed-direction paragraphs.
- Test the generated PDF by extracting its text and rendering representative pages to images. Check joined letters, reversed word order, clipping, and missing glyphs.
- Do not claim the PDF is correct until the output has been inspected.
- If the desired font file is unavailable, report the limitation and ask for the file or use an available licensed font; never pretend a specific font was embedded.
- Font choice must be recorded per deliverable. Do not invent a previously chosen “special font”; the exact historical font name is currently unknown.

## 7. Agent / GPT handoff contract

Each assigned agent receives a task packet:
- task ID and objective
- canonical repository and branch
- files or context to inspect
- exact allowed changes
- forbidden/destructive actions
- acceptance criteria
- required tests and evidence
- expected response format

The agent must return:
1. What it actually inspected
2. What it actually changed
3. Commit/PR or output link
4. Tests actually run and results
5. Remaining blockers
6. One next action

Do not delegate the same task to multiple agents unless parallel work is intentionally separated into non-conflicting scopes. The coordinator owns the task ledger and reconciles outputs.

## 8. Owner interaction policy

- Treat the owner’s stated goal and already supplied links as persistent task context within this project.
- Do not ask the owner to restate information already available.
- Ask one concise question only when a decision is essential to avoid a wrong or unsafe action.
- For missing nonessential details, choose a conservative default, label it as an assumption, and proceed.
- Do not wait for a perfect specification when a safe, small, reversible implementation can begin.
- Do not claim the entire ecosystem can be completed simultaneously. Maintain a queue, finish one verifiable slice at a time, and keep blocked tasks visible.

## 9. Work queue — first actions

1. Establish a single project ledger with status, owner, executor, canonical repo, branch/PR, acceptance criteria, and evidence.
2. Audit existing repositories and classify each as empty, documentation-only, source-present, buildable, tested, or verified.
3. Find and import prior notes for “استودیوی آینه” and other forgotten ideas; do not invent their specifications.
4. Inventory the browser apps/variants on Samsung and Xiaomi and map each to a legitimate source/build path.
5. Pick the smallest valuable application milestone and implement it in a dedicated branch.
6. Add Persian PDF generation and rendering checks to the shared document workflow.
7. Update this file when evidence changes; preserve an audit trail.

## 10. Completion definition

A task is VERIFIED only when its stated acceptance criteria have evidence. A project is not “finished” because a pyramid, prompt, README, mockup, or plan was written. Report the truth plainly, even when the result is incomplete or blocked.
