# AI UX Audit Testbed

### Testing three approaches to AI-powered UX auditing

This repository explores how effectively AI can conduct a UX and heuristic audit of a deliberately flawed user interface.

The experiment uses the **same test interface** and evaluates it through three different AI-assisted approaches:

1. **Claude Skills** — a purpose-built UX audit skill with defined evaluation instructions and output structure.
2. **Custom GPT** — a custom-configured GPT designed to perform UX evaluation.
3. **Direct Prompting** — a general AI model such as ChatGPT or Claude, instructed through prompts to conduct the audit.

The goal is to understand how these approaches compare in their ability to **identify UX issues, correctly map them to usability principles, reason about their impact, assess severity, and produce an audit that is useful to a real product team.**

---

## The Experiment

The experiment starts with a deliberately flawed web interface containing known usability and heuristic issues.

Each AI method is given the same interface and asked to perform a UX audit.

```text
                 SAME TEST UI
                      │
          ┌───────────┼───────────┐
          ↓           ↓           ↓
   Claude Skills   Custom GPT   Direct Prompt
          │           │           │
          ↓           ↓           ↓
       AI Audit     AI Audit     AI Audit
          │           │           │
          └───────────┼───────────┘
                      ↓
             Comparative Analysis
                      ↓
          Structured UX Audit Report
                      ↓
       Stakeholder / Project Team
```

The experiment is therefore not simply testing whether AI can find problems.

It is testing **how different AI approaches perform the task and whether their outputs can be turned into a credible UX audit deliverable.**

---

## The Three AI Methods

### 01 — Claude Skills

A Claude Skill is used to provide AI with a defined UX audit capability, including structured instructions for evaluating an interface.

This approach explores whether a purpose-built AI skill can produce more consistent and defensible UX findings.

### 02 — Custom GPT

A Custom GPT is configured specifically for UX auditing.

This approach explores whether a persistent set of instructions, context, and evaluation criteria can improve the quality and consistency of an AI-generated audit.

### 03 — Direct Prompting

The interface is provided to a general-purpose AI model such as ChatGPT or Claude using prompts created specifically for the audit.

This represents a more accessible approach where a designer does not build a custom skill or configure a dedicated AI.

---

## The Test Interface

The repository contains a deliberately flawed dashboard interface.

The UI intentionally includes usability problems such as:

* Low-contrast text
* Ambiguous or unlabeled controls
* Misleading visual conventions for destructive actions
* Cryptic error messages
* Missing recovery guidance
* Long-running actions without meaningful progress feedback
* Destructive actions without confirmation
* Other intentionally planted UX and heuristic issues

The problems are deliberately introduced so that the AI outputs can be compared against a known baseline.

### Test the UI

Open `Bad_UI.html` in a browser to interact with the test interface.

---

## What is being evaluated?

The experiment evaluates the AI methods across multiple dimensions rather than simply counting how many issues they identify.

| Evaluation area       | Question                                                                  |
| --------------------- | ------------------------------------------------------------------------- |
| **Issue Detection**   | Did the AI identify the UX problem?                                       |
| **Heuristic Mapping** | Did it map the issue to the appropriate usability principle?              |
| **Evidence**          | Did it explain what in the interface supports the finding?                |
| **Reasoning**         | Did it explain why the issue matters to the user?                         |
| **Severity**          | Did it appropriately assess the impact or risk?                           |
| **Precision**         | Is the finding actually defensible, or merely an observation?             |
| **Coverage**          | How many known issues were identified?                                    |
| **False Positives**   | Did the AI report problems that aren't actually violations?               |
| **Actionability**     | Does the recommendation give the project team something useful to act on? |
| **Report Quality**    | Can the output be communicated to stakeholders in a professional format?  |

---

## From AI Finding to Stakeholder Report

A key part of this experiment is that the final output should not simply be a conversation with an AI.

The intended deliverable is a **structured UX audit report in PDF format** that can be handed over to:

* Product teams
* Design teams
* Engineering teams
* Project stakeholders
* Accessibility or UX reviewers

The report should transform AI observations into a format that is understandable and actionable outside the AI interface.

A typical finding may follow a structure such as:

```text
UX Issue
    ↓
What is happening?
    ↓
Why is it a problem?
    ↓
Heuristic / UX principle
    ↓
Evidence
    ↓
Severity / Risk
    ↓
Recommendation
```

The quality of the final report is therefore part of the experiment—not just the accuracy of the underlying AI analysis.

---

## A Critical Distinction: Observation vs. Violation

One of the questions this experiment specifically investigates is whether AI can distinguish between a **visual observation** and a **defensible heuristic violation**.

AI may correctly notice that something looks unusual or potentially problematic.

That does not automatically mean the issue has been correctly mapped to a heuristic.

For example:

> "A critical piece of information isn't visually distinguished according to its importance."

This may be a valid UX observation.

However, a defensible audit needs to establish:

* What makes the information critical?
* Which usability principle does the observation relate to?
* Is that principle actually being violated?
* What evidence from the interface supports the conclusion?
* Is another heuristic or UX principle a better classification?
* How significant is the issue for the user?

This distinction is particularly important when comparing AI-generated audits because a method that produces **more findings** is not necessarily producing a **better audit**.

---

## Comparing the Three Approaches

The experiment will compare the outputs from the three methods to identify differences in:

### Accuracy

Which approach identifies the known issues most reliably?

### Consistency

Does the same approach produce similar quality and structure across audits?

### Reasoning quality

Which approach provides the strongest explanation and evidence?

### False positives

Which approach is most likely to classify normal design decisions as UX violations?

### Actionability

Which approach produces recommendations that a project team could realistically act upon?

### Report readiness

Which approach requires the least manual refinement before producing a stakeholder-ready report?

---

## Expected Output

Each method will produce an AI-generated UX audit.

The outputs will then be reviewed and compared before being compiled into structured documentation.

The repository will contain artifacts such as:

```text
AI-UX-Audit-Testbed/
│
├── Bad_UI.html
│
├── prompts/
│   └── ...
│
├── claude-skills/
│   └── ...
│
├── custom-gpt/
│   └── ...
│
├── direct-prompting/
│   └── ...
│
├── audits/
│   ├── ...
│
├── evaluations/
│   └── ...
│
├── reports/
│   └── ...
│
└── README.md
```

The exact repository structure may evolve as the experiment develops.

---

## The Intended Outcome

The objective is not to prove that one AI method is universally better than another.

Instead, the experiment aims to understand:

> **What makes AI-powered UX auditing reliable enough to become part of a professional design workflow?**

The findings may reveal that different approaches are better suited to different stages of the audit—for example, one approach may excel at issue discovery while another produces better structured reporting.

The experiment will therefore evaluate both **AI reasoning quality** and **workflow practicality**.

---

## Why This Matters

As AI becomes increasingly capable of generating interfaces, design teams will also need effective ways to evaluate those interfaces.

A useful AI UX auditor needs to do more than identify visual anomalies.

It needs to reason about:

* User intent
* Usability principles
* Interaction behavior
* Accessibility
* Error recovery
* Context
* Severity and risk
* Evidence
* Recommended improvements

And importantly, its output needs to be understandable to people who were **not part of the AI conversation**.

That makes the transition from:

**AI analysis → structured UX findings → stakeholder-ready report**

an important part of the problem.

This repository is an experiment into that workflow.

---

## Status

🧪 **Experimental**

This repository documents an ongoing experiment. Prompts, AI configurations, audit findings, evaluation criteria, and reporting formats may evolve as the experiment progresses.

---

## Get Involved

If you're interested in AI × UX, heuristic evaluation, AI-assisted design workflows, or the future of UX auditing, explore the experiment and its artifacts.

Questions, critiques, alternative approaches, and collaborations are welcome.
