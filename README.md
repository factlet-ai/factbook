# factlet-ai/factbook

The operational Factbook for the **factlet-ai** project itself — eaten as dogfood under the open [Factlet Protocol](https://github.com/factlet-ai/spec).

This is **not** an example factbook. It's the real, live factbook that a session touching `factlet-ai/*` repos or `factlet.ai` content should consume before making changes.

## What's in here

`factbook.yaml` — facts about:
- Deploy mechanics (Cloudflare Pages, GitHub integration, wrangler)
- Public eval suite at [factlet-ai/evals](https://github.com/factlet-ai/evals)
- Factbook scoping discipline (per Factlet Protocol v0.2 / RFC-001)
- Relationship to Kernora as the reference implementation

## Why a separate repo (vs. co-locating in kernora-ai/kernora)

The original draft of this factbook was created inside `github.com/kernora-ai/kernora/.nora/factlet-factbook.yaml` — wrong location. Co-locating two project-scoped factbooks (`project:kernora` and `project:factlet-ai`) in the same git repo creates real LLM cross-contamination risk: facts from the wrong project leak into context, IDs collide (`f001` exists in both), and citations become ambiguous.

Per `factlet-ai:f002` in this factbook, **factbooks for distinct projects MUST live in physically separate repos**. This repo is the home for `project:factlet-ai` facts. The Kernora project keeps its own factbook in its own repo, scoped `project:kernora`.

## Scope

```
scope: project:factlet-ai
```

External references to facts in this factbook MUST use the `<scope>:<id>` form: `factlet-ai:f001`, not bare `f001` (per RFC-001 in the [spec repo](https://github.com/factlet-ai/spec/tree/main/rfcs)).

## License

MIT — see [LICENSE](LICENSE).
