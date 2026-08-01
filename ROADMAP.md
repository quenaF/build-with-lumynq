# Public roadmap

This roadmap communicates direction, not guaranteed scope or dates. Priorities may change as outside developers test the Skill and contribute evidence.

## Stable foundation — v0.1.0

- Publish a versioned release ZIP and reliable installation guidance.
- Provide complete examples across review, design, and assistant behavior.
- Improve issue intake for bugs, framework questions, integrations, and case studies.
- Preserve the boundary between the open Skill, customer Domain Packs, and LumynQ Core.
- Gather independent dogfood reports from multiple product domains.

## Phase 2.0 — Agent Bootstrap Contract — in progress

Goal: make a compatible coding agent aware of a product's verified human intent before it plans, reviews, or changes consequential behavior.

- Define the vendor-neutral bootstrap contract and minimum project bundle.
- Keep the public Skill separate from project-owned context.
- Preserve evidence class and owner-verification state as separate dimensions.
- Define authority order, human-approval pauses, unknown handling, and validation gates.
- Dogfood the contract in Project Lighthouse, the white-label youth experience platform.
- Revise the draft from observed agent behavior before declaring a stable bootstrap format.

Phase 2.0 does not add LumynQ Core, certify products, or automate owner confirmation.

## Phase 2.1 — `lumynq init` — proposed

- Discover project instructions, decisions, journeys, promises, unknowns, and validation commands.
- Generate an unverified `lumynq-project-bootstrap` bundle.
- Install or verify the public Build with LumynQ Skill.
- Present consequential mappings to a human owner for confirmation or correction.
- Refresh source pointers without overwriting canonical project documents.

## Phase 2.2 — Agent adapters — proposed

- Validate the bootstrap flow in Replit Agent, Codex, Claude Code, Cursor, and other compatible agents.
- Keep one semantic contract while adapting installation paths and platform capabilities.
- Add compatibility fixtures for discovery, authority conflicts, locked artifacts, unknowns, and safe fallback.
- Document degraded behavior where a client cannot support a required capability.

## Phase 2.3 — Launchpad handoff — proposed

- Export an owner-verified Agent Bootstrap Bundle after Launchpad discovery.
- Carry forward the Experience Map, human outcomes, promises, evidence provenance, corrections, unknowns, and boundaries.
- Keep customer context outside the public Skill and protected Core.
- Make handoff status and unresolved questions visible to both owner and agent.

## Phase 2.4 — Experience gates — proposed

- Check planned and implemented changes against the active bootstrap before release.
- Test consequential states including waiting, denial, correction, cancellation, escalation, and recovery.
- Require human approval where policy, safety, or product governance says the agent cannot decide.
- Report evidence and unresolved risk without claiming certification.

## Parallel learning — real implementations

- Document at least three outside or cross-domain case studies.
- Identify recurring primitives: human outcome, moment that matters, agency requirement, uncertainty, recovery, escalation, and evaluation evidence.
- Refine evidence and severity guidance from observed use.
- Define a vendor-neutral behavioral-evidence model that preserves provenance and separates behavior from emotional inference.
- Explore analytics adapters without embedding surveillance or vendor dependence in the Skill.

Track behavioral-evidence research in [Issue #1](https://github.com/quenaF/build-with-lumynq/issues/1).

## Later — portable tooling and interoperability

- Publish stable machine-readable schemas only after bootstrap dogfood demonstrates the required fields.
- Build a validator and parser before adding broad automation.
- Explore a TypeScript SDK and MCP server after the contracts stabilize.
- Begin HXS working notes by extracting common structures from independent implementations.

## Not yet

- Certification or claims that a product is “LumynQ approved.”
- Direct emotion classification from behavioral data.
- Automatic promotion of agent inference into owner-confirmed intent.
- A formal Human Experience Specification before independent implementations demonstrate an interoperability need.
- Claims that the open Skill or Agent Bootstrap contains proprietary LumynQ Core reasoning.

## How to influence the roadmap

- Report a reproducible problem with the bug form.
- Ask a framework question when a principle is unclear or produces conflicting outcomes.
- Propose a vendor-neutral integration.
- Share a redacted case study with evidence, consequences, and outcomes.

Accepted work should improve people's ability to act, understand, recover, decide, or retain meaningful choice.
