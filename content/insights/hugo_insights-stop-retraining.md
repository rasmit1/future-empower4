---
title: "Stop Retraining. Start Diagnosing."
description: "In enterprise AI, the model is rarely the problem — the system around it almost always is. A real case study in diagnosing three root causes hiding behind what looked like one model failure."
date: 2026-06-07
draft: false
categories: ["Futuristic Transformation", "Organization Science"]
tags: ["AI Diagnostics", "AI Governance", "Model Performance", "5 Whys", "AI Transformation", "Enterprise AI", "Financial Services"]
author: "Rashmi Mittal"
---

> "In enterprise AI the model is rarely the problem. The system around it almost always is."

A customer rep promised a discount. It was the right discount. The model said so. The problem — the policy had changed three days earlier. The model didn't know.

The customer was already engaged. The promise was already made. The rep couldn't honor it. The customer was furious.

When I was brought in, the team's instinct was to retrain the model. Expensive. Time-consuming. And in this case — completely wrong diagnosis.

Retraining fixes a model that learned the wrong thing. It does not fix a model that never knew the right thing to begin with. That is a different problem. With a different fix.

But here is what made this situation more complex. The same model was giving different reps different problems. Not one consistent failure — three separate ones. Each looked like a model problem on the surface. None of them actually were.

What I built instead of recommending a retrain was a diagnostic process. One that asked the right questions before prescribing any solution. I used a combination of three frameworks — the 5 Whys, the Who What When Where Why How questioning structure, and Design Thinking. Together they revealed three completely different root causes hiding behind what looked like one problem.

## The Three Frameworks — How They Work Together

**Who What When Where Why How** is the horizontal scan. It maps the full landscape of a problem before you go deep — who is affected, what exactly is happening, when it started, where in the system it occurs, why it matters, and how it is manifesting. Without this scan you risk drilling deep on the wrong problem.

**5 Whys** is the vertical drill. It takes the surface symptom identified in the scan and asks why five times in sequence — each answer becoming the input to the next question — until you reach the true underlying cause. Most organizations stop at Why 1 or Why 2 and fix the symptom. The real cause is almost always at Why 4 or Why 5.

**Design Thinking** adds the human lens. Once you have identified the root cause, Design Thinking asks whether the proposed fix is desirable (will people actually use it?), usable (can they use it without friction?), feasible (can it technically work?), and viable (does it make business sense?).

## The Case — Three Symptoms, Three Diagnoses

The model had been built as an operational efficiency tool but was also serving customer-facing representatives directly. That dual-purpose deployment — something organizations consistently underestimate — was part of the problem.

### Symptom 01 — Reps Making Promises Based on Outdated Policies

**The story:** A rep quoted a customer a discount that the model confirmed was valid. The policy had changed three days earlier. The team's instinct — retrain the model on updated policies.

**The 5 Whys diagnostic:**
- Why 1: Why did the rep give wrong information? → Because the model said the discount was valid.
- Why 2: Why did the model say it was valid? → Because the model's knowledge base contained the old policy.
- Why 3: Why was the old policy still in the knowledge base? → Because nobody had updated it when the policy changed.
- Why 4: Why had nobody updated it? → Because there was no defined process for keeping the knowledge base current.
- Why 5: Why was there no process? → Because knowledge base governance was never assigned to anyone. Nobody owned it.

**True root cause:** Not a model problem. A governance problem. Nobody owned the knowledge base. No process existed for updating it when business rules changed.

**Fix:** Assign knowledge base ownership. Define update cadence. Implement RAG with live policy documents. Alert system when source documents change.

### Symptom 02 — Vague Results in a Different Business Unit

**The story:** Reps in a second business unit were getting answers that were technically present but unhelpfully vague. Not wrong — just not useful. The team's instinct — the model needs more training data.

**The 5 Whys diagnostic:**
- Why 1: Why were the answers vague? → Because the model wasn't giving specific, actionable responses.
- Why 2: Why wasn't it giving specific responses? → Because it wasn't retrieving the right documents for this unit's queries.
- Why 3: Why wasn't it retrieving the right documents? → Because the reps were using different terminology than the original unit.
- Why 4: Why was terminology different? → Because the model was optimized for one business unit's language and use cases.
- Why 5: Why was it deployed to a second unit without adjustment? → Because the deployment assumed the model was generic when it was domain-specific.

**True root cause:** Not a model quality problem. A deployment assumption problem. More training data would not have fixed this.

**Fix:** Domain-specific prompt layer per business unit. Terminology mapping exercise. Separate knowledge base per unit. User feedback loop to surface terminology gaps.

### Symptom 03 — Rate Questions Answered Well, Then Badly

**The story:** The model handled rate-related questions well for periods of time then suddenly started giving inconsistent or outdated answers. The team's instinct — retrain on current rate data.

**The 5 Whys diagnostic:**
- Why 1: Why were rate answers sometimes wrong? → Because the model was returning rates that were no longer current.
- Why 2: Why was it returning outdated rates? → Because the rate data in the knowledge base was not being updated when rates changed.
- Why 3: Why wasn't rate data being updated? → Because rate data was treated as static content in the knowledge base, not dynamic data.
- Why 4: Why was it treated as static? → Because the system architecture did not distinguish between stable and time-sensitive information.
- Why 5: Why was that distinction not made? → Because nobody assessed information volatility during the design phase. All content was treated the same.

**True root cause:** Not a model performance problem. An architecture and design problem. Retraining would have temporarily improved accuracy and failed again the next time rates moved.

**Fix:** Connect to live rate data source. Classify information by volatility at design. Automated alerts when rate data ages past threshold. Separate static from dynamic content layers.

## What the Design Thinking Lens Revealed

After diagnosing the three root causes, the Design Thinking lens added one more insight that almost changed the entire fix strategy.

The reps in business unit two had already mentally written off the tool. Desirability was gone. Technically fixing the domain mismatch would have produced a better model — but the reps would not have trusted it. The fix had to include a trust-rebuilding element: a pilot with a small group, visible improvement, reps involved in testing and feedback.

The technical fix without the human fix would have failed again — just for a different reason.

## What the Team Got Instead of a Retrain

The reason I built a diagnostic tool rather than just solving the three problems was that the team needed something they could use independently as their AI program scaled. They were going to face new model performance issues. Calling in external help every time was not sustainable.

The diagnostic framework gave them a repeatable process — a set of questions to ask before they touched the model, and a way to distinguish between a model problem, a data problem, a governance problem, and a human adoption problem, because each one requires a completely different response.

The full reusable framework — including the complete question set, the diagnostic map, and the Design Thinking integration — is available as a free download on this site.

> "The most expensive fix in AI is the one that solves the wrong problem."

All three root causes in this case were governance and architecture problems dressed up as model problems. Retraining would have temporarily improved one symptom and left two untouched.

Diagnose before you retrain. Always.

## What to Do This Week

Questions worth sitting with — not a task list, a thinking prompt:

- The next time someone says "the model is wrong" — ask which type of wrong before agreeing to any fix. Confidently wrong, outdated, vague, or inconsistent are four different problems.
- Ask who owns your knowledge base right now. If nobody can answer that in under 30 seconds, you have a governance gap that will surface as a model performance issue eventually.
- Identify one piece of information your AI system uses that changes frequently — rates, policies, product terms. Is it connected to a live source or sitting as a static document? If static, that is your next failure waiting to happen.
- Ask your team how much they trust the AI tool right now, on a scale of one to ten. Below seven means you have a desirability problem. No technical fix will solve a trust problem.
