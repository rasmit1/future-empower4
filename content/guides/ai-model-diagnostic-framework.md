
---
title: "The AI Model Diagnostic Framework"
date: 2026-06-09
draft: false
categories: ["Futuristic Transformation", "Organization Science"]
description: "A three-layer sequential diagnostic process for AI model performance issues. Diagnose before you retrain."
tags: ["AI diagnostics", "model failure", "root cause analysis", "design thinking", "AI governance"]
---

> **Diagnose before you retrain.** The most expensive fix in AI is the one that solves the wrong problem.

Use this framework every time someone says "the model is wrong" — before agreeing to any fix.

---

## How to use this framework

Run the three layers in sequence. Do not skip ahead.

1. **Layer 1 — Horizontal scan:** Map the full problem landscape before going deep.
2. **Layer 2 — 5 Whys drill:** Find the true root cause for each distinct symptom.
3. **Layer 3 — Design Thinking check:** Confirm your fix will actually be adopted.

**Critical rule:** Complete all three layers before recommending any fix. The most expensive mistake in AI diagnostics is solving the wrong problem — and the wrong problem almost always looks like the right problem at Layer 1.

---

## Layer 1 — The Horizontal Scan

**Who · What · When · Where · Why · How — map the full landscape before you drill.**

Before diagnosing anything, build a complete picture of the situation. Without this scan you risk running the 5 Whys on the wrong symptom.

### WHO — Who is affected?

- [ ] Which users or teams are experiencing the problem?
- [ ] Is it everyone, or specific groups only?
- [ ] Who reported it first and when?
- [ ] Who owns the system — technically and operationally?
- [ ] Who are the downstream recipients of the wrong outputs?

### WHAT — What exactly is happening?

- [ ] What type of wrong answer — confidently wrong, outdated, vague, inconsistent, or discriminatory?
- [ ] What is the model being asked to do?
- [ ] What does a correct answer look like?
- [ ] What has already been tried to fix it?
- [ ] What is the business impact of the wrong answer?

### WHEN — When did it start?

- [ ] When did the wrong answers first appear?
- [ ] Was onset sudden or gradual?
- [ ] When does it happen — always, intermittently, at specific times?
- [ ] What changed in the business or environment around that time?
- [ ] When was the model last updated or retrained?

### WHERE — Where in the system?

- [ ] Where in the workflow does the wrong answer appear?
- [ ] Is it isolated to one business unit or system-wide?
- [ ] Where does the model get its information from?
- [ ] Where is the knowledge base stored and who manages it?
- [ ] Where does the output go after the model generates it?

### WHY — Why does it matter?

- [ ] Why is this output consequential — what decisions does it inform?
- [ ] Why are users relying on this output without verification?
- [ ] Why hasn't it been fixed already?
- [ ] Why does the team believe retraining is the solution?
- [ ] Why was the system designed this way originally?

### HOW — How is it manifesting?

- [ ] How often does it happen?
- [ ] How is the wrong answer different from the correct one?
- [ ] How is the model currently monitored?
- [ ] How were users trained to use the system?
- [ ] How confident does the model appear when it gives wrong answers?

### Layer 1 Output

After the horizontal scan you should be able to answer:

- How many distinct problem types are present?
- Who is affected by each?
- What pattern do the timing and location suggest?

**If you have more than one distinct symptom — run Layer 2 separately for each one. Do not combine them.**

---

## Layer 2 — The 5 Whys Vertical Drill

**Ask why five times. Each answer becomes the input to the next question.**

The 5 Whys is a root cause analysis technique from lean manufacturing, adapted here for AI model diagnostics. The principle: the first answer is almost never the real cause. Most organisations stop at Why 2 or Why 3 and fix the symptom. The true root cause is almost always at Why 4 or Why 5.

Run the 5 Whys separately for each distinct symptom identified in Layer 1.

---

### Example 1 — Stale knowledge symptom

| Why | Question | Answer |
|-----|----------|--------|
| Why 1 | Why did the rep give wrong information? | Because the model said the discount was valid. |
| Why 2 | Why did the model say it was valid? | Because the knowledge base contained the old policy. |
| Why 3 | Why was the old policy still there? | Because nobody had updated it when the policy changed. |
| Why 4 | Why had nobody updated it? | Because there was no defined process for keeping the knowledge base current. |
| Why 5 | Why was there no process? | Because knowledge base governance was never assigned to anyone. Nobody owned it. |

**True root cause:** Governance problem. No ownership. No update process.  
**Fix direction:** Assign ownership, define update cadence, implement RAG with live documents.

---

### Example 2 — Vague results in a different business unit

| Why | Question | Answer |
|-----|----------|--------|
| Why 1 | Why were the answers vague? | Because the model wasn't giving specific, actionable responses. |
| Why 2 | Why wasn't it specific? | Because it wasn't retrieving the right documents for this unit's queries. |
| Why 3 | Why not the right documents? | Because the reps were using different terminology than the original unit. |
| Why 4 | Why different terminology? | Because the model was optimised for one business unit's language only. |
| Why 5 | Why deployed without adjustment? | Because the deployment assumed the model was generic when it was domain-specific. |

