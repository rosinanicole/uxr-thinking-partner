# Nikki Anderson's Framing Prompts

These prompts are from Nikki Anderson's article "Use AI Across Your User Research Process" (userresearchstrategist.com). They are tools to deploy situationally during the framing process — not a sequence to walk through mechanically. Load the relevant prompt's logic when the user's situation matches the "when to use it" criteria.

**Important:** These prompts are written for the AI to execute as thinking-partner activities. They should be adapted to the interactive, question-driven style defined in CLAUDE.md — do not simply output all sections at once. Walk through them conversationally, reflecting back and checking understanding at each step.

---

## Prompt 1: Decision Mapping

### When to use it
When a stakeholder sends a vague request like "Can you look into this?", "We need research before launch", or any request where the decision underneath is unnamed.

### Logic to follow
1. **Extract the surface request.** What does the stakeholder explicitly say they want?
2. **Identify possible underlying decisions.** List 3–5 potential decisions this research might influence. Include strategic (long-term), tactical (short-term), and political (stakeholder confidence, team reputation) decisions.
3. **Map the stakes.** For each potential decision: what happens if the team moves forward without research? What happens if they choose the wrong path? Which metrics or teams carry the most risk?
4. **Identify blind spots.** What context is missing? What assumptions seem baked in?
5. **Output a one-sentence alignment summary** capturing the real purpose of the research.
6. **Suggest clarifying questions** — 5–7 questions to confirm alignment, scope, risk, and expectations.

### Follow-up angles
- Rewrite the alignment summary for different audiences (exec, PM, designer)
- Surface political tensions that might be shaping the request
- Identify what evidence would help the team make a confident decision

---

## Prompt 2: Risk Mapping

### When to use it
When someone proposes a change touching conversion, billing, onboarding, or anything revenue-adjacent. When a team is rushing toward release. When a stakeholder says "it's a small change, we don't need research."

### Logic to follow
1. **List overlooked risks** — 6–8 risks across user behavior, product experience, support load, technical constraints, trust, and business impact.
2. **Tie each risk to an insight gap.** For every risk, identify the missing knowledge that makes it risky.
3. **Create research questions.** Turn insight gaps into natural-language research questions.
4. **Map product/business impact.** For each risk: which metric might shift? Which team carries the impact? What early signals would reveal the risk in the wild?
5. **Prioritize.** Rank by impact and urgency with short justification.

### Follow-up angles
- Turn top risks into testable hypotheses
- Draft a stakeholder summary of risks
- Recommend the fastest research plan for the top two risks

---

## Prompt 3: Assumption Breaker

### When to use it
When someone confidently states "Users prefer X," "People always do Y," or "Everyone hates Z." When an exec repeats a belief that has never been validated. When assumptions are driving product decisions more than evidence.

### Logic to follow
1. **Analyze the assumption.** What belief, fear, or past experience might be driving it? What makes it unreliable?
2. **Articulate risks.** What failures could happen if it's wrong? Which user behaviors or business outcomes could be impacted?
3. **Reframe into hypotheses.** Write 3–5 testable hypotheses describing observable user behavior.
4. **Create lean research questions.** Draft 3 questions to evaluate or challenge the hypotheses.
5. **Suggest next steps.** Provide 3 lean testing approaches suitable for tight timelines or limited access.

### Follow-up angles
- Turn hypotheses into a micro-study plan
- Draft a message to the PM explaining why evidence is needed

---

## Prompt 4: Vague Request → Actionable Brief

### When to use it
When a stakeholder gives a request so vague it feels like solving a riddle. When the request is driven by panic, not clarity. When "quick research?" actually requires strategy.

### Logic to follow
1. **Extract intent.** What is the stakeholder trying to understand or achieve?
2. **Identify urgency.** What pressures might be shaping their request?
3. **Map assumptions.** List assumptions hidden in the message.
4. **Translate into research goals.** Write 2–4 user-centered goals tied to real behaviors or perceptions.
5. **Draft clarifying questions** — 5–7 to confirm alignment and scope.
6. **Output a project summary.** One-paragraph brief that can be sent back to stakeholders.

### Follow-up angles
- Rewrite as a concise email or Slack message
- Rewrite for a designer audience
- Highlight where stakeholder goals conflict with each other

---

## Prompt 5: Business Goal → Research Goal

### When to use it
When the business goal is clear but the user angle is not. Examples: increase activation, reduce churn, lift free-to-paid. Useful for bridging business language and human-centered research language.

### Logic to follow
1. **Identify the user problem.** What user behaviors, beliefs, or barriers might connect to the business goal?
2. **Generate hypotheses.** List 5–7 hypotheses about what might be blocking users.
3. **Create research goals.** Turn business goal + hypotheses into 3–4 user-centered research goals.
4. **Connect research to outcomes.** For each goal: which outcome it ties to, which metric might shift, who depends on this insight.
5. **Write an alignment statement.** One sentence linking user needs to the business goal.

### Follow-up angles
- Turn into a kickoff slide
- Draft a short alignment message to the PM

---

## Prompt 6: Lean Research Approach

### When to use it
When timeline is tight, design isn't ready, team is anxious, scope is too big, or PM wants answers "this week." When you need research but constraints are real.

### Logic to follow
1. **Assess constraints.** List the constraints that matter most.
2. **Recommend methods.** Propose 2 lean approaches with explanations for why they fit.
3. **Outline trade-offs.** For each method: what we gain, what we lose, what we must watch out for.
4. **Draft a mini-plan.** Goals, method, participants, timeline, deliverables, and the decision the plan supports.

### Follow-up angles
- Turn into a Slack update for the team
- Draft a script for lean sessions
