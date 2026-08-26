<div align="center">

# 🗂️ OpenClaw Task Progress Tracker（任务进度跟踪器）

**管理工作区 tasks/ 与 projects/ 目录的轻量进度卡系统——目录即容器，PROGRESS.md 即进度。**

纯文件、零依赖、无 CLI。状态 + 进度日志 + 文档索引一体，让每个任务/项目的进度可回溯、文档找得回。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-ready-4b3baf)](https://openclaw.ai)
[![ClawHub](https://img.shields.io/badge/ClawHub-xiaoyaoclaw--task--progress--tracker-blue)](https://clawhub.ai)

</div>

---

## 为什么需要它

AI agent 每次会话都是全新开始。任务做到一半、文档散落各处、下次会话想不起来——进度管理是刚需。

**这个 skill 解决三件事：**
1. **进度记录**：每个任务/项目一份 PROGRESS.md，进度日志按时间追加，像 changelog，随时回溯
2. **文档索引**：干活中天然生成的文档收进 `docs/`，卡片里挂索引，不怕忘
3. **会话恢复**：新会话扫一眼卡片 frontmatter，全貌即知

## 特性

- ✅ **双对象**：tasks（半小时~一周短期任务）+ projects（>一周时刻维护的长期项目）
- ✅ **目录即容器**：`tasks/<slug>/`、`projects/<slug>/` 本身就是任务/项目，不另起炉灶
- ✅ **PROGRESS.md 进度卡**：frontmatter（status/progress/docs）+ 进度日志 + 文档索引
- ✅ **文档索引**：机器可读（YAML docs 数组）+ 人可读（索引表格）双通道
- ✅ **建项克制**：只响应明确指令，不做全局技能钩子（吸取 v1 教训）
- ✅ **零依赖**：纯文件操作，无 CLI、无外部服务、无数据库
- ✅ **三件套协同**：与 workspace-initializer（目录规范）、memory-distill（记忆蒸馏）无缝衔接

## 安装

```bash
# ClawHub
openclaw skills install @dtsola/xiaoyaoclaw-task-progress-tracker

# 或手动：将项目目录复制到你的 skills 目录
# 或 npx clawhub install xiaoyaoclaw-task-progress-tracker
```

## 使用（用户视角，自然语言即可）

| 你想干嘛 | 直接说 |
|---------|--------|
| 开任务 | 「开个任务：调研 XX」 |
| 建项目 | 「建个项目：XX 平台」 |
| 更新进度 | 「任务 XX 进度：资料收集完了，开始写报告」 |
| 挂文档 | 「任务 XX 挂个文档：outputs/xxx.png 是效果图」 |
| 盘点 | 「现在有哪些任务/项目在跑？」 |
| 查进度 | 「XX 项目现在到哪了？」 |
| 完结 | 「任务 XX 完了」 |

详细场景见 [USER_GUIDE.md](USER_GUIDE.md)。

## 🚀 快速上手

1. **安装**：`openclaw skills install @dtsola/xiaoyaoclaw-task-progress-tracker`
2. **建第一个任务**：对 agent 说「开个任务：xxx」→ 自动生成 `tasks/xxx/PROGRESS.md`
3. **日常维护**：干活时说一句进度、挂个文档，其余交给 agent

## 目录结构

```
tasks/<slug>/            # 短期任务（半小时~一周）
└── PROGRESS.md          # 进度卡：状态 + 进度日志 + 文档索引
projects/<slug>/         # 长期项目（>一周，时刻维护）
├── PROGRESS.md          # 进度卡（含 progress 百分比）
└── docs/                # 项目文档（可选）
```

卡片格式见 [templates/](templates/)。

## 姊妹项目

| 项目 | 定位 |
|------|------|
| [xiaoyaoclaw-workspace-initializer](https://github.com/dtsola/xiaoyaoclaw-workspace-initializer) | 工作区目录规范（家） |
| **xiaoyaoclaw-task-progress-tracker**（本仓库） | 任务/项目进度管理（状态） |
| [xiaoyaoclaw-memory-distill](https://github.com/dtsola/xiaoyaoclaw-memory-distill) | 记忆蒸馏（内容） |

## License

[MIT](LICENSE) © 2026 dtsola

---

<p align="center">
  <a href="https://www.yuque.com/dtsola/igp1aa/adcicbai2zlem0bz">🚀 小遥Claw：把 AI 助手装进自己的电脑</a>
</p>
