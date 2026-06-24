---
description: Evidence-backed market research for a startup idea — size, competitors, willingness to pay, and "why now" signals
argument-hint: "<startup idea or market to research>"
allowed-tools: Task, WebSearch, WebFetch, Read
---
Research the market for: $ARGUMENTS

Dispatch the `market-researcher` subagent on this idea and return its brief. If the idea is too vague to
research a specific market — no clear buyer or use case — ask me the one question that would narrow it
before dispatching.

After the brief, add one line: the single market fact that, if false, would most change whether this is
worth building.
