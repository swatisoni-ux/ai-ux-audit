# AI UX Audit Report Structure

The final audit must be delivered as a professional PDF.

The PDF is the primary deliverable. It should be suitable for handoff to product, design, engineering, and project stakeholders.

The report must not read like an AI conversation.

---

# 1. Cover

Include:
- Report title
- Website/product name
- URL
- Audit date
- "AI UX Heuristic Evaluation"
- Optional version

Keep the cover minimal.

---

# 2. Executive Summary

Summarize:
- Overall assessment
- Number of confirmed findings
- Severity distribution
- Major usability risks
- Highest-priority recommendations

Do not introduce findings that do not appear in the detailed findings section.

---

# 3. Audit Scope & Methodology

Document:
- URL audited
- Audit date
- Pages/flows reviewed
- Interaction types tested
- Viewports tested
- Input methods tested
- Nielsen heuristic framework
- Audit limitations

Explicitly state that the audit included both visual inspection and interaction testing.

---

# 4. Finding Summary

Provide a concise table:

| ID | Heuristic | Finding | Severity | Confidence |
|----|-----------|---------|----------|------------|

Keep finding titles short enough to scan.

---

# 5. Detailed Findings

For every confirmed finding use:

## [Finding ID] — [Short title]

**Heuristic**  
Nielsen Heuristic #[X] — [Name]

**Severity**  
Critical / High / Medium / Low

**Confidence**  
High / Medium / Low

**Evidence**  
Describe exactly what was observed or what interaction produced the issue.

**User Impact**  
Explain why the issue matters and what the user may experience.

**Recommendation**  
Provide a specific and actionable improvement.

**Evidence Image**  
Include a relevant screenshot when available.

---

# 6. Interaction Coverage

Summarize what was actually tested.

Use a table such as:

| Area | Status | Notes |
|------|--------|-------|
| Navigation | Tested | Primary and secondary navigation reviewed |
| Forms | Tested | Representative validation states tested |
| Error recovery | Tested | Safe failure states tested |
| Destructive actions | Partial | Irreversible action not executed |
| Responsive | Tested | Desktop and narrow viewport |
| Keyboard | Partial | Environment limitations documented |

Only report interactions that were actually tested.

---

# 7. Heuristic Coverage

Show all ten Nielsen heuristics.

For each heuristic, indicate:
- Confirmed finding(s), or
- No confirmed violation observed

This section is mandatory.

Example:

| Heuristic | Result |
|-----------|--------|
| H1 — Visibility of System Status | 1 finding |
| H2 — Match Between System and Real World | No confirmed violation |
| H3 — User Control and Freedom | 1 finding |

Do not omit heuristics with no findings.

---

# 8. Prioritization

Create a prioritized action list.

Use:

| Priority | Finding | Recommended Action |
|----------|---------|--------------------|
| 1 | H3-01 | Add confirmation and recovery for destructive action |
| 2 | H1-01 | Add visible processing feedback |
| 3 | H9-01 | Rewrite error message and provide recovery guidance |

Prioritize according to user impact and risk.

Do not prioritize solely by implementation effort.

---

# 9. Limitations

Document:
- Inaccessible pages
- Authentication limitations
- Unsupported interactions
- Environment constraints
- Actions intentionally not executed
- Assumptions
- Areas requiring human validation

Clearly distinguish observed evidence from inference.

---

# 10. Appendix

Include when useful:
- Screenshots
- Tested URLs/routes
- Interaction notes
- Heuristic reference
- Audit metadata

Do not add screenshots merely for decoration.

---

# PDF Quality Standards

The PDF should have:

- Clear typography
- Strong information hierarchy
- Consistent spacing
- Scannable tables
- Concise findings
- Consistent severity indicators
- Page numbers
- Report title/date
- Logical page breaks
- Readable screenshots

Avoid:
- Walls of text
- Excessive screenshots
- Repetition
- AI filler
- Internal reasoning
- Chain-of-thought
- Unsupported claims

---

# Final PDF QA

Before delivering:

## Completeness
- Confirm the accessible interface was reviewed.
- Confirm representative interactions were tested.
- Confirm relevant error states were tested.
- Confirm loading states were checked.
- Confirm responsive checks were attempted where possible.
- Confirm keyboard checks were attempted where possible.

## Accuracy
- Every finding has evidence.
- Heuristic mapping is defensible.
- Severity is justified.
- Confidence is justified.
- Duplicate findings are removed.
- Uncertain findings are clearly marked.

## Rendering
- PDF opens successfully.
- All pages are readable.
- Tables render correctly.
- Screenshots render correctly.
- Headings are consistent.
- Page breaks are sensible.
- No content is clipped or unintentionally overlapped.

## Honesty
- Tested behavior is distinguished from inference.
- Limitations are documented.
- Destructive actions not executed are explicitly identified.

Only after these checks should the PDF be considered final.
