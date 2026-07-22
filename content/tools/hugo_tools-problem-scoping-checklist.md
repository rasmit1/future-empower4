---
title: "The 10-Minute AI Problem Scoping Checklist"
description: "Before you diagnose anything, map the full landscape of the problem. Run this checklist before touching a root-cause analysis."
date: 2026-07-18
draft: false
categories: ["Tools"]
tags: ["AI Diagnostics", "Problem Scoping", "AI Transformation", "Enterprise AI"]
author: "Rashmi Mittal"
---

Before diagnosing anything, build a complete picture of the situation. Skipping this step means you risk running a root-cause analysis on the wrong symptom entirely.

Run through all six questions below before moving to root-cause analysis.

**WHO — Who is affected?**
- [ ] Which users or teams are experiencing the problem?
- [ ] Is it everyone, or specific groups only?
- [ ] Who reported it first and when?
- [ ] Who owns the system — technically and operationally?
- [ ] Who are the downstream recipients of the wrong outputs?

**WHAT — What exactly is happening?**
- [ ] What type of wrong answer — confidently wrong, outdated, vague, inconsistent, or discriminatory?
- [ ] What is the model being asked to do?
- [ ] What does a correct answer look like?
- [ ] What has already been tried to fix it?
- [ ] What is the business impact of the wrong answer?

**WHEN — When did it start?**
- [ ] When did the wrong answers first appear?
- [ ] Was onset sudden or gradual?
- [ ] When does it happen — always, intermittently, at specific times?
- [ ] What changed in the business or environment around that time?
- [ ] When was the model last updated or retrained?

**WHERE — Where in the system?**
- [ ] Where in the workflow does the wrong answer appear?
- [ ] Is it isolated to one business unit or system-wide?
- [ ] Where does the model get its information from?
- [ ] Where is the knowledge base stored and who manages it?
- [ ] Where does the output go after the model generates it?

**WHY — Why does it matter?**
- [ ] Why is this output consequential — what decisions does it inform?
- [ ] Why are users relying on this output without verification?
- [ ] Why hasn't it been fixed already?
- [ ] Why does the team believe retraining is the solution?
- [ ] Why was the system designed this way originally?

**HOW — How is it manifesting?**
- [ ] How often does it happen?
- [ ] How is the wrong answer different from the correct one?
- [ ] How is the model currently monitored?
- [ ] How were users trained to use the system?
- [ ] How confident does the model appear when it gives wrong answers?

## 🚦 Decision Gate

After completing the checklist, answer:

Number of distinct problem types identified: ___

Who is affected by each: _________________________________

What pattern do timing and location suggest: _________________________________

**If you identified more than one distinct symptom** — treat each one as a separate problem. Do not diagnose them together; run a root-cause analysis on each symptom individually.

---
*Ready to find the root cause? Continue with [The 5 Whys Root Cause Drill](/tools/five-whys-drill/), or read the full [AI Model Diagnostic Framework](/guides/ai-model-diagnostic-framework/) for the complete method.*
