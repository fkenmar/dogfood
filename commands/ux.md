---
description: A product designer's UX plan — core user flows, key screens & states, UX principles, and v1 design scope
argument-hint: "<path to project doc, or describe the product>"
allowed-tools: Task, Read, Glob, Grep, WebSearch, WebFetch
---
Design the UX for: $ARGUMENTS

If that's a path, read it. Dispatch the `product-designer` subagent on the product — pass it the full doc
or description — and return its plan: the core user flows, key screens and states, UX principles, and the
v1 design scope. When it's time to build the actual frontend, hand off to your frontend tooling (e.g. a
frontend-design skill, or your usual stack).
