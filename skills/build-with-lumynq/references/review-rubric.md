# LumynQ Experience Review

Review the complete stateful experience, not just the happy path or its copy. Cite the artifact, behavior, or assumption behind each finding.

## Evidence classification

Assign the most specific available label to every material finding:

- **Observed—live:** witnessed by interacting with the running experience.
- **Observed—code:** directly supported by source, tests, or configuration, but not verified live.
- **Observed—plan:** directly stated in a plan, specification, or design artifact; evidence of intent only.
- **Inferred:** plausible from available evidence but not directly verified.
- **Unknown:** cannot be responsibly determined from available evidence.

Keep live behavior, code-supported behavior, and planned behavior separate. If they conflict, report the conflict.

## Live-review instrumentation preflight

Before beginning a live experiential review, declare which instruments are actually available:

- interactive pointer and text input;
- keyboard navigation and focus inspection;
- viewport resizing or a real target device;
- reduced-motion control;
- accessibility-tree or DOM inspection;
- an actual screen reader or other assistive technology, when relevant.

Distinguish an instrument that is unavailable from a scenario that fails. A static capture can support live evidence about the rendered state it shows, but not about interaction, focus, announcements, responsive behavior, motion preferences, or recovery paths it cannot exercise.

If an unavailable instrument affects only bounded scenarios, review everything else and list those scenarios as **Unknown**. If it prevents the consequential purpose of the live review from being tested, state that limitation before the findings and use **NOT ADJUDICATED** as the overall verdict. Do not replace missing live evidence with code, test, or plan evidence.

## Review dimensions

| Dimension | What to inspect |
| --- | --- |
| Orientation | Can the person tell where they are, what is happening, and what comes next? |
| Agency | Are real choices, consent, correction, undo, cancellation, and exit available? |
| Dignity | Does the experience avoid blame, shame, condescension, stereotyping, and identity-level judgments? |
| Emotional fit | Does behavior and tone match the stakes instead of performing generic warmth or celebration? |
| Trust | Are consequences, data use, delays, limitations, and uncertainty communicated honestly? |
| Legibility | Can the person understand and challenge a consequential system decision or inference? |
| Recovery | Do errors, denials, incomplete states, and wrong inferences provide a useful next step? |
| Inclusion | Does the path work across relevant language, culture, disability, device, connectivity, and literacy needs? |
| Privacy | Are signals and retained data necessary and proportionate to the human outcome? |
| Continuity | Does completion create closure, handoff, memory, or a trustworthy return path? |

## State coverage

Inspect whichever states exist:

- first arrival and onboarding;
- default, loading, empty, and partial states;
- choice, disclosure, consent, submission, and payment;
- warnings, errors, denials, timeouts, and offline behavior;
- success, confirmation, next step, and return;
- correction, undo, cancellation, deletion, and escalation.

## Common failure patterns

- friendly copy covering a coercive or irreversible action;
- celebration at a moment involving loss, rejection, debt, illness, or uncertainty;
- urgency that exists for conversion rather than the user's welfare;
- a vulnerable user asked to disclose before context or trust is established;
- an emotional inference stated as fact;
- a consequential recommendation with no evidence, uncertainty, or correction path;
- blame-oriented errors such as “you failed” or “invalid user”;
- reassurance without a truthful status, timeframe, owner, or next step;
- a dead end after denial, mismatch, or unsupported need;
- hidden cancellation, preselected consent, or asymmetric friction;
- anthropomorphic language that overstates understanding or care;
- a demo, simulation, or fixed result presented as live, personalized, learned, detected, or analyzed;
- planned behavior described as if it already exists in the running product;
- success measured only by completion, engagement, or retention.

## Demo and simulation truthfulness

Treat simulation as valid when its boundary is honest and visible.

- Label synthetic inputs, hard-coded outputs, mocks, prerecorded behavior, and unavailable integrations at the point of use.
- Verify that consequential capability verbs match actual execution. If entered data does not materially shape an output, do not call the result personalized or analyzed.
- Keep the boundary visible when results appear; do not disclose “demo” on entry and imply real capability later.
- State what is real now, what is simulated, and what remains planned or unknown.

## Reviewing plans and specifications

Evaluate a plan as a proposal, not as proof of implementation:

1. Separate what the current product does, what the plan proposes, and what remains unresolved.
2. Review whether the proposal covers the human consequence, system behavior, controls, language, recovery, and validation.
3. Call a planned change a **planned resolution**, not a fixed finding.
4. Require live or code verification before crediting the running product with the planned behavior.

## Severity calibration

| Severity | Use when | Example |
| --- | --- | --- |
| **Blocker** | The experience creates coercion, material deception, unsafe behavior, or severe loss of agency. | Fixed output is presented as personalized analysis; consequential consent can be bypassed. |
| **Major** | The experience is likely to cause a trust break, exclusion, abandonment, or consequential misunderstanding. | A submitted correction is discarded; a reset silently erases meaningful work. |
| **Moderate** | The experience creates recurring friction, emotional mismatch, or weak recovery without defeating the core outcome. | A waiting state lacks useful timing or ownership, but the person can still recover. |
| **Polish** | The core outcome and controls work; refinement would improve coherence or fit. | Hierarchy or transition language can be clearer without changing behavior. |

## Finding format

Use this compact structure:

| Moment | Evidence class | Evidence | Consequence | Severity | Required change | Acceptance test |
| --- | --- | --- | --- | --- | --- | --- |

Use **Blocker**, **Major**, **Moderate**, or **Polish** severity. Do not manufacture a numerical emotional-intelligence score unless the user asks for one and a defined scoring method exists.

## Recommendation standard

Each material recommendation should connect:

1. the state or behavior that creates the problem;
2. the human consequence;
3. the system, interaction, or language change;
4. the evidence that would show improvement.

Prefer a smaller number of consequential fixes over a long inventory of cosmetic observations.

## Overall verdict

Use one of four outcomes:

- **PASS:** the consequential live scenarios were exercised and no material experience failures remain.
- **PASS WITH POLISH:** the consequential live scenarios were exercised and only non-blocking refinements remain.
- **FAIL:** observed behavior contains a Blocker or Major failure, or a Moderate failure that defeats the review's core human outcome.
- **NOT ADJUDICATED:** missing access or instrumentation prevents the consequential live scenarios from being evaluated. This is an evidence limitation, not a product failure.

Name any bounded Unknowns even when the overall verdict is PASS or PASS WITH POLISH.
