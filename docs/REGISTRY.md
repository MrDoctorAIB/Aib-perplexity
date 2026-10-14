# AIB NEXUS — Registry (Part II)

**Document status:** Initial bootstrap specification  
**Implementation status:** Documentation only; no runtime registry implementation is claimed.  
**Last updated:** 2026-10-14

## 1. Purpose

The Registry is the authoritative inventory of AIB NEXUS components, responsibilities, interfaces, dependencies, lifecycle state, and verification evidence. It prevents planned capabilities from being mistaken for implemented ones.

## 2. Required record schema

Every component record MUST include:

| Field | Requirement | Meaning |
|---|---|---|
| `id` | Required, unique | Stable machine-readable identifier |
| `name` | Required | Human-readable name |
| `role` | Required | One-sentence responsibility |
| `owner` | Required | Accountable owner; never infer |
| `status` | Required | `PROPOSED`, `PLANNED`, `IMPLEMENTED_UNVERIFIED`, `VERIFIED`, `BLOCKED`, or `RETIRED` |
| `interfaces` | Required; empty list allowed | Inputs, outputs, protocol, and version |
| `dependencies` | Required; empty list allowed | Other registry IDs required |
| `security_boundary` | Required | Permitted data and permissions |
| `verification` | Required | Evidence reference or explicit `NOT_RUN` |
| `updated_at` | Required | ISO-8601 date/time or date |
| `notes` | Optional | Risks and unresolved decisions |

## 3. Initial inventory

These are planning records, not proof of implementation.

| ID | Component | Responsibility | Initial status | Verification |
|---|---|---|---|---|
| `aib-nexus-core` | AIB NEXUS Core | Central orchestration, planning, authorization coordination, and verification | `PLANNED` | `NOT_RUN` |
| `aib-registry` | Registry | Inventory components and track lifecycle/evidence | `IMPLEMENTED_UNVERIFIED` (documentation only) | This document only; runtime tests `NOT_RUN` |
| `aib-policy-gate` | Policy Gate | Enforce permission and approval boundaries | `PLANNED` | `NOT_RUN` |
| `aib-task-planner` | Task Planner | Turn user-approved goals into bounded, testable tasks | `PLANNED` | `NOT_RUN` |
| `aib-verification` | Verification Layer | Record expected result, test method, observed result, and evidence | `PLANNED` | `NOT_RUN` |
| `aib-android-contract` | Android Executor Contract | Define a versioned request/response boundary to the separate Android executor | `PROPOSED` | `NOT_RUN` |

## 4. Lifecycle rules

1. `PROPOSED`: idea recorded; not accepted scope.
2. `PLANNED`: scope accepted; implementation not established.
3. `IMPLEMENTED_UNVERIFIED`: an artifact exists; acceptance evidence is incomplete.
4. `VERIFIED`: reproducible evidence is tied to a commit or artifact version and has an explicit pass/fail result.
5. `BLOCKED`: a concrete blocker and smallest next action are recorded.
6. `RETIRED`: intentionally removed from active scope; history is retained.
7. Status never advances solely on a plan, code review, or agent assertion.

## 5. Security and ownership

- AIB NEXUS remains the central coordinator. External models or agents may advise or propose changes but do not silently become owners of the master source.
- Keep online orchestration and the offline Android executor as separate responsibilities, joined only through a versioned, explicit contract.
- Never put secrets, access tokens, personal data, or production credentials in the registry.
- Registration alone does not authorize execution. A separate policy and approval gate must govern actions.
- Unknown ownership, protocol details, and test outcomes must be marked unknown or `NOT_RUN`, not guessed.

## 6. Minimum acceptance tests for a future implementation

A runtime registry implementation is not accepted until automated tests demonstrate:

1. Duplicate IDs are rejected.
2. Unknown lifecycle statuses are rejected.
3. A component cannot be marked `VERIFIED` without evidence metadata.
4. Dependencies referencing unknown IDs are reported.
5. Validation is deterministic and returns a non-zero exit code on invalid input.

**Current result:** Specification draft only. No runtime validator, build, or test is claimed by this document.
