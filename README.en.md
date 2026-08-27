# OpenClaw Task Progress Tracker 🗂️

> Manage tasks/ and projects/ directories with PROGRESS.md cards — directory as container, PROGRESS.md as progress.

<p align="center">
  <img src="./assets/readme/hero.svg" width="100%" alt="OpenClaw Task Progress Tracker — manage tasks/ and projects/ directories with PROGRESS.md cards: status, append-only progress log, and document index">
</p>

> Lightweight progress cards for your workspace tasks/ and projects/ directories.
> Pure files, zero dependencies, no CLI. Status + progress log + document index in one place — every task's progress is traceable, every document findable.

![license](https://img.shields.io/badge/license-MIT-green)
- 📚 **xiaoyaoclaw-kb-retriever** (knowledge base retriever): local KB retrieval — hierarchical data_structure.md index navigation + progressive retrieval over md/pdf/xlsx, zero dependencies, Windows & macOS ready. <https://github.com/dtsola/xiaoyaoclaw-kb-retriever>
[![ClawHub downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fclawhub.ai%2Fapi%2Fv1%2Fskills%2Fxiaoyaoclaw-task-progress-tracker&query=skill.stats.downloads&label=ClawHub%20downloads&color=blue)](https://clawhub.ai/dtsola/skills/xiaoyaoclaw-task-progress-tracker)

## Why you need it

Every AI agent session starts fresh. Without progress tracking, your work will:
- ❌ **Lost context** — tasks half-done across sessions, no way to resume
- ❌ **Scattered documents** — reports and docs buried in random folders, impossible to find later
- ❌ **No traceability** — "what did I do on this task last week?" — gone
- ❌ **Heavy tools** — full project-management suites (CLI + external services) are overkill for a file-based workflow

This skill solves it in one go: **directory as container + PROGRESS.md progress card + document index**.

## Features

- 📁 **Two objects** — tasks (30 min ~ 1 week, short-lived) and projects (> 1 week, continuously maintained)
- 🗂️ **Directory as container** — `tasks/<slug>/`, `projects/<slug>/` are the task/project themselves, no parallel structure
- 📋 **PROGRESS.md progress card** — frontmatter (status / progress / docs) + append-only progress log + document index
- 🔗 **Document index** — machine-readable (YAML `docs` array) + human-readable (index table) dual channel
- 🚦 **Restrained creation** — only responds to explicit instructions, no global skill hooks (lesson learned from v1)
- 🪶 **Zero dependency** — pure file operations, no CLI, no external services, no database
- 🏠 **Sister-skill synergy** — pairs with workspace-initializer (directory rules) and memory-distill (memory distillation)

## Install

```bash
# From ClawHub (recommended)
clawhub install xiaoyaoclaw-task-progress-tracker

# Or manually from GitHub
git clone https://github.com/dtsola/xiaoyaoclaw-task-progress-tracker
# Put SKILL.md and templates/ into your skills directory
```

## Usage

Tell your agent in plain language:

| You say | What happens |
|---------|-------------|
| "Start a task: research XX" | Creates `tasks/xx/` + PROGRESS.md card |
| "Create a project: XX platform" | Creates `projects/xx/` + PROGRESS.md card |
| "Task XX progress: research done, writing report" | Appends progress log + updates timestamp |
| "Attach a doc to XX: outputs/xxx.png is the result" | Moves doc into `docs/` + writes index |
| "What tasks/projects are running?" | Summarizes all active cards |
| "Where is XX project now?" | Reads the PROGRESS.md and reports |
| "Task XX is done" | Marks done + logs to today's memory file |

## 🚀 Quick Start

### Step 1: Install the skill

```bash
clawhub install xiaoyaoclaw-task-progress-tracker
```

### Step 2: Create your first task

Tell your agent:

> start a task: research XX

It will create `tasks/xx/PROGRESS.md` with status active.

### Step 3: Maintain daily

Say a progress update, attach a doc — the agent keeps the card updated. Open any PROGRESS.md to see status, timeline, and document index at a glance.

## How it compares

| | v1 (deprecated) | **v2 (this)** |
|---|---|---|
| Status carrier | PROGRESS.md (dual-track: status layer × content layer) | ✅ PROGRESS.md as the only card (status + log + index in one) |
| Creation trigger | any skill activation = create entry (false positives) | ✅ explicit user instruction / clear expectation only |
| Documents | not managed | ✅ docs/ index (cairn artifact idea, no CLI) |
| Dependencies | none | ✅ none (stays lightweight) |

## Directory structure

```
xiaoyaoclaw-task-progress-tracker/
├── SKILL.md                    # the skill itself (intent table + operations + boundaries)
├── templates/
│   ├── task-card.md            # task PROGRESS.md template
│   └── project-card.md         # project PROGRESS.md template
├── assets/readme/              # hero + community QR
├── DESIGN.md                   # design document
├── USER_GUIDE.md               # user guide (from the user's perspective)
├── README.md
└── LICENSE
```

## License

MIT — use it freely, attribution optional.

---

## 🛠️ Need customization?

**Agent & Skills customization, from ¥800 (≈$110).**

- WeChat: `dtsola` (note: **openclaw custom**)
- Services: OpenClaw multi-agent deployment / workspace standardization / custom Skill development / agent memory system setup

## Sister projects

- 🏠 **xiaoyaoclaw-workspace-initializer** (workspace initializer): gives every agent a "home" — standard directory structure + WORKSPACE.md rules + multi-agent config safety. <https://github.com/dtsola/xiaoyaoclaw-workspace-initializer>
- 🧠 **xiaoyaoclaw-memory-distill** (memory distill): turns conversations into structured memory. <https://github.com/dtsola/xiaoyaoclaw-memory-distill>

## 小遥Claw (XiaoyaoClaw)

**Put an AI assistant in your own computer.**

- 🚀 Landing page: <https://www.yuque.com/dtsola/igp1aa/adcicbai2zlem0bz>
- 📖 Intro repo: <https://github.com/dtsola/xiaoyaoclaw-introduction>

## About the author

- 🌐 Blog: <https://www.dtsola.com>
- 📺 Bilibili: <https://space.bilibili.com/736015>
- 💻 GitHub: <https://github.com/dtsola>
- 📕 Xiaohongshu: <https://www.xiaohongshu.com/user/profile/5b4c0597e8ac2b06aa13346d>

## 💬 Join the community

Xiaoyao product family user group — feedback · usage · feature requests:

<p align="center">
  <img src="./assets/readme/community-qr.png" width="280" alt="Xiaoyao AI user group QR code: scan to join, or add WeChat dtsola (note: join group)">
</p>

<p align="center">Scan to join, or add WeChat <code>dtsola</code> (note: <b>join group</b>)</p>
