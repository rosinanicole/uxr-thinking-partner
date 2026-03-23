# UXR Thinking Partner

A set of Claude Code skills that serve as a user research thinking partner. Designed for product leaders who do research as one of many responsibilities and need structured support to think rigorously through research framing, fieldwork, synthesis, and communication.

## What This Is

This is not a research automation tool. It's a thinking partner that:

- Asks the questions a senior UX researcher would ask
- Helps you move from vague research needs to well-scoped studies
- Pressure-tests your assumptions and evidence quality
- Prevents you from jumping to methods before clarifying what you're actually trying to learn

The system is built on three interdependent frameworks:
- **Erika Hall's Design Research Process Model** — the structural sequence
- **Trevor Calabro's Evidence Hierarchy** — the evidence quality lens
- **Nikki Anderson's FAST Model and prompt toolkit** — the interaction tools

## How to Use

1. Clone this repo
2. `cd uxr-thinking-partner`
3. Run `claude` from this directory
4. Use `/research-framing` to start scoping a study

## Skills

| Skill | Status | Purpose |
|---|---|---|
| `/research-framing` | **Built** | Messy research need → well-scoped study |
| `/research-design` | **Built** | From Scope to Test Plan | Turn the scope into a test plan |
| `/research-checkpoint` | Scaffolded | Mid-study sanity checks and course correction |
| `/research-synthesis` | Scaffolded | Sharpen insights, validate patterns, check bias |
| `/research-communicate` | Scaffolded | Frame findings for audiences, build recommendations |

## Key Principles

- **AI never receives raw user data.** Only your summaries and interpretations.
- **AI supports thinking but does not decide.** It challenges, reframes, and pressure-tests — it doesn't interpret user behavior for you.
- **Behavioral evidence > sentiment.** When what users did and what users said conflict, behavior wins.

## Credits

- [Nikki Anderson](https://www.userresearchstrategist.com/) — FAST model and prompt frameworks
- [Trevor Calabro](https://trevorcalabro.substack.com/) — Evidence hierarchy (Category A/B/C)
- [Erika Hall](https://muledesign.com/) — Design Research Process Model
