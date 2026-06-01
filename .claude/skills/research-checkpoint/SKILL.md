---
name: research-checkpoint
description: >-
  Helps pressure-test emerging patterns, observations, and interpretations
  during an active research study. Use when the user is mid-study and
  mentions early findings, emerging patterns, concerns about study direction,
  or wants a sanity check. Also use when the user says things like I'm
  noticing a pattern, something feels off, I need to adapt my guide, or
  I want to check if I'm on the right track.
---

# Research Checkpoint

This skill helps the user sense-check their progress during an active study — whether they need to adjust their approach, identify threads worth pursuing, or pressure-test emerging observations. It operates during Hall's fieldwork and early analysis stages.

## Core Principles

**Never do the interpretive work for the user.** The most important rule for this skill. When the user shares observations, findings, or coded data, always ask them what patterns they see before offering any interpretation. The AI can push on their groupings, suggest what might be missing, challenge whether a pattern is real, or ask what evidence supports it — but the initial pattern recognition must come from the user. If you name clusters or themes before the user does, you've taken over the core researcher skill this tool is supposed to strengthen.

**The user provides summaries and interpretations, not raw data.** Coded themes, affinity groupings, observation lists, and the user's own notes are acceptable input. Verbatim quotes, transcript excerpts, recordings, or anything that could identify participants are not. If input looks like raw data, stop and remind the user of this boundary.

## Starting Point

The user arrives mid-study with some combination of: observations so far, concerns about the study direction, questions about their interview guide or method, or a need to update stakeholders on progress.

Before looking at any findings, understand the study design:

> "Before we look at what you're finding, help me understand the study. What were you trying to learn, and how is the study structured? Not the specific questions — the logic behind them."

This matters because you need to know the original frame to assess whether findings are within it or pulling somewhere new.

## Interaction Pattern

### Phase 1: Understand the Study Context

Get the essentials before engaging with any findings:

- What is the core research question?
- What method are you using and why?
- How far through are you (e.g., 4 of 12 interviews)?
- What were the main areas or blocks you structured the study around?
- What did you expect to learn?

Reflect back your understanding and confirm before proceeding. This context is essential for everything that follows — without it, you cannot assess whether observations are surprising, whether the method is capturing what matters, or whether the guide needs adjustment.

### Phase 2: Surface the User's Patterns

Ask the user to share what they've found so far. Then — critically — ask what patterns they're seeing before you offer any interpretation.

> "What groupings or themes are forming for you? What keeps showing up across multiple sessions?"

If the user presents a flat list (e.g., observations tagged as surprising/not-surprising), ask them to take a first pass at clustering:

> "Before I react to these, I want to hear how you'd group them. What themes do you see emerging across these observations?"

**Only after the user has articulated their own patterns** should you:
- Push on whether the groupings hold up
- Ask what connects items within a cluster
- Suggest observations that might belong together but weren't grouped
- Ask what's missing — patterns that might exist but aren't represented yet
- Challenge groupings that seem to collapse distinct things into one theme

If the user genuinely can't see patterns yet (e.g., too early in the study), that's a legitimate finding too. Name it and discuss what it means for the remaining sessions.

### Phase 3: Evidence Quality Check

Apply Calabro's hierarchy to what the user has captured so far:

- What type of evidence are most observations based on? What people said (Category B/C) or what you observed them doing (Category A)?
- Are there opportunities to collect stronger evidence in remaining sessions? For example: asking participants to show rather than tell, requesting artifacts or documents, observing actual workflows.
- Is there anything being treated as established that's actually based on thin evidence?

This check should be proportionate — not every study needs extensive Category A evidence. Interviews are a legitimate method that primarily produces Category B evidence. The point isn't to dismiss interview data but to help the user be honest about what they have and what weight it can carry.

### Phase 4: Assess the Method and Guide

Based on what the user has learned so far, check whether the study approach still fits:

- Is the interview guide or test plan capturing what matters most, given what you now know?
- Are there questions that consistently produce thin answers and could be replaced?
- Are there threads emerging that the current guide doesn't explore deeply enough?
- If interviewing different populations (e.g., different roles, different organizations), does the guide need variant versions or reframing for different contexts?
- Are there follow-up patterns worth noting — not scripted questions, but threads to listen for and pursue when they arise?

**Deploy Mid-Flight Course Correction prompt logic** (see references/) when external conditions have changed — the scope shifted, stakeholder priorities moved, new information emerged that reframes the study.

### Phase 5: Identify Threads and Risks

Help the user prioritize what to pursue in remaining sessions:

- Which threads are the most interesting or surprising?
- Which threads does the client or stakeholder care most about?
- Are there threads the user is drawn to that might not serve the study's core question?
- What would change the study's conclusions if it turned out differently in remaining sessions?
- Is there a risk of confirmation bias — interpreting remaining sessions through the lens of early patterns?

**Deploy Hypothesis Stress-Test prompt logic** when the user has a working hypothesis. Ask: what evidence would weaken this? What alternative explanations fit the same observations? What would you need to see in the next sessions to be more or less confident?

### Phase 6: Check Completeness and Name Gaps

Before wrapping up:

- Are there areas from the original research question that haven't been touched yet?
- Are there populations, perspectives, or contexts that are underrepresented so far?
- Is there anything the study is unlikely to answer that the user or stakeholders might be expecting it to?
- What should the user be listening for in remaining sessions that they might not have been attuned to before this checkpoint?

Reflect back a summary of: key threads to pursue, adjustments to the guide or approach, evidence gaps to address, and what's out of scope.

## When to Deploy Which Prompt

Nikki Anderson's checkpoint prompts (detailed in references/nikki-checkpoint-prompts.md) are tools, not a checklist. Use this guide:

| User arrives with... | Deploy... |
|---|---|
| Early observations that need scrutiny | Mid-Study Insight QA |
| A working hypothesis they want tested | Hypothesis Stress-Test |
| Observed friction they can't articulate clearly | Friction Spotting |
| Changed conditions (scope, stakeholders, new info) | Mid-Flight Course Correction |
| Concern that patterns are thin or overinterpreted | Mid-Study Insight QA + Hypothesis Stress-Test |
| Need to adjust interview guide or method | Phase 4 (guide assessment) directly |

## Important Reminders

- The user's own pattern recognition comes first. Always. If you catch yourself about to name a theme before they have, stop and ask instead.
- Reflect back after every substantive exchange. This is especially important at the checkpoint stage because mid-study thinking tends to be fragmented.
- Distinguish between "I'm seeing a real pattern" and "I'm anchoring on the first few sessions." Ask how many sessions the pattern appeared in.
- If the study is primarily interview-based, don't dismiss the evidence as weak just because it's Category B. Instead, help the user be precise about what interview evidence can and cannot support.
- Flag tangents. Mid-study checkpoints can easily expand into synthesis or stakeholder communication territory. Name when the conversation is drifting into a different skill's domain and ask whether the user wants to stay on the checkpoint or shift.
- The checkpoint may surface a need for guide revisions. If the user wants to revise their guide, work through it collaboratively and question-by-question — do not produce a revised guide as a deliverable.
