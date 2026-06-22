---
title: "The 15-Minute AI Fix Viability Scorecard"
date: 2026-06-14
draft: false
categories: ["Futuristic Transformation", "Organization Science"]
description: "Before approving budget or developer time to fix a failing AI model, score the proposed solution across four operational dimensions."
tags: ["AI diagnostics", "model failure", "scorecard", "design thinking", "AI governance", "viability"]
---

Before approving budget or developer time to fix a failing AI model, score the proposed solution across these four operational dimensions.

Rate each category from **1** (Severe Friction / High Risk) to **5** (Seamless / High Return).

---

## 1. Desirability — Trust Quotient

- [ ] **Adoption risk:** Users will embrace this fix — previous model instability has not burned trust beyond repair.
  > If trust is damaged, map a change-management step before scoring higher than 2.

- [ ] **Workflow alignment:** The solution fits how your team already works — no forced behavioral shift required.
  > Unnatural pivots require training budget. If none is planned, reduce score by 1.

**Section score (1–5):** `[ ]`

---

## 2. Usability — Friction Factor

- [ ] **Operational steps:** This fix does not add net-new clicks, prompts, or manual verification steps to the daily workflow.
  > Every extra step is a defection point. Count the added steps; if >2, cap score at 3.

- [ ] **Fallback protocol:** A clear, built-in fallback loop exists for when the model remains uncertain — users never hit a dead end.
  > If the fallback requires a ticket or an IT call, it won't be used. Design must be self-service.

**Section score (1–5):** `[ ]`

---

## 3. Feasibility — Tech Reality

- [ ] **Talent capability:** Your internal team can maintain this change independently — no heavy vendor dependency is created.
  > If maintenance requires the vendor's PS team, add vendor lock-in cost to viability section.

- [ ] **Pipeline architecture:** Existing infrastructure supports this change without a database overhaul or replatform event.
  > Any "we'd need to rebuild X first" is a red flag. Break that into a separate initiative and rerun this scorecard.

**Section score (1–5):** `[ ]`

---

## 4. Viability — Financial Truth

- [ ] **ROI justification:** The lifetime business value of this fix outpaces implementation cost plus ongoing compute — you can model it in a spreadsheet, not just feel it.
  > If you cannot produce a rough NPV in 15 minutes, the ROI case is not ready. Score ≤2 until it is.

- [ ] **Compliance protection:** This fix actively reduces verified legal, brand, or security exposure — not theoretical risk.
  > Cite the specific regulation, incident, or audit finding. Vague risk does not justify budget.

**Section score (1–5):** `[ ]`

---

## 🚦 Decision Gate

Add your four section scores:

| Score | Verdict | Action |
|-------|---------|--------|
| **17–20** | **Greenlight — proceed to deployment** | The fix is technically sound, operationally viable, and commercially justified. Assign a sprint, set a rollback threshold, and ship. |
| **13–16** | **Proceed with conditions** | The technical path is valid but needs support work first. Identify your lowest-scoring dimension, resolve the blocker, then rescore before committing budget. |
| **Under 13** | **Kill the fix — return to root-cause analysis** | Severe friction, weak ROI, or user rejection risk makes this fix more expensive than the problem. Document the failure mode and rerun root-cause analysis before proposing a new solution. |

**Total score:** `___` / 20

**Decision:** `_________________________________`

---

*Framework by Future Empowered · [futureempowered.com](https://futureempowered.com)*
