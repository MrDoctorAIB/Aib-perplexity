# AIB NEXUS

AIB NEXUS is the central online intelligence, orchestration, registry, authorization, planning, verification, and coordination layer of the AIB ecosystem.

## Architectural boundary

AI Model → AIB NEXUS → AIC Contract → AIC Offline Executor → Android

Android → AIC → AIB NEXUS → AI Model

### Non-negotiable boundaries

- AIC remains independent and offline-capable.
- AIB NEXUS is the online orchestrator/bridge.
- External agents are advisors/reviewers/proposal generators; they do not write directly to the Master Source.
- Codex works on dedicated branches and proposes changes through Pull Requests.
- Human approval is required before controlled merge.
- ZERO-GUESS / ZERO-ERROR is the operating target.
- IDEA → VERIFIED is the project completion rule.

## Current baseline

- Master Whitepaper: `AIB_NEXUS_MASTER_WHITEPAPER.md`
- Next architecture artifact: Part II — Registry
- Pilot is an explicit project phase/mode.

## Repository workflow

INSPECT → BASELINE → BRANCH → IMPLEMENT → TEST → SECURITY SCAN → DIFF REVIEW → PUSH → PR → HUMAN REVIEW → CONTROLLED MERGE

## Brand

MrEsfahan visual language:
- Base: matte/velvet black
- Primary accent: warm gold/yellow
- Secondary accent: blue
- Premium modern glassmorphism
- No dated/plain UI treatment

## Status

Bootstrap phase. No production implementation is claimed until build/test evidence exists.
