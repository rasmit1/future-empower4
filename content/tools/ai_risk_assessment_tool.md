
---
title: "AI Risk Assessment Tool"
date: 2026-01-01
description: "Answer 8 questions about your AI deployment and get an instant risk tier — High, Medium, or Low — with specific actions to take. Takes 3 minutes. No theory. Just your tier and what to do next."
author: "Rashmi Mittal"
tags: ["AI Governance", "Risk Assessment", "AI Strategy", "Enterprise AI", "Financial Services"]
type: "tool"
draft: false
---

> **Takes 3 minutes. No theory. Just your tier and what to do next.**

Answer these 8 questions about a specific AI system you are deploying or planning to deploy. Score each answer — Low = 1, Medium = 2, High = 3. Add up your total at the end.

---

## How to score

For each question circle or note your answer. Each answer carries a score:

- **Low risk answer = 1 point**
- **Medium risk answer = 2 points**
- **High risk answer = 3 points**

**Total your score at the end and find your tier.**

---

## Question 1 — Who are the end users?

The closer the AI is to real customers making real decisions, the higher the risk.

| Answer | Score |
|--------|-------|
| Internal employees only — low-stakes tasks (e.g. internal search, meeting summaries, code assistance) | 1 |
| Internal employees — consequential decisions (e.g. customer service reps, analysts, underwriters using AI to inform decisions) | 2 |
| External customers directly (e.g. chatbots, automated decisions, customer-facing recommendations) | 3 |

**My score: ___**

---

## Question 2 — Does it affect consequential decisions?

Does this AI system make or directly influence decisions that affect people's money, credit, employment, or legal rights? Regulatory frameworks specifically flag these as high-risk categories.

| Answer | Score |
|--------|-------|
| No — it is purely informational or productivity-focused | 1 |
| Partially — it informs decisions but a human makes the final call | 2 |
| Yes — it makes or heavily automates consequential decisions (e.g. credit approval, fraud flags, hiring screens) | 3 |

**My score: ___**

---

## Question 3 — What happens if the AI gives a wrong answer?

Impact severity determines how much governance and verification the system needs.

| Answer | Score |
|--------|-------|
| Minor inconvenience — easily corrected, no lasting impact | 1 |
| Moderate impact — rework required, trust damaged, incorrect internal decision | 2 |
| Serious impact — financial, legal, reputational, or safety consequences | 3 |

**My score: ___**

---

## Question 4 — Does it process sensitive personal data?

Financial data, health data, biometric data, and demographic data all trigger specific regulatory obligations.

| Answer | Score |
|--------|-------|
| No personal data — uses only anonymised or aggregate data | 1 |
| General personal data — name, contact, preferences | 2 |
| Sensitive personal data — financial, health, biometric, or demographic | 3 |

**My score: ___**

---

## Question 5 — Is there a human reviewing AI outputs?

Human oversight is a primary risk mitigation mechanism. Its absence significantly raises the risk tier.

| Answer | Score |
|--------|-------|
| Yes — every output is reviewed by a human before use | 1 |
| Partially — humans review flagged or low-confidence outputs only | 2 |
| No — fully automated, no human review in the loop | 3 |

**My score: ___**

---

## Question 6 — How explainable are the AI decisions?

Explainability is both a regulatory requirement in many contexts and a governance essential. You cannot govern what you cannot explain.

| Answer | Score |
|--------|-------|
| Fully explainable — we can explain every decision in plain language | 1 |
| Partially explainable — we understand key factors but not every decision | 2 |
| Black box — we cannot explain individual decisions | 3 |

**My score: ___**

---

## Question 7 — Is the system monitored in production?

A model that was accurate at launch can become inaccurate or biased over time. Without monitoring you will not know until something goes wrong.

| Answer | Score |
|--------|-------|
| Yes — active monitoring with defined KRIs and alerts | 1 |
| Partially — we monitor but reactively, not proactively | 2 |
| No — we are not actively monitoring this system in production | 3 |

**My score: ___**

---

## Question 8 — Have control partners signed off?

In regulated industries — especially financial services — governance sign-off is not optional. Its absence is itself a risk.

| Answer | Score |
|--------|-------|
| Yes — full sign-off from legal, compliance, and risk before deployment | 1 |
| Partially — some review but not complete sign-off | 2 |
| No — control partners have not been involved | 3 |

**My score: ___**

---

## Your total score

Add up all 8 scores: **Total = _____ / 24**

---

## Find your risk tier

| Total score | High answers (score of 3) | Risk tier |
|-------------|--------------------------|-----------|
| 18 or above | Any | **HIGH RISK** |
| Any | 4 or more | **HIGH RISK** |
| 11 to 17 | 2 or 3 | **MEDIUM RISK** |
| 10 or below | 0 or 1 | **LOW RISK** |

