# LumynQ Integration and Domain Packs

Use this reference only with documented public LumynQ interfaces or as a clearly labeled provisional architecture. Never infer package behavior from the LumynQ philosophy alone.

## Establish the integration facts

Verify:

- package or API name and version;
- public exports, request and response types, and supported runtime;
- initialization, configuration, errors, and lifecycle;
- data classification, retention, network behavior, and observability;
- licensing and permitted distribution;
- Domain Pack schema, loading rules, and version compatibility.

If any fact is unavailable, mark it **unverified** and keep it out of executable code.

## Preserve four boundaries

1. **LumynQ Core:** protected, domain-neutral reasoning and orchestration surface.
2. **Domain Pack:** versioned domain vocabulary, outcomes, constraints, evidence rules, and response guidance.
3. **Application policy:** customer-specific permissions, thresholds, workflows, and escalation ownership.
4. **Experience layer:** interface states, controls, explanations, copy, and channel-specific rendering.

Do not bury customer policy in Core, UI copy in the Domain Pack, or proprietary Core logic in the public Skill.

## Use an application adapter

Place a typed boundary between product code and the documented Core interface. The adapter should:

- validate inputs and outputs;
- translate application events into supported LumynQ inputs;
- attach the correct Domain Pack version;
- handle uncertainty, timeouts, unavailable states, and safe fallbacks;
- preserve evidence or provenance required for consequential outputs;
- expose stable application-facing results without leaking internal reasoning.

Do not render hidden chain-of-thought. Provide concise reasons, source evidence, applicable constraints, and correction paths when explanation is warranted.

## Define a provisional Domain Pack

Include only fields supported by the actual schema. During design, consider:

| Area | Contents |
| --- | --- |
| Identity | Pack ID, domain, owner, version, compatibility, and status |
| Scope | Included and excluded actors, journeys, decisions, and jurisdictions |
| Language | Domain vocabulary, aliases, sensitive terms, and plain-language equivalents |
| Human outcomes | Capabilities or supported shifts the experience should enable |
| Moments | High-stakes, uncertain, vulnerable, or recovery-heavy situations |
| Evidence | Permitted sources, provenance rules, freshness, and confidence handling |
| Signals | Allowed inputs, prohibited proxies, and minimization rules |
| Inference limits | Claims the system must not make, especially diagnosis or identity assignment |
| Responses | Suitable strategies, tone constraints, explanations, and fallback behavior |
| Escalation | Triggers, human owner, handoff payload, and user-visible expectation |
| Evaluation | Fixtures, edge cases, counterexamples, and acceptance criteria |

Keep secrets, production credentials, raw customer PII, and unsupported proprietary materials out of a Domain Pack.

## Test at two levels

### Boundary tests

- schema and version compatibility;
- deterministic handling of required, optional, malformed, and unavailable inputs;
- timeout and safe fallback behavior;
- prohibited inference and privacy constraints;
- traceable response metadata where supported.

### Experience tests

- representative moments and edge states;
- incorrect emotional hypotheses and user correction;
- ambiguity, conflicting evidence, and low confidence;
- cultural, language, accessibility, and literacy variation;
- denial, exit, escalation, and recovery;
- whether the user retains understanding and agency.

## Report the result

Separate:

- **Verified implementation:** supported by current documentation or code.
- **Provisional design:** proposed contract awaiting confirmation.
- **Blocked detail:** cannot be implemented responsibly without a missing interface, policy, or decision.

Never turn a provisional Domain Pack into a claim that the protected engine has been trained or integrated.
