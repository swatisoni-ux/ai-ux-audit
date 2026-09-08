---
name: AI UX Heuristic Audit
description: Conduct a rigorous UX and Nielsen heuristic audit of a website URL by inspecting visuals, interacting with UI patterns, testing safe workflows, and producing a stakeholder-ready PDF report with evidence, severity, and recommendations.
---

# AI UX Heuristic Audit

## Purpose

Use this skill when asked to audit, evaluate, review, or assess the UX/usability of a website or web application provided through a URL.

The objective is to produce a **defensible UX heuristic evaluation**, not a superficial visual critique.

You must inspect the interface **and interact with it** before producing the final report. Treat the website as a product that a real user would operate.

The final deliverable must be a **professionally structured PDF report** suitable for handoff to a product, design, engineering, or project team.

---

# Core Principles

1. **Inspect before judging.**
   Do not report an issue merely because an element looks unusual.

2. **Interact before concluding.**
   Important controls, navigation, forms, menus, dialogs, states, and workflows must be tested where safely possible.

3. **Separate observation from violation.**
   An observation becomes a confirmed finding only when there is sufficient evidence that it violates a usability principle or creates a meaningful user problem.

4. **Use evidence.**
   Every finding must identify the specific UI element, state, or interaction that supports the conclusion.

5. **Do not invent behavior.**
   If an interaction cannot be tested, say so. Never claim that an interaction fails without evidence.

6. **Prioritize user impact.**
   Severity should reflect the effect on users and task completion, not how visually noticeable the issue is.

7. **Avoid false positives.**
   Do not force every unusual design choice into a heuristic violation.

8. **Do not alter real-world data destructively.**
   Never perform irreversible actions such as deleting an account, submitting a real purchase, sending a real message, changing production data, or publishing content unless the user explicitly provides a safe test environment and authorizes the action.

9. **Use safe test data.**
   When forms can be tested, use clearly fictional values unless the user provides test values.

10. **Be transparent about coverage.**
    Report what was tested, what could not be tested, and any constraints.

---

# Input

The primary input is a website URL.

If no URL is provided, ask for one.

If the website requires credentials, payment, CAPTCHA completion, or other information that is unavailable, do not fabricate access. Record the limitation and continue with whatever can be safely evaluated.

If multiple URLs are provided, treat each as a separate audit target unless the user explicitly asks for a comparative audit.

---

# Audit Workflow

Follow this sequence. Do not skip directly from page inspection to report generation.

## Phase 1 — Establish the audit scope

Before evaluating the site:

1. Open the supplied URL.
2. Confirm the page loads successfully.
3. Identify the apparent product/page purpose.
4. Identify the primary user goal or task.
5. Note whether the page is:
   - marketing/content
   - dashboard/application
   - form/workflow
   - ecommerce
   - account/settings
   - documentation
   - other
6. Record the audit date.
7. Record the URL.
8. Note any access, environment, or technical limitations.

Do not infer product context beyond what the site makes reasonably clear.

---

# Phase 2 — Visual and Structural Inspection

Inspect the interface before interacting with it.

Review:

### Layout and hierarchy
- Page structure
- Information hierarchy
- Grouping and proximity
- Alignment
- Density
- Whitespace
- Content prioritization
- Section hierarchy

### Navigation
- Primary navigation
- Secondary navigation
- Breadcrumbs
- Tabs
- Sidebars
- Back/close controls
- Current-location indicators

### Controls
Inspect:
- Buttons
- Links
- Icon-only controls
- Toggles
- Checkboxes
- Radio buttons
- Select menus
- Inputs
- Search
- Filters
- Pagination
- Tooltips

### Visual communication
Look for:
- Meaning conveyed only through color
- Ambiguous icons
- Weak affordances
- Inconsistent component patterns
- Misleading visual hierarchy
- Poor state differentiation
- Text that is difficult to read
- Inconsistent terminology

### Accessibility signals
Perform a practical visual accessibility review including:
- Text contrast
- Control contrast
- Focus visibility where observable
- Text sizing
- Touch target size where relevant
- Labels for controls
- Error identification
- Color-only communication

Do not claim formal WCAG compliance or non-compliance unless the evidence supports the specific criterion.

---

