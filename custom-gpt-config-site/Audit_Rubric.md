# AI UX Audit Rubric

Use this rubric to evaluate the quality of a heuristic audit.

The rubric is intended to make findings evidence-based, comparable, and useful to a real product team.

## 1. Issue Detection

**Question:** Did the audit identify a genuine usability problem?

- Strong: identifies the underlying user problem clearly
- Weak: reports a vague visual concern without establishing user impact

## 2. Heuristic Mapping

**Question:** Is the issue mapped to the most appropriate Nielsen heuristic?

- Strong: the selected heuristic directly explains the problem
- Weak: the mapping is forced, generic, or materially less appropriate than another heuristic

Do not create duplicate findings simply because one issue could be associated with multiple heuristics.

## 3. Evidence

**Question:** Is there concrete evidence supporting the finding?

Evidence may include:
- Specific UI element
- Visible state
- Interaction behavior
- Error state
- Navigation behavior
- Responsive behavior
- Screenshot

A finding without observable evidence should not be presented as a confirmed violation.

## 4. User Impact

**Question:** Does the finding explain what happens to the user?

Strong findings explain consequences such as:
- Confusion
- Error likelihood
- Task failure
- Increased cognitive load
- Loss of work
- Accidental action
- Reduced discoverability
- Increased task time
- Abandonment risk

Avoid generic statements such as "this is bad UX."

## 5. Severity

Use four levels.

### Critical
Major data loss, irreversible harm, blocked critical tasks, or severe user failure.

### High
Substantial interference with important tasks, significant user errors, or likely abandonment.

### Medium
Meaningful confusion, friction, or inefficiency from which users can generally recover.

### Low
Minor usability issue with limited impact on task completion or comprehension.

Severity is based on user impact, not visual prominence.

## 6. Confidence

Assign one level:

### High
Directly observed and reproducible.

### Medium
Supported by evidence but partially constrained by the environment.

### Low
Plausible concern that could not be fully verified.

Low-confidence observations must not be presented as established facts.

## 7. Actionability

A recommendation should tell the project team what could reasonably be changed.

Weak:
"Improve the error message."

Strong:
"Replace the technical error code with a plain-language explanation of what failed and provide a clear next step for correcting the input."

Recommendations should address the underlying usability problem rather than merely its visual symptom.

## 8. Coverage

The audit should attempt to cover:
- Visual UI
- Navigation
- Controls
- Forms
- Error states
- Loading/processing states
- Dialogs and overlays
- Destructive actions
- Responsive behavior where possible
- Keyboard interaction where possible
- All ten Nielsen heuristics

The report must distinguish between:
- Tested
- Partially tested
- Not tested
- Not applicable

## 9. False Positives

A false positive occurs when the audit reports something as a heuristic violation without sufficient evidence.

Common causes:
- Treating personal design preference as a heuristic violation
- Assuming behavior that was not tested
- Mapping every accessibility issue to one heuristic
- Overinterpreting unusual visual styling
- Reporting the same problem multiple times
- Assuming a missing feature is automatically a usability failure

Favor precision over quantity.

## 10. False Negatives

A false negative occurs when a known, observable usability problem is missed.

When evaluating the audit against a human baseline, distinguish between:
- Completely missed issue
- Partially identified issue
- Correctly identified issue but incorrectly classified
- Correctly identified and classified issue

## 11. Finding Quality

A strong finding should answer:

1. What is wrong?
2. Where does it occur?
3. What did the user experience?
4. Why is it a usability problem?
5. Which heuristic does it violate?
6. How severe is it?
7. How confident are we?
8. What should the team consider changing?

## 12. Overall Assessment

When comparing audit approaches, do not rank them solely by number of findings.

Consider:
- Correct findings
- Missed known findings
- False positives
- Heuristic accuracy
- Evidence quality
- Severity accuracy
- Recommendation quality
- Coverage
- Report usability

A shorter, more accurate audit can be better than a longer audit containing many weak findings.
