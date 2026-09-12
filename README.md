Software Engineer — Applied AI & LLM Infrastructure. 14 years of production systems (ex-AWS S3), building agent tooling in public: the DSH plugin suite, model routing, autonomous orchestration. Insurance software background (Segfy, Cotak). One rule underneath everything: *the shortest working diff wins*.

## The suite

**One command installs it all:**

```bash
dsh plugin --profile <profile> add github:andrepontesmelo/dsh-suite
```

That single command installs the bundle, pulls both plugin dependencies (`@andrepontesmelo/dsh-model-router`, `deep-horizon`), and points DSH skill discovery at the nine bundled skills.

| Repo | Type | What it does |
|---|---|---|
| [`dsh-suite`](https://github.com/andrepontesmelo/dsh-suite) | bundle | The entrypoint: 9 agent skills + 2 plugins, installable in one command |
| [`dsh-model-router`](https://github.com/andrepontesmelo/dsh-model-router) | plugin | Virtual model ids routed over real provider/model candidates — priority failover with exponential backoff, round-robin rotation, sleep windows |
| [`deep-horizon`](https://github.com/andrepontesmelo/deep-horizon) | plugin + CLI | Keeps a project's aim — one about line, up to 5 gaps — in front of every agent session, via per-harness adapters over one shared `.horizon` store |
| [`dsh-wayfinder-ui`](https://github.com/andrepontesmelo/dsh-wayfinder-ui) | plugin | Spawns one live session per ready Wayfinder task and renders the dependency map in the DSH chat GUI |
| [`archloop`](https://github.com/andrepontesmelo/archloop) | standalone | Overnight architecture-improvement loop driver — auto-scan + refactor cycle for git repos |
| [`hkrc`](https://github.com/andrepontesmelo/hkrc) | standalone | Hermes Kanban Recovery Controller — portable, instance-scoped blocker recovery |

Also public, kept out of the bundle: [`moving-target`](https://github.com/andrepontesmelo/moving-target) (plugin, **deprecated** — superseded by deep-horizon), and two forks carrying local features — [`dsh-telegram-channel`](https://github.com/andrepontesmelo/dsh-telegram-channel) (Telegram mobile remote: `/new`, gesture passthrough) and [`deepseek-harness-mobile`](https://github.com/andrepontesmelo/deepseek-harness-mobile) (Android companion). Legacy: `publications` (2016, archived).

## How I work

I design agent orchestration and self-improvement loops that keep code clean, scalable, and maintainable in the AI era — context and memory management, multi-agent workflows, intelligent model routing — built and tested in public here, and run daily in my own workspace.
