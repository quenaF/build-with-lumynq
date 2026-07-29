# Sample read-only review

This short example demonstrates the evidence discipline and finding format. It is illustrative, not evidence about a real product.

## Review boundary

- Interactive browser: available
- Keyboard input: available
- Viewport control: unavailable
- Reduced-motion control: unavailable
- Accessibility-tree inspection: available
- Screen reader: unavailable

Mobile, real reduced-motion behavior, and actual screen-reader output remain **Unknown**.

## Finding

**Moment:** A person submits an application and reaches a waiting state.

**Evidence class:** Observed—live

**Evidence:** The interface shows “We’ll be in touch” with no timeframe, status location, correction path, or way to withdraw.

**Human consequence:** The person cannot tell whether the submission succeeded, what happens next, or how to recover from a mistake. The uncertainty is created by the product, not the person.

**Severity:** Major

**Required change:** Confirm receipt, name the review stage and expected window, provide a status location, and offer correction and withdrawal paths.

**Acceptance test:** After submission, the person can identify whether it succeeded, when the next update is expected, where status lives, and how to correct or withdraw without contacting support.

## Recommendation

**PASS WITH POLISH** is not appropriate because the missing recovery and status behavior creates a material trust break. The reviewed journey receives **FAIL** until the Major finding is resolved and verified live.

