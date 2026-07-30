# Example 2: Workforce marketplace Experience Map

This fictional Build Mode example shows how to design a consequential marketplace journey before implementation.

## Request

```text
Use Build with LumynQ to create an Experience Map for a skilled-trades marketplace where a worker receives a job offer, reviews the terms, and accepts or declines. Preserve worker agency and make uncertainty visible.
```

## Scope and assumptions

- The worker can review an offer before creating a payment account.
- Pay, location, schedule, travel, overtime, duration, and cancellation terms are supplied by the contractor.
- Whether those terms have been independently verified is Unknown.
- “Good fit” is a provisional product hypothesis, not a statement about the worker’s identity or worth.

## Experience Map

### Human outcome

The worker can decide whether the opportunity fits their circumstances without pressure, hidden terms, or penalty for declining.

### Experience hypothesis

If the marketplace presents complete terms, explains uncertainty, and preserves a private decline path, workers can make decisions with greater clarity and control.

| Moment that matters | Likely state or need | Product behavior | Agency and recovery | Validation signal |
|---|---|---|---|---|
| Offer arrives | Attention, uncertainty | Name the job, contractor, location, and response window without artificial urgency | Snooze or dismiss notifications | Workers can find the offer later |
| Terms review | Comparison, consequence | Show pay basis, expected hours, overtime, travel, lodging, duration, start date, and verification status | Save, export, ask a question | Fewer term-related support contacts |
| Fit explanation | Skepticism, curiosity | Show source-linked reasons the opportunity was surfaced; label unverified assumptions | Correct profile facts or hide a signal | Corrections change later matching |
| Decision | Commitment | Present Accept and Decline with equal visual dignity | Decline privately without ranking penalty | Decline completes without coercive copy |
| After acceptance | Planning | Confirm next steps, responsible party, deadlines, and what remains conditional | Withdraw and contact a human | Worker can locate status and exit path |
| Change or cancellation | Disruption | State what changed, why, and which party initiated it | Reconsider, withdraw, or request support | Recovery path works without starting over |

## Key copy

**Fit explanation**

> This opportunity was surfaced because your profile lists the required license and your travel preference includes this region. The employer has not yet verified the proposed overtime schedule.

**Decline confirmation**

> Declined. This will not lower your standing. You can optionally tell us what did not fit, or leave without giving a reason.

## Failure and repair behavior

- If terms are missing, block acceptance and identify the party responsible for completing them.
- If the worker corrects a profile fact, preserve the prior value in an audit trail but stop using it for future matching.
- If an offer changes after acceptance, require renewed consent rather than treating silence as agreement.
- If a worker requests human help, preserve the current decision state and context so they do not have to repeat the journey.

## Acceptance criteria

- Accept and Decline are both keyboard accessible and neither uses shaming or loss-framed language.
- Missing consequential terms prevent acceptance.
- Every match explanation distinguishes verified facts from marketplace inference.
- Corrected worker information changes subsequent matching behavior.
- A changed offer requires explicit renewed acceptance.
