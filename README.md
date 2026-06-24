# Founder Studio

> An AI startup studio for Claude Code. Hand `/founder` a raw idea; a team of specialist agents
> interrogates it, researches the market, tears it apart, and hands you back a validated,
> execution-ready project doc — or an honest verdict to kill it before you waste months.

Most AI "idea validators" are flattering hype machines. Founder Studio is built around the opposite
instinct: **a plan has to survive a cold, adversarial critique before it ships.** The honesty is the
whole point — if your idea is weak, it will tell you, and show its work.

## What you get

`/founder "your idea"` runs an 8-phase pipeline:

1. **Grills you** on founder-market fit (only if the idea is thin).
2. **Researches the market** and drafts a first plan through Y-Combinator's rules.
3. **Critiques it cold** — a fresh adversarial agent returns `KILL IT` / `MAJOR REWORK` / `PROCEED WITH FIXES`.
4. **Revises** to kill every fatal flaw — looping critique↔revise until the plan survives.
5. **Ships the project doc** (14 sections: problem, narrow user, wedge, why-now, market, competition,
   model, GTM, MVP, validation, risks, 90-day plan, critique log).
6. **Convenes the specialist team** — validation, UX, technical, legal, finance, and growth each deepen
   their section.
7. **Project manager** turns it all into a sequenced execution roadmap.
8. **Pitch strategist** writes the investor narrative + deck outline.

The output ends with a **critique log** showing how the idea changed under fire.

## The team

Every specialist is also a standalone command — point it at any idea or doc on its own.

| Command | Agent | What it does |
|---|---|---|
| `/founder` | *(orchestrator)* | Runs the whole studio end-to-end |
| `/critique` | *(cold subagent)* | Brutally honest teardown: verdict + ranked fatal flaws |
| `/market-research` | `market-researcher` | Market size, competitors, willingness to pay, why-now — cites sources, won't fabricate numbers |
| `/validate` | `customer-discovery` | Riskiest assumption, Mom-Test interview script, the cheapest pre-build test |
| `/ux` | `product-designer` | Core user flows, key screens & states, UX principles, v1 scope |
| `/tech-plan` | `technical-founder` | Feasibility, pragmatic stack, architecture, build-vs-buy, technical MVP |
| `/legal-review` | `startup-lawyer` | Entity, equity/IP, privacy, regulatory exposure *(issue-spotting, not legal advice)* |
| `/financials` | `finance-lead` | Pricing, unit economics (CAC/LTV/payback), runway, default-alive math |
| `/growth` | `growth-marketer` | First-100-users playbook, the channel to win first, launch, growth loop |
| `/roadmap` | `project-manager` | Sequenced execution roadmap with acceptance checks and a cut list |
| `/pitch` | `pitch-strategist` | Investor narrative + slide-by-slide deck outline |

## What it is — and isn't

- **It is** a fast way to pressure-test an idea, expose the assumptions it rests on, and turn a vague
  notion into a concrete, sequenced plan.
- **It is *not* a substitute for talking to real customers.** No agent can interview your market for
  you. The studio *designs* the validation experiments — who to talk to, the questions, the cheapest
  pre-build test — but you still have to go run them. A doc that survived an AI critique has survived
  contact with a language model, not with reality.

## Install

Requires [Claude Code](https://claude.com/claude-code).

**As a plugin (recommended):**

```
/plugin marketplace add fkenmar/founder-studio
/plugin install founder-studio
```

**Or manually** — copy the commands and agents into your config:

```bash
git clone https://github.com/fkenmar/founder-studio
cp -r founder-studio/commands/* ~/.claude/commands/
cp -r founder-studio/agents/*   ~/.claude/agents/
```

## Usage

```
/founder a tool that auto-files quarterly taxes for freelancers
```

Point it at a file instead of a sentence:

```
/founder ./idea.md
```

Or run any single specialist on its own:

```
/critique ./my-plan.pdf
/market-research B2B onboarding analytics for fintechs
/validate ./idea.md
```

## Example

[`examples/founder-studio-self-review.md`](examples/founder-studio-self-review.md) — Founder Studio run
on *itself*, including the critique that returned **MAJOR REWORK**.

## License

[MIT](LICENSE).
