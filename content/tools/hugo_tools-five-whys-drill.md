---
title: "The 5 Whys Root Cause Drill"
description: "A fillable template to find the true root cause of an AI model issue — before recommending a fix. Most teams stop at Why 2. The real cause is almost always at Why 4 or 5."
date: 2026-07-18
draft: false
categories: ["Tools"]
tags: ["AI Diagnostics", "5 Whys", "Root Cause Analysis", "AI Transformation", "Enterprise AI"]
author: "Rashmi Mittal"
---'

The first answer is almost never the real cause. Most organizations stop at Why 2 or Why 3 and fix the symptom instead of the source. Run this drill separately for each distinct symptom you identified during problem scoping.

## Your Root Cause Drill

**Symptom:** _________________________________

| Why | Question | Answer |
|---|---|---|
| Why 1 | Why is this happening? | |
| Why 2 | Why is *that* happening? | |
| Why 3 | Why is *that* happening? | |
| Why 4 | Why is *that* happening? | |
| Why 5 | Why is *that* happening? | |

**True root cause:** _________________________________

**Fix direction:** _________________________________

## The Rule

If your Why 5 answer still sounds like a technical fix, you haven't gone deep enough. The true root cause is almost always a governance gap, ownership gap, design assumption, or process failure — not a model failure.

## Quick Reference — Common Patterns

| Surface Symptom | Likely Root Cause at Why 4–5 | Fix Direction |
|---|---|---|
| Confident wrong answers | No grounding — model using memory, not documents | RAG implementation |
| Outdated information | No knowledge base ownership or update process | Governance and process |
| Accuracy declining over time | Concept drift — real world changed, model didn't | Retraining + monitoring |
| Vague or unhelpful answers | Domain mismatch — wrong knowledge base for this user | Prompt and retrieval layer |
| Different outcomes for same inputs | Historical bias encoded in training data | Fairness audit + legal escalation |
| Works in testing, fails in production | Test data not representative of real users | Test set redesign |
| Inconsistent answers | Temperature too high or no grounding | Configuration + RAG |

---
*Found your root cause? Confirm your fix will actually be adopted with [The 15-Minute AI Fix Viability Scorecard](/tools/ai-fix-viability-scorecard/), or read the full [AI Model Diagnostic Framework](/guides/ai-model-diagnostic-framework/) for the complete method.*
