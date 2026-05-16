# Changelog.md

本项目所有重要变更将被记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)  
本项目遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/)

## [0.8.0] - 2026-05-17 (UTC+8)

### Changed
- **重构首页 (`index.md`)**：将原有的空泛愿景替换为实务性的“管理改革提案”。

### Changed
- `pyproject.toml`: 版本号升级至 `0.8.0`。

## [0.7.0] - 2026-05-17 (UTC+8)

### Added
- 新增 `docs/skills/communication.md`：建立组织级沟通规范与异步协作共识。

### Changed
- `pyproject.toml`: 版本号升级至 `0.7.0`。

## [0.6.0] - 2026-05-17 (UTC+8)

### Added
- 新增 `docs/skills/docs-standard.md`：建立 THRD 文档标准。

### Changed
- `pyproject.toml`: 版本号升级至 `0.6.0`。

## [0.5.0] - 2026-05-16 (UTC+8)

### Added
- 新增 `docs/governance/access-control.md`：确立基于技能等级（L1-L3）的权限矩阵。
- 引入“休眠与复苏”机制：以 180 天为周期进行安全保护，支持一键恢复权限。

### Changed
- `pyproject.toml`: 版本号升级至 `0.5.0`。

## [0.4.0] - 2026-05-16 (UTC+8)

### Added
- 新增 `docs/governance/decision-making.md`：确立“Issue 讨论 -> PR 定稿”的异步决策流。
- 确立 RFC (提案) 流程，明确“未合并即无效”的决策原则。

### Changed
- 修改 `mkdocs.yml`：开启 `admonition` 及其相关扩展，支持 `!!!` 提示框语法。
- 修改 `README.md` 项目结构：新增 `docs/proposals/` 目录。
- `pyproject.toml`: 版本号升级至 `0.4.0`。 

## [0.3.0] - 2026-05-15 (UTC+8)

### Added
- 新增 `docs/skills/tech-stack.md`：建立基于核心项目（TMA、Danmaku Sender）的“Python/Vue 3 二选一”最小准入标准。
- 在 `tech-stack.md` 中明确对全栈（Full-stack）能力的鼓励与职能互补原则。

### Changed
- `README.md`: 完整同步最新目录树结构，明确 `skills/` 目录的技术准入属性与维护者要求。
- `pyproject.toml`: 版本号升级至 `0.3.0`，更新项目描述以体现技术改革导向。

## [0.2.0] - 2026-05-15 (UTC+8)

### Added
- 新增 `docs/governance/maintainer-role.md`：明确“三位一体”维护者（Maintainer）角色定义。
- 确立“管理即代码”核心理念：异步协作、文档先行、工业级极简。
- 建立维护者身份流转机制：取消传统行政职级，强调技术共感与共同维护。

### Changed
- `pyproject.toml`: 版本号升级至 `0.2.0`。

## [0.1.0] - 2026-05-15 (UTC+8)

### Added
- 初始化 MkDocs 骨架，配置 Material 工业级主题。
- 建立 `pyproject.toml` 作为项目元数据与依赖管理中心。
- 预设 `governance/`, `action-guide/`, `skills/`, `ethics/` 四大核心目录。