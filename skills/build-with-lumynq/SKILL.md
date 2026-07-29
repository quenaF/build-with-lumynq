---
name: build-with-lumynq
description: Design, review, and prepare integrations for emotionally intelligent digital products using the LumynQ approach. Use when a developer, product team, designer, or agent asks to make an onboarding flow, marketplace, assistant, form, notification, error state, decision experience, or other customer journey more emotionally intelligent; define the human outcome or emotional shift an experience should support; audit a product for confusing, coercive, dismissive, shame-inducing, exclusionary, or tone-deaf behavior; create a LumynQ Experience Map; define a provisional Domain Pack; or integrate against documented LumynQ Core interfaces. Do not use for generic visual polish or copyediting when human state, trust, agency, or experience behavior is not materially involved.
---

# Build with LumynQ

Help teams build products that understand human context, preserve dignity and agency, and support meaningful change. Treat emotional intelligence as system behavior—not a personality layer or a warmer choice of words.

Use this governing idea:

> The user is the person becoming. The product should illuminate the path, not make itself the hero.

## Protect the LumynQ boundary

- Treat this Skill as the developer-facing build method, not LumynQ Core itself.
- Do not claim access to proprietary LumynQ reasoning, weights, prompts, customer Domain Packs, or unpublished interfaces.
- Do not claim a product is powered by LumynQ unless a real LumynQ integration exists.
- Use only documented public Core interfaces. Never invent package exports, schemas, endpoints, or runtime behavior.
- When integration documentation is missing, produce a clearly labeled provisional contract or implementation plan and identify what must be verified.
- Label demos, simulations, synthetic data, hard-coded results, mocks, and planned capabilities at the point where a person encounters or evaluates them.
- Describe only behavior the running system actually performs. Do not call an output personalized, inferred, learned, detected, or analyzed unless implemented behavior uses the relevant input to produce it.
- Keep proprietary engine logic separate from public experience guidance and customer-specific domain knowledge.

## Apply the non-negotiables

- Infer emotional state only as a hypothesis. Distinguish observed evidence, reasonable inference, and unknowns.
- Never diagnose a user or present a transient signal as identity.
- Preserve informed choice, meaningful consent, reversibility, and an honest exit.
- Reject dark patterns, emotional pressure, manufactured urgency, shame, dependency engineering, and exploitative personalization.
- Earn trust through behavior. Do not use reassuring copy to conceal uncertainty, risk, delay, data use, or consequences.
- Design failure, denial, waiting, correction, cancellation, and recovery states with the same care as the happy path.
- Minimize sensitive data and recommend human escalation where the stakes exceed the system's competence.

## Select the operating mode

### Build Mode

Use for new experiences, redesigns, product flows, critiques, and emotionally consequential copy.

1. Identify the practical task and the human outcome.
2. State who the user is becoming or becoming able to do; avoid prescribing how they must feel.
3. Identify emotional, cognitive, social, and practical stakes.
4. Map the moments that matter, especially uncertainty, commitment, waiting, failure, and repair.
5. Design across four layers:
   - system behavior;
   - interaction and control;
   - language and tone;
   - feedback, measurement, and recovery.
6. Make assumptions visible and propose ways to validate consequential ones.

Read [experience-map.md](references/experience-map.md) when creating or materially redesigning a journey. Read [review-rubric.md](references/review-rubric.md) when evaluating an existing experience.

### Integration Mode

Use for LumynQ Core boundaries, adapters, Domain Packs, schemas, tests, and runtime integration plans.

1. Establish the actual package or API name, version, public documentation, and supported runtime.
2. Separate universal engine behavior, domain-specific context, application policy, and presentation.
3. Define permitted signals, prohibited inferences, human outcomes, response strategies, escalation paths, and evaluation fixtures.
4. Put a typed adapter between the application and documented Core surface.
5. Test consequential behavior deterministically at the boundary and experientially at the journey level.
6. Label all placeholders and unresolved interface decisions.

Read [integration-and-domain-packs.md](references/integration-and-domain-packs.md) before drafting a Domain Pack or implementation architecture.

## Work from evidence

Use supplied screens, code, product requirements, research, analytics, support patterns, or user statements. If the user supplies a URL or names a current product, inspect it when tools and authorization allow.

Use the most specific evidence label available:

- **Observed—live:** witnessed in the running experience through direct interaction.
- **Observed—code:** directly supported by source, tests, or configuration; do not assume it is reachable or working live.
- **Observed—plan:** stated in a plan, specification, or design artifact; treat it as evidence of intent, not current capability.
- **Inferred:** a plausible interpretation that needs validation.
- **Unknown:** missing information that could materially change the design.

Do not use code or planned behavior to imply that a capability exists in the running product. State conflicts between evidence sources instead of silently reconciling them.

Before issuing a live-review verdict, inventory the available interaction instruments and read the live-review preflight in [review-rubric.md](references/review-rubric.md). Test only what those instruments can genuinely exercise. If missing instrumentation prevents the consequential live scenarios from being evaluated, return **NOT ADJUDICATED** rather than converting code evidence into live proof or treating an untested product as failed.

Ask a question only when the answer would materially alter the outcome. Otherwise, proceed with an explicit assumption.

## Implement the experience

When the user asks for a product or code change, inspect the relevant components, state transitions, data flow, and existing tests, then implement the change within scope. Do not stop at a critique or copy recommendation.

- Represent meaningful states explicitly, including unavailable, incomplete, waiting, denied, incorrect-inference, correction, and recovery paths.
- Align system behavior, controls, accessibility, and language; do not solve a behavioral problem with copy alone.
- Preserve the application's established architecture and design system unless either causes the experience failure.
- Add or update tests for consequential transitions, correction, safe fallback, and any non-negotiable gate.
- Keep emotional hypotheses out of durable profiles, analytics, or logs unless collection is necessary, disclosed, consented to, and appropriately governed.

## Produce implementation-grade guidance

Lead with the experience change and the human result it supports. Then provide only the structure the task needs.

For a read-only review, stop at evidence-backed findings, required changes, and acceptance tests. Do not edit files, create replacement artifacts, or implement recommendations unless the user separately asks for changes.

When reviewing a plan or specification, separate current behavior, proposed behavior, and unresolved behavior. Evaluate whether the plan addresses a finding, but do not describe the current product as fixed until implementation is verified.

For a substantial Build Mode request, include:

- human outcome;
- experience hypothesis;
- moments that matter;
- concrete behavior, interaction, and copy changes;
- failure and repair behavior;
- assumptions and validation signals.

For a review, prioritize findings by consequence:

- **Blocker:** coercion, material deception, unsafe behavior, or severe loss of agency;
- **Major:** likely trust break, exclusion, abandonment, or consequential misunderstanding;
- **Moderate:** recurring friction, emotional mismatch, or weak recovery;
- **Polish:** refinement that improves coherence without changing the core outcome.

For an Integration Mode request, include:

- verified and unverified dependencies;
- boundary and data-flow decisions;
- Domain Pack contents or changes;
- privacy and inference constraints;
- tests and acceptance criteria;
- explicit open questions.

Scale the response down for a small request. Do not force a full framework onto a single error message or microinteraction.

## Quality check

Before finalizing, verify that:

- the proposed experience helps the user act, understand, recover, or decide;
- the emotional goal is not forced positivity or compliance;
- behavior and controls support the words;
- consequential inferences remain provisional and explainable;
- edge states preserve dignity and a next step;
- the product remains truthful about uncertainty and capability;
- the recommendation is specific enough to implement and test.