**True root cause:** Deployment assumption problem. Not a model quality issue.  
**Fix direction:** Domain-specific prompt layer, terminology mapping, separate knowledge base per unit.

---

### Example 3 — Rate answers intermittently wrong

| Why | Question | Answer |
|-----|----------|--------|
| Why 1 | Why were rate answers sometimes wrong? | Because the model was returning outdated rates. |
| Why 2 | Why outdated? | Because rate data in the knowledge base wasn't being updated when rates changed. |
| Why 3 | Why wasn't it being updated? | Because rate data was treated as static content. |
| Why 4 | Why treated as static? | Because the architecture didn't distinguish stable from time-sensitive information. |
| Why 5 | Why was that distinction not made? | Because nobody assessed information volatility during the design phase. |

**True root cause:** Architecture and design problem. Retraining would not have fixed this.  
**Fix direction:** Connect to live data source, classify information by volatility, separate static from dynamic layers.

---

### Symptom → Root Cause Quick Reference

| Surface symptom | Likely root cause at Why 4–5 | Fix direction |
|-----------------|------------------------------|---------------|
| Confident wrong answers | No grounding — model using memory, not documents | RAG implementation |
| Outdated information | No knowledge base ownership or update process | Governance and process |
| Accuracy declining over time | Concept drift — real world changed, model didn't | Retraining + monitoring |
| Vague or unhelpful answers | Domain mismatch — wrong knowledge base for this user | Prompt and retrieval layer |
| Different outcomes for same inputs | Historical bias encoded in training data | Fairness audit + legal escalation |
| Works in testing, fails in production | Test data not representative of real users | Test set redesign |
| Inconsistent answers | Temperature too high or no grounding | Configuration + RAG |

**The 5 Whys rule:** If your Why 5 answer still sounds like a technical fix — you have not gone deep enough. The true root cause is almost always a governance gap, ownership gap, design assumption, or process failure — not a model failure.

---

## Layer 3 — The Design Thinking Check

**Desirability · Usability · Feasibility · Viability — ensure your fix will actually be adopted.**

This is the layer that purely technical diagnostics miss. A model can be technically correct and still fail — because users have stopped trusting it, the fix creates more friction than it removes, or the business case doesn't justify the cost.

Apply all four dimensions to your proposed fix before recommending it.

---

### Desirability — Will people actually want to use it?

- [ ] Do users trust the model enough to use the fix?
- [ ] Has previous failure damaged adoption? What is the trust-rebuilding plan?
- [ ] Does the fix align with how users actually work?
- [ ] Have users been involved in designing the solution?
- [ ] What does success look like from the user's perspective?

**Score (1–5):** `[ ]`

---

### Usability — Can they use it without friction?

- [ ] Does the fix add steps to the user's workflow?
- [ ] Is the output format usable in the context where it appears?
- [ ] Do users need training to use the fixed system?
- [ ] Is there a fallback when the model is uncertain?
- [ ] Can users provide feedback when something is wrong?

**Score (1–5):** `[ ]`

---

### Feasibility — Can it technically work?

- [ ] Is the data available and clean enough for the fix to work?
- [ ] Does the team have the skills to implement and maintain it independently?
- [ ] Can it be implemented in a timeframe that matters?
- [ ] Does it integrate with existing systems without a replatform event?
- [ ] Can it be tested before full deployment?

**Score (1–5):** `[ ]`

---

### Viability — Does it make business sense?

- [ ] What is the cost of the fix vs the cost of the problem? (Model it — don't feel it.)
- [ ] Does it create ongoing maintenance burden?
- [ ] What is the ROI timeline?
- [ ] Does it comply with regulatory requirements? (Name the specific regulation.)
- [ ] Is it sustainable as the AI programme scales?

**Score (1–5):** `[ ]`

> **Adoption warning:** If users have already lost trust in the tool — the technical fix alone will not restore adoption. You need a trust-rebuilding plan alongside the technical fix.

---

## The Diagnostic Sequence — Quick Reference

| Step | Action | Stop condition |
|------|--------|----------------|
| 1 | **Resist the instinct to fix.** Gather facts before prescribing solutions. | You have a written problem statement. |
| 2 | **Run the horizontal scan.** Map the full landscape. Count distinct symptoms. | You can answer: how many symptoms, who is affected, what the pattern suggests. |
| 3 | **Run 5 Whys separately for each symptom.** Do not combine them. | Each chain reaches a human decision — a governance, ownership, or design failure. |
| 4 | **Keep asking until you reach a human decision.** The root cause is almost never the model. | Your Why 5 names a person, process, or decision — not a technical component. |
| 5 | **Apply the Design Thinking check to your proposed fix.** All four dimensions must pass. | Desirability, Usability, Feasibility, and Viability are each scored ≥ 3. |
| 6 | **Recommend both an immediate fix and a structural fix.** The immediate fix stops the bleeding. The structural fix prevents recurrence. | Both fixes are documented with owners and timelines. |
| 7 | **Flag the regulatory implication.** In financial services, every model performance issue has a potential regulatory dimension — FCA, CFPB, DORA, SR 11-7. Name it explicitly. | The relevant regulation or standard is cited by name in your recommendation. |

---

*Framework by Future Empowered. 
