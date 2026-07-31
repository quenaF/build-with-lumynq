# Build with LumynQ

**An open developer Skill for building software around human state, dignity, trust, and agency.**

Most software is designed around what a system needs people to do.

Build with LumynQ helps developers and AI coding agents also ask what people may be experiencing—and what the product must do to preserve truth, dignity, trust, accessibility, recovery, and meaningful choice.

This is not a tone guide or an empathy checklist. It is a product-building discipline for examining how system behavior affects human experience.

## What it does

Build with LumynQ helps a developer, product team, designer, or AI agent:

- design emotionally consequential journeys before implementation;
- review running products, source code, plans, and specifications without confusing one evidence type for another;
- identify coercion, confusion, shame, exclusion, trust breaks, and loss of agency;
- define a LumynQ Experience Map;
- design failure, waiting, correction, cancellation, and recovery states;
- prepare provisional Domain Packs and integrations against documented LumynQ Core interfaces;
- turn findings into implementation-grade behavior, tests, and acceptance criteria.

The Skill works across four layers: system behavior, interaction and control, language and tone, and feedback and recovery.

## Why it is different

Build with LumynQ treats emotional intelligence as product behavior—not warmer copy added after the decisions are made.

It requires reviewers to separate:

- **Observed—live**
- **Observed—code**
- **Observed—plan**
- **Inferred**
- **Unknown**

If a live review lacks the instruments needed to exercise consequential behavior, the Skill returns **NOT ADJUDICATED** instead of pretending automated evidence is live proof.

## Install

Download the versioned package from the [latest GitHub Release](https://github.com/quenaF/build-with-lumynq/releases/latest). The release asset is the recommended installation source because it is stable, versioned, and measurable.

For Replit Agent, install the community Skill directly from GitHub:

```bash
npx skills add quenaF/build-with-lumynq -a replit -s build-with-lumynq -y
```

See [INSTALLATION.md](INSTALLATION.md) for tested folder layouts and installation steps for:

- ChatGPT and Codex;
- Replit Agent;
- Claude Code;
- other Agent Skills-compatible environments.

## Try it

```text
Use Build with LumynQ to review this onboarding flow for moments that may create confusion, pressure, shame, exclusion, or loss of agency.
```

```text
Use Build with LumynQ to create an Experience Map before implementing this marketplace.
```

```text
Use Build with LumynQ to conduct a read-only live review. Separate live observations, code evidence, planned behavior, inferences, and unknowns.
```

## Repository structure

```text
.
├── .codex-plugin/
│   └── plugin.json
├── .github/
│   └── ISSUE_TEMPLATE/
├── examples/
│   ├── 01-application-waiting-state-review.md
│   ├── 02-workforce-marketplace-experience-map.md
│   └── 03-assistant-correction-and-escalation.md
├── skills/
│   └── build-with-lumynq/
│       ├── agents/
│       │   └── openai.yaml
│       ├── references/
│       └── SKILL.md
├── CONTRIBUTING.md
├── INSTALLATION.md
├── LICENSE
├── ROADMAP.md
└── README.md
```

The installable Skill stays inside `skills/build-with-lumynq/`. Public documentation and examples remain outside it so agents load only what they need.

## Proven in practice

The first dogfood target was LumynQ Launchpad itself. The Skill’s evidence discipline prevented a static preview from being misrepresented as an interactive review. A later live walkthrough found a real keyboard-focus defect that the green automated test suite had missed. The product was fixed, targeted tests were added, and the live review passed.

That loop—observe honestly, protect the human consequence, implement, test, and verify—is the point.

## Version

Current public release: **v0.1.0**. See the [release notes and downloadable ZIP](https://github.com/quenaF/build-with-lumynq/releases/tag/v0.1.0).

## License and brand

The Skill is available under the [MIT License](LICENSE).

“LumynQ” and associated branding identify the originating project. The MIT License permits use of the Skill’s contents but does not grant permission to imply endorsement by, partnership with, or certification from LumynQ.

## Contributing

Contributions are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or pull request.

See the [public roadmap](ROADMAP.md) for current priorities. Use the issue forms to report a bug, ask a framework question, propose an integration, or share a case study.
