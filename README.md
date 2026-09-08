# AI UX Audit Testbed

### Can AI detect what’s wrong with a deliberately flawed interface?

This repository is a testbed for experimenting with **AI-powered UX auditing**.

It contains a deliberately flawed web interface designed to violate common UX and usability principles. The UI acts as a controlled input for testing whether AI can identify usability problems, map them to appropriate heuristic principles, explain the evidence, and distinguish genuine heuristic violations from observations that merely *look* like UX issues.

The goal is not to create a good interface.

The goal is to **test the quality of AI-generated UX audits**.

---

## What is this?

Traditional UX audits rely heavily on human interpretation and experience. An experienced designer can look at an interface, recognize a problem, understand its context, and determine which usability principle it violates.

But what happens when AI is asked to perform the same task?

This experiment explores that question using a deliberately problematic interface as the test subject.

The repository can be used to evaluate:

* How well AI detects visible UX problems
* Whether AI correctly identifies heuristic violations
* Whether AI chooses the appropriate heuristic principle
* How well AI explains *why* something is a problem
* Whether AI can distinguish observation from defensible heuristic violation
* Whether AI identifies severity and risk consistently
* Where AI misses obvious problems
* Where AI incorrectly flags something as a violation
* How prompting affects the quality of the audit

---

## The Test Interface

The repository includes a deliberately flawed dashboard interface.

The interface intentionally contains problems such as:

* Low-contrast text
* Ambiguous or unlabeled controls
* Destructive actions using misleading visual conventions
* Cryptic error messages
* Missing recovery guidance
* Long-running actions without meaningful progress feedback
* Destructive actions without confirmation
* Other usability issues designed to challenge automated UX evaluation

The purposefully flawed nature of the UI makes it possible to compare AI's findings against a known set of planted issues.

### Open the test UI

Open `Bad_UI.html` in a browser to interact with the test interface.

---

## Experiment Structure

The repository is intended to evolve as the experiment progresses.

```text
AI-UX-Audit-Testbed/
│
├── Bad_UI.html
│
├── prompts/
│   ├── ...
│
├── audits/
│   ├── ...
│
├── evaluations/
│   ├── ...
│
└── README.md
```

The exact structure may change as additional experiments are added.

### Test UI

The deliberately flawed interface used as the input for the audit.

### Prompts

Prompts used to ask AI to inspect, evaluate, classify, or explain issues in the interface.

### Audits

Raw or refined AI-generated UX audit results.

### Evaluations

Comparison of AI findings against the known issues in the test interface.

---

## What is being evaluated?

The experiment looks beyond simple issue detection.

An AI model saying:

> "This button could be improved."

is not necessarily demonstrating useful UX auditing.

A stronger audit should be able to establish:

**What is happening → Why it is a problem → Which principle it violates → What evidence supports the finding → How serious the problem is**

For example:

| Dimension      | Question                                            |
| -------------- | --------------------------------------------------- |
| Detection      | Did AI notice the issue?                            |
| Classification | Did AI identify the correct UX/heuristic principle? |
| Evidence       | Did it explain what in the UI supports the finding? |
| Reasoning      | Did it explain why the issue affects the user?      |
| Severity       | Did it appropriately assess the risk?               |
| Precision      | Is the finding actually defensible?                 |
| Coverage       | How many planted issues did it identify?            |

---

## An Important Distinction

One of the things this experiment is specifically interested in is the difference between a **visual observation** and a **defensible heuristic violation**.

AI can be very good at noticing that something *looks wrong*.

That does not automatically mean it has correctly identified a heuristic violation.

For example, an AI might observe that:

> "A critical piece of information isn't visually distinguished according to its importance."

That can be a legitimate UX observation.

However, the next step requires reasoning:

* What exactly makes the information critical?
* Which usability principle does this relate to?
* Is the principle actually being violated?
* What evidence from the interface supports the claim?
* Is another heuristic a better mapping?

The experiment therefore treats **observation and heuristic classification as separate evaluation steps**.

---

## Why use a deliberately bad UI?

A real product interface contains too many uncontrolled variables.

A deliberately flawed interface provides a more controlled experiment.

Known problems can be planted intentionally and then used as a baseline against which AI-generated findings can be compared.

This makes it possible to ask:

> **Did the AI actually detect the problem we expected it to detect?**

rather than simply asking:

> **Does this AI-generated audit sound reasonable?**

---

## Potential Experiments

The same interface can be evaluated using different approaches.

### 01 — Baseline Audit

Give AI the interface with minimal instructions.

Measure what it identifies without providing a detailed evaluation framework.

### 02 — Structured Prompt

Provide explicit instructions for:

* What to inspect
* What heuristics to use
* How to structure findings
* How to assign severity

Compare the output against the baseline.

### 03 — Evidence-Based Audit

Require AI to provide evidence for every finding before classifying it as a confirmed violation.

This tests whether structured reasoning improves precision.

### 04 — Multi-Pass Audit

Separate the process into stages:

```text
Observe
   ↓
Identify potential issues
   ↓
Map to heuristic
   ↓
Validate evidence
   ↓
Assess severity
   ↓
Produce final audit
```

Compare this against a single-prompt audit.

### 05 — Model Comparison

Run the same audit using different AI models and compare:

* Detection
* Accuracy
* False positives
* False negatives
* Severity consistency
* Quality of reasoning

---

## What this repository is NOT

This is not intended to be:

* A production design system
* A real product
* A recommendation that the interface should look this way
* A definitive benchmark for AI UX capabilities
* A replacement for human UX evaluation

The interface is intentionally artificial and intentionally flawed.

The value is in **testing the audit process**, not in the interface itself.

---

## Why this matters

AI can increasingly generate interfaces.

That creates a corresponding question:

**Can AI reliably evaluate the interfaces it helps create?**

If AI is going to participate throughout the product design lifecycle, UX evaluation cannot simply depend on whether a model can recognize obvious visual problems.

It needs to reason about:

* User intent
* Context
* Usability principles
* Accessibility
* Interaction behavior
* Error recovery
* Risk and severity
* Evidence

This repository is a small experiment toward understanding where AI performs well, where it struggles, and what a more reliable **AI-assisted UX audit workflow** might look like.

---

## Status

🧪 **Experimental**

This repository is actively used for experimentation. Findings, prompts, evaluation methods, and supporting artifacts may change as the experiment evolves.

---

## Get involved

If you're interested in AI × UX, heuristic evaluation, AI-assisted design workflows, or simply want to experiment with the test interface, feel free to explore the repository.

Questions, critiques, experiments, and collaborations are welcome.
