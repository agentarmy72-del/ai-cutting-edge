# Public Skills

This folder is for reusable agent procedures derived from AI Cutting Edge material.

## Qualification gate

A public skill must have:

1. a recurring task and clear trigger boundary;
2. explicit inputs and prerequisites;
3. complete executable steps rather than advice alone;
4. failure and safety behavior;
5. a real verification path or test;
6. public provenance, evidence limitations, licence status, and review date.

Expected layout:

```text
library/skills/<skill-name>/
  SKILL.md
  references/   # only when needed
  scripts/      # only when executable support is required
```

## Current status

No creator-derived procedure has passed this gate yet. The current [CLI-first agent tooling](../../creators/guides/cli-first-agent-tools.md) material remains a practical guide because its broader efficiency claims have not been established by a matched benchmark or a published runnable implementation.

This restraint is intentional: a useful guide is better than an untested skill presented as operational truth.
