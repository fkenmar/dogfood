# dogfood

> The AI co-founder honest enough to tell you to **kill your idea** — and show its work.

Most AI "idea validators" are flattering hype machines. **dogfood** is the opposite: hand `/founder` a
raw idea and a team of specialist agents researches the market, drafts a plan through Y-Combinator's
rules, then a cold adversarial critic with *no stake in the draft* returns `KILL IT` / `MAJOR REWORK` /
`PROCEED WITH FIXES` — and loops critique↔revise until the plan survives. You leave with a validated,
execution-ready project doc, or an honest verdict that saves you three months.

The name is the method: we ran dogfood on itself. Verdict — **MAJOR REWORK**. The flaws it found are in
[`examples/dogfood-self-run.md`](examples/dogfood-self-run.md), unedited, and they shaped this README.

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
8. **Pitch strategist** writes the launch/investor narrative.

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
| `/pitch` | `pitch-strategist` | Launch/investor narrative + slide-by-slide outline |

## What it is — and isn't

- **It is** a fast way to pressure-test an idea, expose the assumptions it rests on, and turn a vague
  notion into a concrete, sequenced plan.
- **It is *not* a substitute for talking to real customers.** No agent can interview your market for
  you. dogfood *designs* the validation experiments — who to talk to, the questions, the cheapest
  pre-build test — but you still have to go run them. A doc that survived an AI critique has survived
  contact with a language model, not with reality.

## Install

Requires [Claude Code](https://claude.com/claude-code).

**As a plugin (recommended):**

```
/plugin marketplace add fkenmar/dogfood
/plugin install dogfood
```

**Or manually** — copy the commands and agents into your config:

```bash
git clone https://github.com/fkenmar/dogfood
cp -r dogfood/commands/* ~/.claude/commands/
cp -r dogfood/agents/*   ~/.claude/agents/
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

[`examples/dogfood-self-run.md`](examples/dogfood-self-run.md) — the full pipeline run on dogfood
itself, including the critique that returned **MAJOR REWORK**.

## Disclaimer

dogfood's output is **AI-generated** and may be wrong. The legal (`/legal-review`), financial
(`/financials`), and market (`/market-research`) sections are **not** legal, financial, investment, tax,
or professional advice and create no professional relationship — treat everything as a starting point and
verify with qualified professionals before relying on it. See [DISCLAIMER.md](DISCLAIMER.md).

## License

[MIT](LICENSE).
