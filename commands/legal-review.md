---
description: Early-stage startup legal & compliance check — entity, equity/IP, terms & privacy, regulatory exposure, contracts (issue-spotting, not legal advice)
argument-hint: "<path to project doc, or describe the startup>"
allowed-tools: Task, Read, Glob, Grep, WebSearch, WebFetch
---
Run a legal & compliance review for: $ARGUMENTS

If that's a path, read it. Dispatch the `startup-lawyer` subagent on the project — pass it the full doc
or description — and return its review. It spots issues and flags what needs a licensed attorney; it is
not a substitute for one.

If the idea is too vague to assess (no clear product, users, or data), point me at `/founder` first.
