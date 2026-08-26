---
type: project
status: active
progress: 90
created: 2026-08-26
updated: 2026-08-26
docs:
  - path: DESIGN.md
    desc: 设计文档（数据模型 + 三条红线 + 三件套协同）
  - path: USER_GUIDE.md
    desc: 用户使用指南（站在使用者角度）
  - path: SKILL.md
    desc: 技能主体（意图识别 + 操作手册 + 边界）
  - path: README.md
    desc: 项目 README（发布用）
---

# xiaoyaoclaw-task-progress-tracker v2

## 目标 / 背景

重启同名项目（v1 因双轨制 + 全局钩子误报废弃）。v2 定位：管理 tasks/projects 目录生命周期的轻量进度卡系统——目录即容器，PROGRESS.md 即进度（状态 + 进度日志 + 文档索引），与 initializer + memory-distill 组成三件套。

## 当前状态

已发布：GitHub（main + MIT + topics×7 + 双语描述）✅ + ClawHub v1.0.0 已提交（pending-publication 待安全扫描公开）。实测通过（task + project 双卡片全链路）。

## 进度日志

- 2026-08-26 11:36：调研交付，指挥官拍板自研方案
- 2026-08-26 18:22：设计确认（PROGRESS.md 命名 + 用户视角指南）
- 2026-08-26 18:37：模板 / SKILL.md / README / LICENSE / 全局技能同步完成，开始实测
- 2026-08-26 18:45：实测通过（task + project 双卡片：立项→进度→挂文档→完结→日志）
- 2026-08-26 18:50：发布完成——GitHub 仓库 + push（直连成功，代理 22307 挂）+ topics（gh CLI，API PUT 422 异常）+ ClawHub v1.0.0 提交

## 文档索引

| 文档 | 说明 | 更新 |
|------|------|------|
| DESIGN.md | 设计文档 | 2026-08-26 |
| USER_GUIDE.md | 用户使用指南 | 2026-08-26 |
| SKILL.md | 技能主体 | 2026-08-26 |
| README.md | 项目说明 | 2026-08-26 |

