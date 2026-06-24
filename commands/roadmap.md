---
description: Turn a project doc or plan into a sequenced, acceptance-checked execution roadmap (riskiest-assumption-first)
argument-hint: "<path to project doc, or describe the project & its plan>"
allowed-tools: Task, Read, Glob, Grep
---
Build an execution roadmap for: $ARGUMENTS

If that's a path, read it. Dispatch the `project-manager` subagent on the project — pass it the full doc
or plan — and return its roadmap.

If there's no plan to work from yet (just a raw idea), don't guess a roadmap — point me at `/founder`
first to produce the project doc, then come back here.
