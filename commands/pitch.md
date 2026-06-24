---
description: An investor pitch — fundraising narrative and a slide-by-slide deck outline, plus the ask and the toughest questions
argument-hint: "<path to project doc, or describe the startup>"
allowed-tools: Task, Read, Glob, Grep, WebSearch, WebFetch
---
Build an investor pitch for: $ARGUMENTS

If that's a path, read it. Dispatch the `pitch-strategist` subagent on the project — pass it the full doc
or description — and return the narrative, the slide-by-slide deck outline, the ask, and the toughest
investor questions with answers.

If there's no plan to pitch from yet (just a raw idea), point me at `/founder` first.
