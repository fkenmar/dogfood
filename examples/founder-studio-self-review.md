# Example: Founder Studio, reviewed by Founder Studio

A real (lightly trimmed) run of the specialist agents on the idea *"Founder Studio"* itself. It's the
honest test: if the studio can't survive its own critique, it shouldn't ship. Spoiler — the critique
returned **MAJOR REWORK**, and that feedback shaped this repo's README.

> This is illustrative output. Numbers from the market agent are its estimates with sources; treat them
> as a starting point, not gospel.

---

## Market snapshot (`/market-research`)

**Market:** tooling for technical solo founders / indie hackers who already use Claude Code and want to
pressure-test and plan an idea — a plugin competing for the "validate + plan my idea" job, not a
standalone SaaS.

**The honest read:** this is a *real but small, fast-growing, already-contested* niche. Direct
open-source competitors already exist inside the ecosystem:

- `idea-validation-agents` — ~329★, MIT, venture-analyst agents (nearly the same product).
- `the-startup` — ~297★, MIT, build-focused agent roles (leaves validation/critique as a gap).
- Mega agent marketplaces (tens of thousands of stars) could fold a "founder pack" in for free.

Standalone web validators (ValidatorAI, IdeaProof, DimeADozen) anchor willingness-to-pay at **~$0–$50/mo**
with a steep free→paid cliff.

**Confidence: LOW** on absolute sizing (no public install counts), **MEDIUM** on the relative read.
**Biggest unknown:** how many Claude Code users are *aspiring founders who'd actually invoke a planning
agent* vs. only code. The cheapest way to find out: ship the OSS command and measure real usage against
the ~300-star benchmark before building anything paid.

---

## The critique (`/critique`) — verdict: **MAJOR REWORK**

> The product is buildable in a weekend and the wedge is real, but the plan rests on a success metric
> (GitHub stars) that measures nothing the business needs, and the "brutal critique" differentiator is
> trivial for a competitor — or the platform vendor — to copy.

**Fatal flaws (worst-first):**

1. **Vanity metric.** Stars and installs measure curiosity, not value. The thing that matters — *did
   anyone use the output to make a real go/no-go decision?* — isn't tracked anywhere.
2. **The wedge is just a prompt.** An "adversarial critic agent" is one markdown file with a stern system
   prompt. No moat; copyable in an afternoon.
3. **Artifact, not action.** The cure for building-the-wrong-thing is talking to real humans. The product
   ships *a better document* — which can make founders feel "validated" and ship to silence.

**Cheapest next test:** don't build the 10-agent orchestra first. Wire up `/critique` + `/founder`, hand
it to 5 real founders with a live idea, and measure one thing: within two weeks, did the output cause a
*concrete real-world action* (kill, pivot, a customer email, a line of code)? If fewer than 3 of 5 act,
the artifact-not-action flaw is fatal and no amount of agents fixes it.

*Credit where due: the `/critique`-as-gate instinct is the genuinely good idea — just point it at the
business, not only the user's plan.*

---

## Validation plan (`/validate`)

**Riskiest assumption:** founders will *trust an AI-generated critique enough to change what they do
next* — and the output is good enough that they come back. (Not "will people install a free tool" — that's
cheap and proves nothing.)

**Cheapest experiment:** a concierge MVP. Run 5 founders' real ideas through the agents by hand, deliver
the doc, then watch whether they take a concrete action within 7 days.

**Pass bar:** ≥3 of 5 take a concrete action from the doc, and ≥1 says the critique changed their
decision.

---

## How the critique changed the product

The README you're reading reflects the teardown: it leads with honesty over hype, states plainly that the
studio **plans** validation but doesn't replace talking to customers, and frames stars as vanity — the
real signal is whether the output changes what a founder does next.
