I build the **DSH productivity suite** — plugins and agent skills for the [DeepSeek Harness](https://www.npmjs.com/package/@deepseek-ai/dsh) (DSH), an agentic coding harness. Everything here follows one rule: *the shortest working diff wins*.

## The suite

**One command installs it all:**

```bash
dsh plugin --profile <profile> add github:andrepontesmelo/dsh-suite
```

That single command installs the bundle, pulls both plugin dependencies (`dsh-model-router`, `moving-target`), and points DSH skill discovery at the nine bundled skills.

| Repo | Type | What it does |
|---|---|---|
| [`dsh-suite`](https://github.com/andrepontesmelo/dsh-suite) | bundle | The entrypoint: 9 agent skills + 2 plugins, installable in one command |
| [`dsh-model-router`](https://github.com/andrepontesmelo/dsh-model-router) | plugin | Virtual model ids routed over real provider/model candidates — priority failover with exponential backoff, round-robin rotation, sleep windows |
| [`moving-target`](https://github.com/andrepontesmelo/moving-target) | plugin | Cold-start context — distills your first prompts into one goal paragraph, injected into every new session |
| [`archloop`](https://github.com/andrepontesmelo/archloop) | standalone | Overnight architecture-improvement loop driver — auto-scan + refactor cycle for git repos |
| [`hkrc`](https://github.com/andrepontesmelo/hkrc) | standalone | Hermes Kanban Recovery Controller — portable, instance-scoped blocker recovery |

## How I work

- Vertical slices, sequential implementers, mandatory review loops (`strong-orchestrator`)
- Lazy-senior-dev output style: delete over add, boring over clever (`ponytail` family)
- Every published repo passes the same gate: README review · tests green · secrets scan · MIT

## Elsewhere

- Forgejo (self-hosted): full development history before public export
