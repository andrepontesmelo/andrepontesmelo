I build the **DSH productivity suite** — plugins and agent skills for the [DeepSeek Harness](https://www.npmjs.com/package/@deepseek-ai/dsh) (DSH), an agentic coding harness. Everything here follows one rule: *the shortest working diff wins*.

## The suite

**One command installs it all:**

```bash
dsh plugin --profile <profile> add github:andrepontesmelo/dsh-suite
```

That single command installs the bundle, pulls both plugin dependencies (`dsh-model-router`, `deep-horizon`), and points DSH skill discovery at the nine bundled skills.

| Repo | Type | What it does |
|---|---|---|
| [`dsh-suite`](https://github.com/andrepontesmelo/dsh-suite) | bundle | The entrypoint: 9 agent skills + 2 plugins, installable in one command |
| [`dsh-model-router`](https://github.com/andrepontesmelo/dsh-model-router) | plugin | Virtual model ids routed over real provider/model candidates — priority failover with exponential backoff, round-robin rotation, sleep windows |
| [`deep-horizon`](https://github.com/andrepontesmelo/deep-horizon) | plugin + CLI | Keeps a project's aim — one about line, up to 5 gaps — in front of every agent session, via per-harness adapters over one shared `.horizon` store |
| [`archloop`](https://github.com/andrepontesmelo/archloop) | standalone | Overnight architecture-improvement loop driver — auto-scan + refactor cycle for git repos |
| [`hkrc`](https://github.com/andrepontesmelo/hkrc) | standalone | Hermes Kanban Recovery Controller — portable, instance-scoped blocker recovery |

Also public, kept out of the bundle: [`moving-target`](https://github.com/andrepontesmelo/moving-target) (plugin, **deprecated** — superseded by deep-horizon), and two forks carrying local features — [`dsh-telegram-channel`](https://github.com/andrepontesmelo/dsh-telegram-channel) (Telegram mobile remote: `/new`, gesture passthrough) and [`deepseek-harness-mobile`](https://github.com/andrepontesmelo/deepseek-harness-mobile) (Android companion). Legacy: `publications` (2016, archived).

## How I work

- Vertical slices, sequential implementers, mandatory review loops (`strong-orchestrator`)
- Lazy-senior-dev output style: delete over add, boring over clever (`ponytail` family)
- Every published repo passes the same gate: README review · tests green · secrets scan · MIT

## Elsewhere

- Forgejo (self-hosted): full development history before public export
