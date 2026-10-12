# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

### 变更

- `journal/default/`：183 篇日志（2026-03-11 ~ 2026-09-19）整体迁出至 `quanttide-journal-of-founder` 的 `default/<YYYY-MM>/`；本仓库 `journal/default/` 清空（AGENTS.md 同步）
- `fiction/journal/`：4 篇创作日志（2026-03-16 ~ 2026-03-31）迁出至 `quanttide-journal-of-founder` 的 `write/<YYYY-MM>/`

## [1.1.1] - 2026-09-27

`journal/write/` 等 write 域资源分批迁出本仓库，移交叙事工程归档（quanttide-archive-of-narrative-engineering）；其中 fiction 主题日志随即回迁本仓库 `fiction/journal/`。内容逐字节不变。

### 路径映射

| 旧路径 | 新路径 |
|--------|--------|
| `journal/write/fiction/**` | `fiction/journal/**`（回迁本仓库） |
| `journal/write/**`（其余） | `quanttide/domains/quanttide-write/data/archive/journal/**` |
| `context/write/**` | `quanttide/domains/quanttide-write/data/archive/context/**` |
| `handbook/write/**` | `quanttide/domains/quanttide-write/data/archive/handbook/**` |
| `profile/write/**` | `quanttide/domains/quanttide-write/data/archive/profile/**` |
| `report/write/**` | `quanttide/domains/quanttide-write/data/archive/report/**` |

### Changed

- `fiction/journal/`：新建，回迁原 `journal/write/fiction/` 日志 4 篇（2026-03）
- `context/`、`handbook/`、`profile/`、`report/`：移除 write 层，资源平铺入领域归档同名资产目录
- AGENTS.md、README.md、CONTRIBUTING.md、fiction/README.md：移除「write 存量保持原状」表述，登记迁出与回迁目标
- 全部已知读者（本仓库文档、主仓库 `journal-to-archive` skill）已同步

## [1.1.0] - 2026-09-27

升级 `fiction/`、`game/` 一级主题目录以兼容记忆集新结构（`write/` 集更名 `fiction/`、新增 `game/` 集）；存量 `journal/write/` 保持原状不迁移。

### 路径映射

| 旧路径 | 新路径 |
|--------|--------|
| `journal/game/**` | `game/journal/**` |

### Added

- `fiction/README.md`：写作主线归档角色说明（作品 + fiction 记忆集日志归档位 `journal/`，按需创建）
- `game/README.md`：补充结构说明（项目文档 + `journal/` 记忆集日志）
- 归档规则：记忆集在归档站有同名一级主题目录时入 `<主题>/journal/`，否则入 `journal/<分类>/`

### Changed

- `journal/game/2026-05-02.md` → `game/journal/2026-05-02.md`
- README.md、AGENTS.md、CONTRIBUTING.md：结构与归档规则登记 `fiction/`、`game/` 一级目录，`journal/write/` 标注为存量保持原状
- 全部已知读者（本仓库文档、主仓库 `journal-to-archive` skill）已同步

## [1.0.1] - 2026-09-26

### Added

- `journal/default/`：日报备份 2026-07-29 ~ 2026-09-19
- `game/`：qtgame-war 遗留文档归档（`qtgame-war/docs/` 下 STATUS、brochure、bylaw、context、insight、intention、report、roadmap、spec）与 `game/README.md`
- `fiction/职场言情/`：初稿 `0_前言`、`男女主散步`，提纲 `男主演讲`，改稿 `展会再遇`，素材 `创作日记1`
- `profile/media/`：老街探店小红书文案

### Changed

- `fiction/职场言情/` 草稿按 提纲/素材/初稿/改稿 分目录整理（`小龙虾.md` 移入 `提纲/`）
- `AGENTS.md`、`CONTRIBUTING.md`：发布版本声明更新为 1.0.1

## [1.0.0] - 2026-08-10

首个正式发布（1.0.0）：归档结构与目录规范已稳定，后续版本遵循语义化版本规范，破坏性变更将单独声明。

### Added

- journal/default/: 接收来自 docs/memory 的日报备份 2026-06-28 ~ 2026-07-28

## [0.4.0] - 2026-06-01

### Added

- journal/default/: 接收来自 docs/memory 的日报备份 2026-05-06 ~ 2026-05-27
- journal/agent/: 接收 agent 日志备份 2026-05-26
- journal/health/: 接收 health 日志备份 2026-05-25
- report/write/: 接收报告归档 2026-05-30
- journal/: 接收来自 docs/memory 的 journal 归档
- report/: 接收来自 docs/memory 的 report 归档
- brochure/: 接收 brochure 归档
- context/: 接收 context 归档
- vision/: 接收 vision 归档
- profile/: 接收 profile 归档
- essay/: 接收 essay 归档
- laboratory/: 接收 laboratory 归档

## [0.3.1] - 2026-05-06

### Added

- journal/default/: 接收来自 docs/memory 的日报备份 2026-04-18 ~ 2026-05-05
- journal/product/: 接收产品日志备份 2026-05-02
- journal/game/: 接收游戏日志备份 2026-05-02
- journal/qtcloud/: 接收云平台日志备份 2026-05-02 ~ 2026-05-03

## [0.3.0] - 2026-05-05

### Added

- report/default/diary/: 接收来自 docs/memory 的日报归档
  - 2026-04-21.md, 2026-04-23.md, 2026-04-25.md, 2026-05-03.md
- report/write/diary/: 接收写作日志归档
  - 2026-05-03.md

## [0.2.1] - 2026-04-05

### Changed

- 接收 product/ 目录下的产品日志（从 journal 子模块归档）
- 将 legal/ 文件重组到 roadmap/ 目录下

## [0.2.0] - 2026-03-23

### Added

- **journal/write/history/**: Journal history archive
- **report/**: Report archives (default, code, write)

### Changed

- Expanded archive structure with multiple categories

## [0.1.0] - 2026-03-17

### Added

- **Archive Structure**: Initial project structure with journal, handbook, and platform modules
- **Journal Module**: Categorized work logs including default, product, code, write, execute, connect, data, agent, meta, stdn categories
- **Handbook Module**: Process documentation for journal cleaning, refining, and management
- **Platform Module**: 
  - Python packages: core, agent, apple, feishu
  - CLI tools for knowledge management and metadata processing
  - Test fixtures and examples
- **Git Configuration**: .gitignore for Python, IDEs, and environments
- **Documentation**: README, CONTRIBUTING, AGENTS, and CHANGELOG

### Changed

- Archive workflow: journal entries from 2026-03-11 to 2026-03-17
- Process documentation: refined journal cleaning and refinement procedures