---

## HIGH RISK tier

**What this means**

This AI system has significant risk characteristics that require immediate governance attention. Board-level oversight, external audit consideration, and documented controls are required before or immediately after deployment.

**Governance requirements**
- Board or executive sign-off required before deployment
- External audit or independent review strongly recommended
- Full regulatory compliance assessment — FCA, CFPB, SR 11-7 as applicable
- Bias and fairness testing mandatory before any customer-facing deployment
- Human oversight required for all consequential outputs
- Model card with full risk documentation
- Audit trail for every decision the AI influences
- Monthly monitoring review minimum
- Incident response plan documented and tested
- Customer appeals process if AI affects their rights

**Actions — in order**

**Today** — Stop or restrict deployment if any of these are missing: human oversight, legal sign-off, bias assessment. Do not proceed without them.

**This week** — Escalate to legal and compliance immediately. Brief them on the system, its scope, and the questions in this assessment. Get their input before any further action.

**Within 2 weeks** — Complete bias and fairness assessment across all demographic groups the system affects. Document findings. Address gaps before deployment.

**Within 1 month** — Implement monitoring and alerting. Define KRIs — key risk indicators — with thresholds that trigger automatic review. Monthly performance review minimum.

**Ongoing** — Quarterly governance review with risk, compliance, and product owner. Board-level reporting on AI risk annually minimum.

---

## MEDIUM RISK tier

**What this means**

This AI system has moderate risk characteristics. Senior leadership sign-off, documented controls, and a defined monitoring cadence are required. Quarterly review recommended.

**Governance requirements**
- Senior leadership or CISO sign-off required
- Documented controls in place before deployment
- Legal and compliance awareness — formal sign-off recommended
- Quarterly monitoring review minimum
- Human review for edge cases — confidence thresholds should trigger escalation
- Model card documenting capabilities and limitations
- Basic audit trail for consequential decisions
- Defined escalation path when model flags uncertainty
- Annual full governance review

**Actions — in order**

**This week** — Get legal and compliance awareness if not already in place. They do not need to block — they need to know. Brief them on scope and planned controls.

**Within 2 weeks** — Document a model card — what the system does, its limitations, its risk tier, its owner, and when it will next be reviewed.

**Within 1 month** — Set up monitoring — at minimum a monthly check of model performance against actual outcomes. Define what would trigger an urgent review.

**Ongoing** — Quarterly review cadence with the product owner and risk partner. Annual formal governance review with documented sign-off.

---

## LOW RISK tier

**What this means**

This AI system has low risk characteristics. Standard controls and light-touch governance apply. Annual review is sufficient unless the system scope changes.

**Governance requirements**
- Named product owner — one person accountable
- Basic documentation — what it does and who uses it
- Simple user feedback mechanism — how users flag problems
- Annual review — confirm scope has not changed and tier is still accurate

**Actions — in order**

**This week** — Name a product owner. One person accountable for this system. Not a team. One person.

**Within 2 weeks** — Write a one-page brief — what the system does, who uses it, and how users can flag if something goes wrong. File it somewhere findable.

**Annually** — Reassess the risk tier. If scope expands to new users, new decisions, or new data, run this assessment again. Low risk today can become medium risk tomorrow.

**Watch for** — Scope creep. The biggest risk at Low tier is that the system grows beyond what was assessed. If users start relying on it for consequential decisions it was not designed for — reassess immediately.

---

## Important notes

**One system at a time** — Each AI system should be assessed separately. A low-risk internal tool and a high-risk credit model cannot share a risk tier even if they are built on the same platform.

**Reassess when things change** — A tier is not permanent. Reassess when the user base changes, when the decisions it influences change, when the data it processes changes, or when the regulatory environment changes.

**The tier is the floor not the ceiling** — These are minimum governance requirements. Your organisation may choose to apply higher standards. That is always appropriate. Applying lower standards than the tier requires is not.

**This is a starting point not a substitute for professional advice** — In regulated industries — financial services, healthcare, insurance — always involve your legal and compliance teams in the governance design for any AI system regardless of tier.

---

*Rashmi Mittal is an AI Transformation & Product Leader with 15+ years in financial services. He helps organisations move AI from pilot to production — unblocking the technical, business, and human barriers that stop AI programmes from scaling. 🌐 [futureempowered.com](https://futureempowered.com)*

`#AIGovernance #RiskAssessment #AITransformation #EnterpriseAI #AIStrategy #FinancialServices #FutureEmpowered`
