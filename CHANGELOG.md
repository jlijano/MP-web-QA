# Master Prompt Changelog

This file records controlled updates to `MASTER_PROMPT.md`.

## 1.4.0 — Evidence logging and release checklist

Status: Added

Purpose:
- make QA evidence collection auditable and repeatable
- make Master Prompt changes explicitly logged, not only committed
- add a formal pre-change, post-change, deployment, regression, accessibility, media, conversion, SEO, performance, privacy, security, and release checklist
- prevent source updates from being mistaken for live verification
- make user corrections, mitigations, preservation requirements, and residual risks part of the release record

Added / strengthened:
- Master Prompt Update Logging Standard
- QA Evidence Log Standard
- Implementation / Release Checklist
- Release Gate and residual-risk rules
- requirement to record version, reason, affected sections, evidence, mitigations, commit SHA, deployment status, and remaining unverified items
- checklist coverage for targeted changes, adjacent behavior preservation, responsive states, keyboard/touch/reduced-motion, native media controls, CTA completion, dead-code cleanup, SEO, performance, privacy/security, and deployment truth

Reason:
The prior QA and implementation session showed that strong audit rules alone are not enough. Reliable website work also requires a repeatable record of what changed, why it changed, what evidence supports it, what must remain unchanged, what was verified, what remains blocked, and whether the production deployment was actually observed.

## 1.3.0 — Implementation safety and regression prevention

Status: Added

Purpose:
- extend the Master Prompt from review-only QA into implementation-aware QA
- prevent narrow user requests from causing unrelated regressions
- preserve adjacent working behavior
- improve media/carousel, conversion, accessibility, maintainability, and source-control practices

Key additions:
- Implementation Mode
- Targeted Change / No-Overshoot Rule
- Regression Guardrail
- Deployment Truth Rule
- User Correction Protocol
- Source Control Safety
- Front-End Maintainability Rule
- Third-Party Asset Reliability
- Media and Carousel Best Practices
- Touch / Hover Parity
- Static-Site Data / Polling Rule
- CTA Functional Integrity
- Placeholder and Fake-Success Rule
- Proof / Trust Claim Rule
- Reusable Implementation Patterns
- Mitigations / Things Not To Do

## 1.2.0

Baseline version before the implementation-safety expansion.
