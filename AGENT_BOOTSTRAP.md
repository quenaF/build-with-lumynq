# LumynQ Agent Bootstrap Contract

**Status:** Provisional Phase 2.0 draft  
**Contract version:** 0.1-draft  
**Compatibility target:** Agent Skills-compatible coding agents

## Purpose

Agent Bootstrap makes a coding agent aware of a product's verified human intent before it plans, reviews, or changes consequential behavior.

It connects two things without merging them:

- **Build with LumynQ** supplies the public product-building method.
- **The project bootstrap bundle** supplies project-specific, owner-verifiable context and governance.

The bundle should help an agent preserve what the product is trying to make possible for people, recognize what remains unknown, and avoid silently rewriting founder intent or human-authority boundaries.

## Non-goals

Agent Bootstrap does not:

- contain or expose LumynQ Core;
- prove that LumynQ Core is integrated;
- certify a product as emotionally intelligent or “LumynQ approved”;
- infer a person's emotional state as fact;
- replace product-owner, domain-expert, legal, safety, or operational authority;
- turn unreviewed project documents into verified truth;
- grant an agent permission to change files, publish, deploy, or contact people.

## The two-layer model

A conforming project keeps the reusable method separate from project-owned context:

```text
.agents/skills/
├── build-with-lumynq/          # Versioned public Skill; installed unchanged
└── lumynq-project-bootstrap/   # Project-owned, generated or maintained locally
    ├── SKILL.md
    └── references/
        ├── source-map.md
        └── boundaries.md
```

Agent-specific adapters may use another documented Skills directory, but the contents and behavior of the two layers should remain equivalent.

Do not place customer secrets, credentials, raw personal data, proprietary Core logic, or a private Domain Pack in either Skill.

## Minimum bootstrap bundle

A bundle conforms to this draft only when it contains all three files below.

### 1. `SKILL.md`

Defines when the project bootstrap activates and the agent workflow it requires. It must:

- trigger before materially consequential product planning, review, or implementation;
- require the agent to load only the canonical sources relevant to the task;
- preserve evidence class and owner-verification state;
- require a preflight against project promises, boundaries, unknowns, and approval rules;
- require relevant validation before reporting completion;
- state that the bundle is project context, not LumynQ Core.

### 2. `references/source-map.md`

Points to canonical project sources instead of copying them. At minimum it maps:

- founder or owner intent;
- human outcomes and promises;
- Experience Maps, journeys, or moments that matter;
- actors, perspectives, or affected groups;
- ratified decisions and governance;
- open questions and unknowns;
- evaluation gates and validation commands.

Each entry records its source path, evidence class, owner-verification state, and last verification date when known.

### 3. `references/boundaries.md`

States the constraints the agent must not infer from scattered documentation. At minimum it records:

- actions requiring human approval;
- prohibited product behavior or inferences;
- privacy and data-minimization rules;
- locked or append-only artifacts;
- safe fallback and escalation behavior;
- project-specific release or validation gates.

## Evidence and verification are separate dimensions

A bootstrap must not collapse “where this came from” into “who has approved it.”

Use one evidence class:

- **Observed—live:** witnessed in the running experience.
- **Observed—code:** supported by source, tests, or configuration.
- **Observed—plan:** stated in a plan, specification, decision, or design artifact.
- **Inferred:** plausible interpretation requiring validation.
- **Unknown:** missing information that may change the result.

Also use one owner-verification state when applicable:

- **Unreviewed**
- **Owner-confirmed**
- **Owner-corrected**
- **Deprioritized**
- **Not applicable**

For example, a promise may be `Observed—plan + Owner-confirmed`; a suspected user need may be `Inferred + Unreviewed`. An agent must preserve both.

## Authority order

Within the permissions granted for the task, a conforming agent uses this order:

1. platform safety, tool, and authorization policy;
2. the user's explicit current instruction;
3. ratified project governance and human-approval boundaries;
4. owner-confirmed or owner-corrected intent and decisions;
5. task-relevant observed evidence;
6. unreviewed plans and inferences;
7. unknowns.

The agent must surface a material conflict instead of silently choosing a lower-authority source. The agent cannot promote its own inference, generated copy, or implementation into owner-confirmed intent.

## Required agent behavior

Before a consequential change, the agent must:

1. identify the practical task, human outcome, affected actors, and operating mode;
2. read the bootstrap source map and boundaries;
3. load only the relevant canonical project sources;
4. separate current behavior, planned behavior, inference, and unknowns;
5. state any material assumption it can safely carry;
6. pause for human direction when a conflict, approval boundary, or unknown would materially change the result;
7. test the proposed change against promises, recovery paths, reversibility, privacy, and truthful capability;
8. implement only within the user's authorized scope;
9. run the project’s applicable technical and experience gates;
10. report what changed, what evidence supports it, and what remains unresolved.

For a read-only request, the agent stops at evidence-backed findings and acceptance tests.

## Lifecycle

- **Initialize:** Discover canonical project sources and generate an unverified bundle.
- **Verify:** A product owner confirms, corrects, deprioritizes, or marks unknown the consequential entries.
- **Activate:** Install the public Skill and project bootstrap in the agent's supported project Skills directory.
- **Use:** Load the bundle before relevant planning, review, or implementation.
- **Refresh:** Update source pointers and verification dates when canonical decisions change.
- **Revoke:** Remove the project bootstrap without deleting or rewriting canonical project evidence.

A future `lumynq init` command may automate Initialize and Activate. It must not automate owner confirmation.

## Conformance checks

A bundle passes this Phase 2.0 draft when:

- the agent can discover both Skills in a new session;
- project context is referenced, not duplicated;
- an unfilled placeholder or missing canonical source is treated as Unknown;
- the agent does not claim Core integration or certification;
- owner-confirmed intent outranks agent inference;
- a locked or approval-gated change causes an explicit pause;
- project validation gates are run before completion is claimed;
- removing the bootstrap leaves the application and canonical project documents intact.

## Dogfood plan

Project Lighthouse, the white-label youth experience platform, is the first dogfood target.

The test should install the public Skill unchanged, generate a separate `lumynq-project-bootstrap` bundle, point it to the existing Project Lighthouse Codex and Experience Explorer, and verify that an agent respects tenant separation, no-real-child-data rules, human approval boundaries, open questions, and the locked Codex without duplicating those sources.

Results from this dogfood test should revise this contract before Phase 2.1 begins.