# Phase 3 — Interaction and State Testing

This phase is mandatory.

Interact with the website rather than relying only on screenshots or static inspection.

Test, where applicable:

## Navigation

- Primary navigation
- Secondary navigation
- Back navigation
- Breadcrumbs
- Tabs
- Internal links
- External links
- Menu open/close behavior
- Mobile navigation if available

Check whether users can understand:
- where they are
- where they came from
- where they can go
- what is currently selected

## Buttons and controls

For representative controls, test:
- Click/tap behavior
- Hover states where applicable
- Focus states where applicable
- Disabled states
- Loading states
- Success states
- Failure states
- Whether the control behaves as its label suggests

Pay particular attention to destructive, irreversible, or high-impact actions.

## Forms

Test representative forms.

Check:
- Label clarity
- Required-field communication
- Input affordances
- Placeholder usage
- Validation timing
- Error messages
- Error placement
- Error recovery
- Preservation of entered data
- Success confirmation
- Keyboard behavior
- Submit behavior
- Duplicate submission risk

Use safe fictional values.

Where possible, intentionally test common invalid states such as:
- empty required field
- malformed input
- invalid format
- boundary value
- duplicate value

Do not attempt malicious payloads or security testing unless explicitly requested.

## Menus, dialogs, and overlays

Test:
- Opening
- Closing
- Escape behavior
- Outside-click behavior where relevant
- Focus behavior where observable
- Clear action hierarchy
- Confirmation patterns
- Whether the user can recover from accidental actions

## Dynamic and asynchronous behavior

Look for:
- Loading indicators
- Progress indicators
- Skeleton states
- Delayed responses
- Disabled controls during processing
- Success feedback
- Error feedback
- Timeout behavior

If an action takes time, observe whether the user is told what is happening.

## Error and recovery paths

Do not test only the happy path.

Intentionally create safe failure states and evaluate:
- What went wrong
- Whether the system explains the problem
- Whether the message uses understandable language
- Whether the user knows what to do next
- Whether the system preserves work
- Whether recovery is obvious

---

# Phase 4 — Responsive and Input-Mode Review

If the environment allows it, inspect the site at multiple viewport sizes.

At minimum consider:
- Desktop
- Narrow/mobile viewport

Look for:
- Broken layouts
- Horizontal overflow
- Hidden controls
- Unusable navigation
- Text truncation
- Overlapping content
- Inadequate touch targets
- Changes in interaction patterns
- Missing mobile equivalents

If actual mobile/touch interaction cannot be tested, state that limitation.

Where keyboard interaction is available, test representative flows using keyboard navigation.

Check:
- Tab order
- Focus visibility
- Ability to reach interactive controls
- Ability to operate controls
- Ability to dismiss dialogs
- Logical progression through forms

---

# Phase 5 — Nielsen Heuristic Evaluation

Evaluate the interface against all ten Nielsen usability heuristics.

Do not assume every heuristic must produce a finding.

## Heuristic #1 — Visibility of System Status

Evaluate whether the system keeps users informed about:
- loading
- processing
- progress
- success
- failure
- current state
- saved/unsaved status

## Heuristic #2 — Match Between System and the Real World

Evaluate:
- language
- terminology
- familiar concepts
- meaningful labels
- understandable error messages
- natural ordering and representation

## Heuristic #3 — User Control and Freedom

Evaluate:
- undo
- cancel
- back
- exit
- dismissal
- confirmation for risky actions
- ability to recover from mistakes

## Heuristic #4 — Consistency and Standards

Evaluate:
- terminology
- component behavior
- visual conventions
- interaction conventions
- platform/web standards
- destructive/success conventions

## Heuristic #5 — Error Prevention

Evaluate whether the design prevents errors before they occur through:
- constraints
- defaults
- validation
- confirmation
- safe actions
- prevention of accidental submission

Do not confuse error prevention with error recovery. Evaluate both separately.

## Heuristic #6 — Recognition Rather Than Recall

Evaluate whether users can recognize:
- available actions
- navigation location
- meanings of controls
- previously entered information
- system options

Flag interfaces that require users to remember information unnecessarily.

## Heuristic #7 — Flexibility and Efficiency of Use

