# Example 1: Application waiting-state review

This fictional example shows a bounded, read-only review. It demonstrates evidence discipline, a consequential finding, and an adjudicated recommendation.

## Request

```text
Use Build with LumynQ to conduct a read-only review of the application submission flow. Focus on trust, agency, waiting, correction, and recovery. Do not edit the product.
```

## Instrumentation preflight

- Interactive browser: available
- Keyboard input: available
- Viewport control: unavailable
- Accessibility-tree inspection: available
- Screen reader: unavailable
- Source code: unavailable

Mobile layout and actual screen-reader output remain **Unknown**.

## Human outcome

After applying, a person should know that the application arrived, what happens next, when to expect an update, and how to correct or withdraw it.

## Finding

**Moment:** Submission confirmation and transition into waiting.

**Evidence class:** Observed—live

**Evidence:** After successful submission, the interface displays “We’ll be in touch.” It provides no receipt identifier, review stage, expected update window, status location, correction path, or withdrawal control.

**Human consequence:** The product creates avoidable uncertainty about whether the application succeeded and removes meaningful control during a consequential waiting period.

**Severity:** Major

**Required change:** Confirm receipt, name the current stage and expected update window, provide a persistent status location, and expose correction and withdrawal paths.

**Acceptance test:** After submission, a keyboard-only user can identify whether it succeeded, when the next update is expected, where status lives, and how to correct or withdraw without contacting support.

## Recommendation

**FAIL.** The missing status and recovery behavior creates a material trust and agency break. Mobile and screen-reader-specific behavior remain Unknown and are not counted as failures.
