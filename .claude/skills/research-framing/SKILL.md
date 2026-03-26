---
name: research-framing
description: Guides the user from a messy, vague research need to a well-scoped study design with clear decisions, assumptions, evidence plan, and method. Use this skill whenever the user mentions wanting to test something, run a study, do user research, put something in front of users, validate a design, scope a research project, or says anything that sounds like a vague research request that needs sharpening. Also use when the user asks "what should I test?" or "how should I research this?" or describes a product problem they want to investigate.
---

# Research Framing

This skill walks the user through research framing — going from a loose, messy research need to a well-scoped study. It draws on the frameworks defined in CLAUDE.md (Hall's process model, Calabro's evidence hierarchy, Anderson's FAST model) and deploys Nikki Anderson's framing prompts as situational tools.

## Interaction Pattern

Work through these phases in order. Do not skip phases, but adapt depth to what the user needs. Some phases may be brief if the user arrives with clarity; others will require extended dialogue.

**After every substantive response from the user, reflect back what you heard in structured form before moving to the next phase.** This is not optional.

### Phase 1: Get the Messy Brief

Ask the user to describe their research need in whatever form it takes. Explicitly invite messiness:

> "Tell me what you'd tell a UX researcher if you had one on staff. Don't clean it up — the messy version is more useful because it shows me where the real uncertainty lives."

Do not provide structure or a template at this stage. Let the user dump what's in their head. Listen for:
- Whether they're describing a problem or jumping to a solution/method
- Whether there's a decision embedded in the request or just a vague "we should test this"
- What evidence or prior research they reference (or don't)
- Which FAST elements are present and which are missing

After they respond, reflect back what you heard and identify what's missing before proceeding.

### Phase 2: Separate the Decision Layers

Using Hall's decision levels, identify what type of decision the research actually needs to support. The user will often collapse multiple levels into one request. Your job is to pull them apart.

**Strategic:** Are we solving the right problem? Is this the right direction?
**Tactical/Concept:** Is this the right solution approach? Does the concept resonate?
**Targeted/Evaluative:** Does this specific implementation work? Can people use it?

Common patterns to watch for:
- User says "test the design" but hasn't validated the concept underneath it
- User wants usability testing but the real uncertainty is strategic
- User treats the solution as decided and only wants to refine execution, when the assumptions underneath haven't been examined

Ask the user directly which layer they're trying to address. If you see layers they're skipping, name them and explain why they matter. Let the user decide what's in scope, but make the tradeoffs visible.

**Deploy Nikki's Decision Mapping prompt logic** (see references/nikki-framing-prompts.md) when the user has a stakeholder request or vague brief that needs the underlying decision surfaced.

**Deploy Nikki's Business Goal → Research Goal prompt logic** when the user has a clear business objective but no user-centered research framing.

### Phase 3: Surface Assumptions and Evidence

Once the decision level is clear, examine the evidence base for the current direction. Ask:

- What do you already know, and how do you know it?
- What type of evidence supports the current direction? (Apply Calabro: is it Category A behavioral evidence, Category B interpretation, or Category C preference/sentiment?)
- What's assumed without evidence?
- Where is the team's confidence higher than the evidence warrants?

This phase often reveals that a design direction is built primarily on Category B and C evidence (user interviews about what they want, stakeholder assumptions). That's not automatically wrong, but it should be named explicitly because it affects what needs testing.

**Deploy Nikki's Assumption Breaker prompt logic** when you identify a specific belief the team holds that hasn't been validated.

**Deploy Nikki's Risk-Mapping prompt logic** when the product decision touches conversion, key workflows, or other high-impact areas and risks haven't been mapped.

**Transition to structuring:** If after 2–3 exchanges in this phase the user hasn't articulated testable layers on their own, shift from questioning to proposing. Offer a framework for what's testable — for example, distinguishing concept validity, information architecture/mental model fit, and interaction usability as separate layers — and ask the user to validate, adjust, or reject it. The goal is to give the conversation structure to move toward, not to keep surfacing assumptions indefinitely. A good thinking partner knows when to offer a frame, not just another question.

### Phase 4: Define the Evidence Plan

Now that you know what decision the research supports and what's assumed versus known, define what evidence the study should collect. Work through this with the user:

**Category A — What behaviors would signal success or failure?**
Ask: "If you were watching someone use this and you couldn't ask them anything — what would you see them doing if the concept is working? What would worry you?"

This is the most important question in the framing process. It forces the user to define success in observable, behavioral terms rather than preference terms.

**Category B — What interpretation evidence matters?**
Ask: "What do you need to understand about how users think about this? What mental models or expectations matter?"

**Category C — Explicit deprioritization.**
Name it: "Preference and sentiment data (do they like it, does it feel good) is worth capturing but cannot be the primary evidence for this decision. If someone says 'I love it' but didn't actually use the features, the behavioral evidence takes priority."

After this discussion, reflect back the evidence plan in structured form.

### Phase 5: Scope the Study

Bring everything together into a clear scope. This should include:

1. **The decision** this research supports (one sentence)
2. **The population** — who should be in the study, and critically, who should not be
3. **The evidence plan** — what Category A, B, and C evidence you're targeting
4. **The artifact needed** — what level of prototype or stimulus is required
5. **The method** — what approach fits the decision, evidence needs, and constraints
6. **What's explicitly out of scope** — name what this study will NOT answer

**Deploy Nikki's Lean Research Approach prompt logic** when constraints are tight (timeline, resources, participant access, design readiness).

**Deploy Nikki's Vague Request → Actionable Brief prompt logic** to help produce the final scope summary if needed.

Present the scope as a structured summary and ask the user to confirm, correct, or refine.

**Transition to proposing:** Once you have the decision level, the testable layers, the evidence types, and the user has confirmed the framing is right — stop asking questions and draft the scope. Don't ask what artifact they have or clarify further constraints unless something is genuinely ambiguous. Propose a complete scope summary and let the user react to it. A concrete draft they can push back on moves the conversation forward faster than another round of questions.

**Handoff:** Once the scope is agreed, offer to save it to a study folder (e.g., `studies/[study-name]/scope.md`). If the user wants to move to test design — building the screener, questions, and protocol — direct them to the `/research-design` skill. Do not produce a test plan within the framing skill.

## When to Deploy Which Prompt

Nikki Anderson's framing prompts (detailed in references/nikki-framing-prompts.md) are tools, not a checklist. Use this guide:

| User arrives with... | Deploy... |
|---|---|
| A vague stakeholder request | Decision Mapping + Vague Request → Brief |
| A vague request that needs a precise scope | Vague Request → Precise Scope |
| A clear business goal but no research angle | Business Goal → Research Goal |
| A specific assumption the team holds | Assumption Breaker |
| A product change touching high-impact areas | Risk-Mapping |
| Too many research goals, scope creep | Prioritize Research Goals |
| A clear decision but unclear method | Decision → Method Recommendation |
| A clear decision and method already chosen | Go straight to Phase 4–5 |

## Important Reminders

- Do not accept "let's just do usability testing" as a starting point. Always ask what decision it supports first.
- The user knows research methodology — your job is to reactivate that knowledge through questions, not to teach it from scratch.
- If the user provides evidence from prior research, ask what type it is (Calabro categories) before accepting it as settled.
- The reflect-back after each phase is mandatory. It is the single most valuable interaction mechanic for this user.
- If a tangent emerges (e.g., a related but separate research question), flag it and ask whether to pursue it or park it.