Evaluate:
- shortcuts
- efficient workflows
- sensible defaults
- personalization where appropriate
- power-user support
- repetitive task burden

Do not flag the absence of shortcuts as a violation unless the context makes efficiency materially important.

## Heuristic #8 — Aesthetic and Minimalist Design

Evaluate:
- unnecessary information
- visual clutter
- competing hierarchy
- excessive complexity
- irrelevant content
- density that interferes with task completion

Do not equate minimal visual style with good usability.

## Heuristic #9 — Help Users Recognize, Diagnose, and Recover from Errors

Evaluate:
- clarity of error messages
- explanation of what happened
- identification of the affected field/action
- recovery instructions
- preservation of user work

## Heuristic #10 — Help and Documentation

Evaluate whether help is:
- available when needed
- discoverable
- concise
- task-oriented
- understandable
- relevant to the user's context

Do not classify every accessibility issue as Heuristic #10. Map findings to the heuristic that most directly explains the usability problem.

---

# Finding Validation

Before adding a finding to the final report, validate it using this checklist:

### Evidence
Can you point to a specific element, state, or interaction?

### User impact
Can you explain what a user is likely to experience?

### Heuristic fit
Does the selected heuristic actually explain the problem?

### Severity
Is the severity proportional to the consequence?

### Reproducibility
Can the issue be reproduced or observed reliably?

### Recommendation
Can the problem be improved through a concrete design or interaction change?

If any of these are uncertain, lower the confidence or exclude the finding.

---

# Severity Model

Use a four-level severity scale.

### Critical
The issue can cause major data loss, irreversible harm, blocked critical tasks, or severe user failure.

### High
The issue substantially interferes with important tasks or is likely to cause significant user errors or abandonment.

### Medium
The issue causes meaningful friction, confusion, or inefficiency but users can generally recover.

### Low
The issue is minor and has limited impact on task completion or comprehension.

Severity is not a visual-design score.

A visually ugly issue may be Low, while a subtle interaction problem may be Critical.

---

# Confidence

Assign a confidence level to every finding:

- **High** — directly observed and reproducible.
- **Medium** — supported by evidence but partially constrained by the environment.
- **Low** — plausible concern that could not be fully verified.

Do not present Low-confidence observations as confirmed violations.

---

# Avoid Duplicate Findings

One underlying problem may affect multiple heuristics.

Do not create multiple findings simply because the same issue can be described using several heuristics.

Choose the **primary heuristic** that best explains the problem.

If another heuristic is materially relevant, mention it as a secondary relationship rather than creating a duplicate finding.

---

# Finding Format

Every confirmed finding must contain:

1. Finding title
2. Heuristic number and name
3. Severity
4. Confidence
5. Evidence
6. User impact
7. Recommendation
8. Tested state or interaction, when applicable

Use concise language.

Avoid vague findings such as:

> "The UX could be improved."

Prefer:

> "The form displays a generic error code after submission, giving users no indication of what failed or how to recover."

---

# Evidence and Screenshots

Capture screenshots when the environment supports it.

Prioritize screenshots for:
- important findings
- error states
- dialogs
- interaction states
- confusing controls
- responsive issues
- high/critical severity issues

Each screenshot should support a specific finding.

Do not fill the report with screenshots that add no evidence.

When a screenshot is used, include a short caption explaining what the reviewer should notice.

---

# Report Generation

The final deliverable MUST be a PDF.

Do not submit only a chat response or Markdown file as the final audit.

Use the available PDF/document-generation capability in the environment.

If a PDF-generation skill or tool is available, use it rather than manually simulating a PDF in plain text.

If code execution is available and required, generate the PDF programmatically using a reliable document/PDF workflow.

---

# Required PDF Structure

Create a professional report with the following structure.

## 1. Cover

Include:
- Report title
- Website name or URL
- Audit date
- "AI UX Heuristic Evaluation"
- Optional audit version

Keep the cover minimal.

## 2. Executive Summary

Summarize:
- overall assessment
- number of findings
- severity distribution
- major usability risks
- most important recommended actions

Do not introduce findings that are not documented later.

## 3. Audit Scope and Method

Document:
- URL audited
- date
- pages/flows reviewed
- interaction types tested
- viewport/input modes tested
- heuristic framework used
- limitations

