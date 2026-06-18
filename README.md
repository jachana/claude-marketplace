# jachana's Claude Code skills

A single **marketplace** for all my [Claude Code](https://docs.claude.com/en/docs/claude-code) skills. Add it once, install any skill by name, and they update themselves whenever I ship a new version.

> 🌍 Most skills are bilingual — they work in **English and Spanish** and reply in whichever you write in.

## Quick start

```bash
# 1. add this marketplace (once)
/plugin marketplace add jachana/claude-marketplace

# 2. install any skill by name (see the list below)
/plugin install ship@jachana
```

**Auto-update:** open `/plugin` → **Marketplaces** → turn on *Enable auto-update* for `jachana`. After that, new versions arrive on their own.

---

## The skills

### 🧠 Second brain — Obsidian vault
| Install | What it does |
|---|---|
| `brain-init@jachana` | Register a repo with your central Obsidian vault and scaffold the `.brain/` bridge. |
| `brain-sync@jachana` | Work inside a `.brain/` repo: read tasks/context down, write status/log/answers back up. |
| `brain-connect@jachana` | Surface reuse across projects — what you built in one is useful in another. |
| `brain-report@jachana` | A progress report across every project in the vault. |

### 📋 Project boards — works offline (local), or on Trello / Jira
| Install | What it does |
|---|---|
| `ship@jachana` | Take the top card all the way to shipped: build, test, commit, move to review. |
| `triage@jachana` | Sort an incoming pile: route, prioritize, size, dedupe, flag dependencies. |
| `breakdown@jachana` | Split a big or vague card into small, shippable subtasks with acceptance criteria. |
| `refine@jachana` | Groom a backlog: enrich thin cards, estimate, order by priority, flag blocked/duplicate. |
| `prune@jachana` | Clear dead weight: duplicates, stale cards, done items, zombies. |
| `dependency-graph@jachana` | See what blocks what — Mermaid diagram + tree + cycle detection. |

### 🚀 DevOps — Coolify PaaS
| Install | What it does |
|---|---|
| `coolify@jachana` | Manage a self-hosted Coolify over its API (apps, DBs, services, env vars). Dry-run by default. |
| `coolify-deploy@jachana` | Trigger a deploy and validate it — never reports success on a red build. |
| `coolify-audit@jachana` | Read-only audit: resource inventory, secret hygiene, exposed ports. |

### 📝 Reporting & writing
| Install | What it does |
|---|---|
| `human-readable-report@jachana` | Write a report people actually read — status, summary, analysis, or briefing. |
| `proposal-writer@jachana` | Draft a client proposal or quote, grounded in your real project context. |

### ✉️ Email
| Install | What it does |
|---|---|
| `email-assistant@jachana` | Draft replies grounded in your second-brain; keep long threads coherent. |

### ✅ Quality
| Install | What it does |
|---|---|
| `prove-it-validation@jachana` | Verify a change actually works and show the evidence before calling it done. |

### 🛠️ Dev workflow
| Install | What it does |
|---|---|
| `issue-fix-workflow@jachana` | Drive one GitHub issue to a tested PR with before/after evidence; auto-detects your repo's conventions on first run. |
| `game-improvement-analysis@jachana` | Analyze a game's code and produce a ranked, prioritized improvement report. |

---

## How it works

Each skill lives in its **own** `skill-<name>` repo under [github.com/jachana](https://github.com/jachana?tab=repositories&q=skill-). This repo is just the **catalog** ([`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json)) that points Claude Code at them. Updating a skill is a push to its repo — with auto-update on, you get it next session.

| Task | Command |
|---|---|
| Update one skill now | `/plugin update <name>@jachana` |
| List what's installed | `/plugin list` |
| Remove this marketplace | `/plugin marketplace remove jachana` |
