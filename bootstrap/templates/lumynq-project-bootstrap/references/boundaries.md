# Project boundaries

**Bundle status:** template-uninitialized

Replace every bracketed placeholder during initialization. Missing boundaries are Unknown, not permission.

## Human authority

Human approval is required before:

- [consequential product, policy, safety, or release action]
- [change to a locked or ratified artifact]
- [collection, retention, or sharing of sensitive data]
- [external publication, deployment, or communication]

Escalation owner: [person or accountable role]  
Safe fallback while waiting: [read-only analysis, reversible prototype, or stop]

## Prohibited behavior and inference

The product and agent must not:

- diagnose a person or present a transient signal as identity;
- use pressure, shame, hidden loss, false reassurance, or manufactured urgency;
- claim personalization, detection, verification, safety, or integration that is not implemented;
- [project-specific prohibited behavior];
- [project-specific prohibited inference].

## Privacy and data minimization

- Permitted data: [minimum necessary data or fixture classes]
- Prohibited data: [secrets, raw PII, protected or high-risk data]
- Synthetic or mock requirement: [where realistic synthetic data is required]
- Retention or logging constraint: [rule or Unknown]

## Governance

- Locked artifacts: [paths or None]
- Append-only artifacts: [paths or None]
- Change process: [RFC, decision record, owner confirmation, or other rule]
- Bundle authority: This bootstrap points to governance; it does not replace or amend it.

## Validation gates

Run before completion is claimed:

1. [technical validation command]
2. [architecture, boundary, or tenant-separation gate]
3. [experience, accessibility, safety, or recovery review]
4. [human approval or release gate, when applicable]

If a gate cannot be run, report the result as not verified and explain the blocker.