Explicitly state that the audit included both **visual inspection and interaction testing**.

## 4. Finding Summary

Provide a scannable table:

| ID | Heuristic | Finding | Severity | Confidence |
|----|-----------|---------|----------|------------|

Keep the summary concise.

## 5. Detailed Findings

For each finding provide:

### [Finding ID] — [Short title]

**Heuristic:**  
Nielsen Heuristic #[X] — [Name]

**Severity:**  
[Critical / High / Medium / Low]

**Confidence:**  
[High / Medium / Low]

**Evidence:**  
What was observed or what interaction produced the issue.

**User impact:**  
Why the issue matters and what users may experience.

**Recommendation:**  
A specific, actionable improvement.

**Evidence image:**  
Include a relevant screenshot when available.

## 6. Interaction Coverage

Summarize what was actually tested.

Example:

| Area | Tested | Notes |
|------|--------|-------|
| Navigation | Yes | Primary and secondary navigation reviewed |
| Forms | Yes | Empty and invalid states tested |
| Error recovery | Yes | Representative failure states tested |
| Destructive actions | Safe inspection only | Irreversible action not executed |
| Responsive | Yes | Desktop and narrow viewport |
| Keyboard | Partial | Environment limitations noted |

Never claim an interaction was tested if it was not.

## 7. Heuristic Coverage

Show all ten heuristics.

For each, indicate:

- Finding(s), or
- No confirmed violation observed

This is important because the absence of a finding is itself part of the audit coverage.

## 8. Prioritization

Provide a prioritized action list.

Example:

| Priority | Finding | Recommended action |
|----------|---------|--------------------|
| 1 | H3-01 | Add confirmation and recovery for destructive action |
| 2 | H1-01 | Add visible processing feedback |
| 3 | H9-01 | Rewrite error message and provide recovery guidance |

Prioritize by user impact and risk, not by how easy the fix is.

## 9. Methodology and Limitations

Document:
- environment constraints
- inaccessible flows
- unavailable authentication
- unsupported interaction modes
- assumptions
- areas requiring human validation

Be explicit about uncertainty.

## 10. Appendix

Include, when useful:
- screenshots
- tested URLs/routes
- interaction notes
- heuristic reference
- audit metadata

---

# Report Quality Standards

The PDF should feel like a professional UX deliverable, not an AI transcript.

### Do:
- Use clear hierarchy.
- Use consistent spacing.
- Keep findings concise.
- Use tables for summaries.
- Use screenshots selectively.
- Make severity visually scannable.
- Use page numbers.
- Include report title and audit date.
- Keep terminology consistent.
- Proofread the final document.
- Verify that the PDF opens correctly.

### Do not:
- Include internal chain-of-thought.
- Include hidden reasoning or private model deliberation.
- Include irrelevant commentary.
- Overuse AI-generated filler.
- Repeat the same finding.
- Claim tests that were not performed.
- Present assumptions as facts.
- Produce a visually dense wall of text.

---

# Final QA Before Submission

Before delivering the PDF, perform a final audit of the audit.

Check:

### Completeness
- Was the entire accessible page reviewed?
- Were important navigation paths tested?
- Were representative interactions tested?
- Were safe error states tested?
- Were responsive/keyboard checks attempted where possible?

### Accuracy
- Does every finding have evidence?
- Is the heuristic mapping defensible?
- Is severity justified?
- Are duplicate findings removed?
- Are uncertain findings clearly marked?

### Report quality
- Does the PDF open?
- Are all pages readable?
- Are tables and screenshots correctly rendered?
- Are headings consistent?
- Are page breaks sensible?
- Is there a clear executive summary?
- Is there a prioritized action list?

### Honesty
- Does the report clearly distinguish tested behavior from inferred behavior?
- Are limitations documented?
- Are destructive actions that were not executed explicitly identified?

Only after these checks should the PDF be considered final.

---

# Final Response

When the audit is complete:

1. Provide the generated PDF.
2. Briefly state the number of confirmed findings.
3. State the number of heuristics with confirmed violations.
4. Mention any major audit limitations.
5. Do not replace the PDF with a long conversational summary.

The PDF is the primary deliverable.
