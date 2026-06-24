# Example: dogfood, run on itself

A real run of the full `/founder` pipeline on the idea of **dogfood** itself — the honest test. The
critique came back **MAJOR REWORK**; that feedback shaped the README and this repo. Output is lightly
trimmed for length. Market and financial numbers are the agents' estimates with sources — starting
points, not gospel.

> *Disclaimer: AI-generated. The legal and financial sections below are not professional advice.*

---

## Verdict — MAJOR REWORK

> Buildable in a weekend and the wedge is real, but the original plan rested on a success metric (GitHub
> stars) that measures nothing the project needs, and the "brutal critique" differentiator is the easiest
> thing on earth for a competitor — or the platform vendor — to copy.

---

## 1. One-liner
An open-source Claude Code plugin that runs your startup idea through a team of AI agents — including a
cold critic that can tell you to kill it — and hands back a validated, execution-ready project doc.

## 2. Problem
Founders waste months building things nobody wants, and the AI tools meant to help make it worse: they're
flattering hype machines that tell every idea it's brilliant. Sycophancy is most dangerous exactly when
you're attached to an idea. A painkiller for the founder who is *about* to sink a weekend (or a quarter)
into an unvalidated idea.

## 3. Target user
Indie hackers, solo and technical founders, and Claude Code power users who already live in the terminal
and want to pressure-test an idea fast. The narrow first 100: Claude Code users active in founder/maker
communities who post "is this worth building?" today.

## 4. Solution & wedge
The wedge is the **critique-as-gate**: a plan must survive a cold, adversarial critic (fresh context, no
stake in the draft) before it ships, and the critique log shows how it changed. **Not built yet:** a
hosted version, accounts, telemetry, or a paid tier.

## 5. Why now
Subagents and plugins in Claude Code only became generally usable in late 2025 — orchestrating ten
specialist roles, each with its own context and tools, went from a real engineering project to a folder
of markdown files plus a one-command marketplace install.

## 6. Market *(Confidence: LOW on absolute size, MEDIUM on the relative read)*
A real but small, fast-growing, already-contested niche: tooling for the slice of Claude Code users who
are also aspiring founders. Direct open-source competitors already exist — `idea-validation-agents`
(~329★) is nearly the same product; `the-startup` (~297★) is build-focused and leaves critique as a gap.
Standalone web validators anchor willingness-to-pay at **~$0–$50/mo** with a steep free→paid cliff. The
honest opportunity here is **distribution and reputation, not direct revenue**.

## 7. Competition & why you win
- **Direct (inside Claude Code, free, MIT):** `idea-validation-agents`, `the-startup`, mega
  agent-marketplaces that could fold a "founder pack" in for free.
- **Indirect:** web validators (ValidatorAI, IdeaProof) — hosted, not in-terminal, and they cheer.
- **Status quo / do-nothing:** prompting raw ChatGPT/Claude. Free, and the real bar to beat.
- **Why dogfood:** the adversarial critique-as-gate, the verdict, and a visible critique log — the
  willingness to say *KILL IT*. That's a positioning edge (taste + trust), **not a technical moat.**

## 8. Business model
Free, MIT, $0-cost to operate — **default-alive from day one** (public-repo hosting, the user's own
compute). A hosted "pro" tier is only viable if it sells something a forked plugin structurally can't:
managed infra or licensed data — not "more markdown." The decisive unknown is free→paid conversion among
a pay-resistant audience; test it with a fake-door waitlist before building any infrastructure. *(Not
financial advice; figures are estimates.)*

## 9. Go-to-market
Win the **Claude Code power-user community first** (Anthropic Discord, r/ClaudeAI, `awesome-claude-*`
lists) where install friction is ~zero, then a public wave: Show HN + Product Hunt + r/SideProject.
The **growth loop is the verdict artifact** — a `KILL IT` with receipts is screenshot-bait that carries
the repo link. First 10 users: people you know who run Claude Code, by hand.

## 10. MVP & milestones
Smallest thing that proves the point: `/founder` + `/critique` + 3–4 core agents (the full roster already
exists but isn't the MVP). Milestones gate on validation, not features: M0 core runs clean on a fresh
install → M1 five founders recruited → M2 docs delivered → **M3 validation verdict (the existence gate)**
→ M4 community seed → M5 public launch.

## 11. Validation & the one metric
**The one metric: did the output change what the founder did next** — not stars, not installs. Cheapest
test (run before building more): concierge — run 5 real founders' live ideas through the core by hand and
measure whether **≥3 take a concrete action within 7 days**, with **≥1** saying the critique changed their
decision.

## 12. Risks that kill it
- 🔴 **Artifact ≠ action.** A polished doc can make founders feel validated and ship to silence. Mitigation:
  the success metric is behavioral; the validation plan pushes them to real customers.
- 🔴 **No moat.** The wedge is a prompt; a clone or the platform vendor can copy it. Mitigation: accept it —
  compete on taste, trust, and being the honest one; it's a portfolio/community play, not a defensible business.
- 🟡 **Token/context cost** of ~10 subagents per run. Mitigation: cap section lengths, route factual
  sections to cheaper models, measure before expanding the roster.
- 🟡 **No top-level disclaimer** for AI legal/financial output *(fixed — added `DISCLAIMER.md` + agent disclaimers)*.
- 🟡 **Platform dependency** on Claude Code. Mitigation: plain-markdown files, so a break is a quick edit.

## 13. 90-day plan (next 3 moves)
1. Recruit 5 founders with a *live* idea (the bottleneck — start day one).
2. Run the core on your own idea on a fresh install; clock token cost and confirm the loop terminates.
3. Concierge-test the 5; score against the pass bar before building or launching anything wider.

## 14. Critique log
| Round | Verdict | Flaw flagged | How the plan changed |
|---|---|---|---|
| 1 | MAJOR REWORK | Vanity metric (stars) | Success metric reframed to "did the output change behavior" |
| 1 | MAJOR REWORK | Wedge is just a prompt | Repositioned as an OSS / portfolio + community play, no claimed moat |
| 1 | MAJOR REWORK | Artifact ≠ talking to customers | README + product now state plainly that it plans validation, doesn't replace it |

---

## Appendix — specialist deep-dives (condensed)

- **Technical:** shippable today; markdown command + agent files, no backend. Real risks: subagent
  context/token cost, portability (use relative paths / `${CLAUDE_PLUGIN_ROOT}`), platform dependency.
  Keep orchestration flat — only `/founder` dispatches.
- **UX:** it's a CLI + document product. Verdict-first (terminal and doc), visible phase progress, a
  short-circuit `KILL IT` path, and a copy-pasteable shareable verdict block. Every section opens with a
  one-line bottom line; confidence tags on every market number.
- **Legal *(issue-spotting, not legal advice)*:** MIT is fine for the code; the real exposure was missing
  disclaimers on AI legal/financial output — now added. Name "dogfood" is brandable but check for
  conflicts before investing in it.
- **Execution roadmap:** riskiest-assumption-first — the concierge validation test runs on the existing
  core *before* any further building, launch, or paid surface. Build nothing new until ≥3 of 5 founders act.
- **Launch narrative:** lead with the contrarian hook ("honest enough to tell you to kill your idea"),
  prove it with the self-run, and ask for one thing over a star — *did the output change what you did next?*
  Honest answer on raising money: **no** — it's a portfolio + community project, not a venture business.
