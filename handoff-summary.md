# UXR Thinking Partner — Handoff Summary

## What this is
A set of Claude Code skills that serve as a user research thinking partner. The project lives in a GitHub repo with a CLAUDE.md foundation file and skills in `.claude/skills/`. Start by reading the repo's CLAUDE.md and README.md for full context.

## What's been built and tested

### research-framing (tested 3x, iterated twice)
Guides from a messy research need to a well-scoped study. Tested against a real project: OCCRP homepage redesign to increase returning user engagement.

**Key design lessons from testing:**
- The skill was too slow to transition from questioning to proposing. Two targeted instructions were added: one at Phase 3 (after assumption-surfacing, offer a testable framework rather than asking indefinitely) and one at Phase 5 (once the decision/layers/evidence are clear, draft the scope rather than asking more questions).
- The skill initially produced a full test plan when asked, which the user rubberstamped without reasoning through it. This led to a foundation-level guardrail: never produce a complete deliverable without working through key decisions collaboratively.

### research-design (tested 1x, iterated once)
Bridges a completed scope to a runnable test design (screener, structure, questions, protocol). Tested against the same OCCRP homepage project.

**Key design lessons from testing:**
- The skill conceded too quickly when the user pushed back on question framing feedback. An instruction was added about holding ground on vocabulary, evidence categories, and leading language — restating the reason rather than deferring after one objection.
- This principle was also added to the CLAUDE.md as a general guardrail.

### research-checkpoint (tested 1x against a different project)
Helps sense-check emerging patterns during active fieldwork. Tested against a real project: newsroom reach operationalization case study (interview-based, 4 of 10-12 interviews complete).

**Key design lesson from testing:**
- The AI named three observation clusters from the user's data before asking the user what patterns they saw. This is the most important anti-pattern for the checkpoint skill. The core principle: always ask the user what patterns they see before offering any interpretation. The AI can challenge, extend, and pressure-test — but initial pattern recognition must come from the user.

### research-synthesis (scaffolded, not designed)
Needs a live design session against real post-study work.

### research-communicate (scaffolded, not designed)
Needs a live design session against real communication challenge.

## Design methodology that worked

Every skill was designed the same way:
1. Work through a real research problem collaboratively
2. Notice which moments in the conversation were most useful
3. Extract the interaction pattern from what helped
4. Build the skill, test it against the same problem
5. Compare the skill's output to the live conversation
6. Identify specific failure modes and fix with targeted instructions
7. Retest

This approach consistently produced better skills than designing abstractly from prompt templates.

## Key architectural decisions

- **CLAUDE.md** is the shared foundation (always loaded). Contains user context, OCCRP context, three frameworks (Hall, Calabro, Anderson FAST), interaction principles, and guardrails.
- **Skills** are stage-specific. Each has a SKILL.md with the interaction pattern and a references/ directory with Nikki Anderson's prompts for that stage.
- **Nikki's prompts are tools, not sequences.** Each skill has a deployment table mapping situations to prompts. The skill assesses what the user needs and deploys the relevant prompt, rather than walking through all prompts mechanically.
- **Nikki's prompts should not be rewritten** to match the interaction style. The SKILL.md handles the interaction pattern; the reference prompts provide analytical logic to apply within that pattern. Rewriting them double-encodes principles and distorts the original content.
- **Three frameworks are interdependent:** Hall provides the sequence, Calabro provides the evidence quality lens at every stage, Anderson's FAST structures effective user input.
- **The Hall PDF** (Mule Design Research Process Model v2) lives at `references/hall-design-research-process-model.pdf` and is referenced in CLAUDE.md.

## Important guardrails discovered through testing

1. **Never produce deliverables directly.** Even when asked. "Understood, let's build that together."
2. **Never do interpretive work before the user.** Especially pattern recognition, clustering, and theming. Ask first, then push on what they surface.
3. **Don't concede too quickly.** When pushing back on question framing or evidence quality, restate the reason rather than deferring. Two concessions in a row signals excessive agreeableness.
4. **Transition from questioning to proposing.** The skill needs explicit signals for when to stop asking questions and offer structure. Without these, it stays in questioning mode too long.
5. **Evidence quality checks are proportionate.** Interview-based studies primarily produce Category B evidence — don't dismiss this as weak, but help the user be honest about what it can support.

## Active research projects

### OCCRP Homepage Concept Test
- Scope completed (saved as homepage-concept-test-scope.md)
- Test design drafted: screener, first impression, browsing scenario, follow-up questions
- Next step: build prototype in Figma Make, set up test in Lyssna
- Decision: whether fixed structural elements (filters, content categorization, new/archived distinction) are ready to build

### Newsroom Reach Operationalization Case Study
- Freelance project for external client
- Interview-based study, 4 of 10-12 interviews complete
- Three emerging clusters identified: measurement fragmentation, aspiration-vs-implementation gap, organizational power dynamics
- Next steps: interview editorial/leadership (not just audience teams), adapt guide for different audiences, possibly incorporate client's quantitative reach data

## What's still to do

1. **Test the checkpoint skill** against the newsroom reach project to see if it handles the "ask user for patterns first" principle correctly
2. **Design and build research-synthesis** through a live session with real post-study data
3. **Design and build research-communicate** through a live session with a real stakeholder communication need
4. **Consider a continuous discovery skill** — the user mentioned doing weekly user interviews without fixed questions, wanting to build a practice around that. Separate from the study-specific skills.
