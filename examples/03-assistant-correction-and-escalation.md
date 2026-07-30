# Example 3: Assistant correction and human escalation

This fictional example shows how an assistant should respond when its inference is wrong and the stakes exceed its authority.

## Request

```text
Use Build with LumynQ to redesign an assistant that recommends financial hardship resources. It currently says “You seem overwhelmed” and automatically enrolls people in a callback queue.
```

## Human outcome

A person can explore support options without being diagnosed, categorized, or enrolled in contact they did not request.

## Experience hypothesis

If the assistant explains why it surfaced an option, treats interpretation as provisional, and asks before escalating, people can correct it and seek help without surrendering privacy or control.

## Consequential moments

### 1. The assistant notices a possible need

**Problem:** “You seem overwhelmed” converts limited behavioral evidence into an emotional claim.

**Behavior change:** State the observed context and offer a choice.

> You’ve revisited the payment-options page twice. Would it help to compare due-date, payment-plan, and human-support options?

Controls: **Compare options**, **Talk to someone**, **Not now**

### 2. The person corrects the inference

**Behavior change:** Accept the correction without defensiveness and stop using the signal.

> Thanks for correcting that. I won’t use those page visits as a sign that you want hardship support.

Controls: **Continue normally**, **Review what informed this**

### 3. Human support becomes appropriate

**Behavior change:** Explain what the handoff does before asking for consent.

> A support specialist can discuss account-specific choices that I cannot approve. If you choose a callback, we’ll share your account number and the options you viewed—not an emotional label.

Controls: **Request callback**, **See other contact methods**, **Keep exploring here**

### 4. Callback is unavailable

**Behavior change:** Preserve context and provide a next step.

> Callbacks are unavailable right now. Your place has not been added to a queue. You can try during tomorrow’s hours, call directly, or save these options.

## State model

```text
possible_need → option_offered → dismissed
                              → corrected → signal_retired
                              → self_service
                              → escalation_explained → consented → queued
                                                     → declined
                                                     → unavailable
```

## Data boundaries

- Store the person’s explicit support choice, not a durable label such as “overwhelmed.”
- Do not add them to a callback queue before explicit consent.
- Show the data shared during handoff.
- Let the person revoke a pending callback request.
- Retire a corrected inference from future recommendations.

## Acceptance criteria

- The assistant never states an emotional condition as fact.
- “Not now” ends the prompt without repeated pressure.
- A correction changes later behavior.
- No callback record exists before explicit consent.
- An unavailable escalation path states that no queue entry was created and offers alternatives.
