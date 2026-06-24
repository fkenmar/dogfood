---
description: Design a demand-validation plan for a startup idea — riskiest assumption, customer interviews, and the cheapest pre-build test
argument-hint: "<path to project doc, or describe the idea>"
allowed-tools: Task, Read, Glob, Grep, WebSearch, WebFetch
---
Design a validation plan for: $ARGUMENTS

If that's a path, read it. Dispatch the `customer-discovery` subagent on the idea — pass it the full doc
or description — and return its plan: the riskiest assumption, who to talk to and where to find them, the
Mom-Test interview script, and the cheapest pre-build experiment with a pass/fail bar.
