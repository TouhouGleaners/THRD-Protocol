# Changelog.md

本项目所有重要变更将被记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)  
本项目遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/)

## [1.0.0-beta.2] - 2026-06-21 (UTC+8)

### Changed
- **导航重组**：新增"入门"板块，`onboarding.md` 迁出治理目录；板块重命名为"成员分类"，决策流程与沟通规范移入"行动指南"。
- 首页（`index.md`）重写为欢迎页，包含推荐导航与板块卡片。
- 改革白皮书独立为 `proposal.md`。
- 运营维护者补充 PR Review 权限。
- 技能大纲补充技术路线说明。
- 术语首次出现时附加解释。

### Fixed
- 修正多处引号样式与相对路径。
- 修正白皮书盘古排版。

## [1.0.0-beta.1] - 2026-06-09 (UTC+8)

### Added
- 新增 `docs/assets/` 目录：存放全局静态资源。
- 新增 `governance/lifecycle.md`：维护者生命周期文档，涵盖退出、休眠与除名机制。

### Changed
- **重写关于页面 (`about.md`)**：补充协议起因、编写过程与期望。
- **治理文档结构重组**：将原本混杂在各文档中的内容按主题拆分为独立文档，每篇文档聚焦单一主题。
    - `maintainer-role.md`：仅保留角色定义与晋升机制，退出/除名移至 `lifecycle.md`。
    - `access-control.md`：移除休眠保护机制，仅保留权限分配与授权矩阵。
    - `decision-making.md`：将“为什么用 PR”作为理念说明移至文档开头，裁决流程简化为“批准 / 拒绝 / 异议”三步。
    - `index.md`：新增生命周期导航条目，移除未实现的“快速上手清单”引用，弱化改革提案中的个人色彩表述。
    - `README.md`：目录结构新增 `lifecycle.md`。
- **裁决机制简化**：将原“否决 + 否决覆写”机制简化为“拒绝 + 异议”流程——任一核心维护者可直接合并或拒绝（需书面解释并打标签），其他维护者可在 7 天内表态反对拒绝，超过全体维护者半数则强制合并。
- **除名机制简化**：将原“两步走”流程简化为统一的三步流程——降权与归档（24h）→ 裁决表决（7d）→ 除名或恢复 → 申诉（7d）。
- **权限矩阵简化**：状态-权限映射表移除观察期、即时除名等中间状态，合并为统一的除名 (Removal) 状态。

## [1.0.0-alpha.1] - 2026-05-20 (UTC+8)

### Added
- **发布 THRD Protocol 首个公开预览版 (Alpha 1)**。
- 新增 `docs/about.md`：记录本协议的起源历史。.
- **新增全局样式 (`overrides/partials/copyright.html`)**：定制版权信息，明确版权归属。

### Changed
- **重构引导手册 (`README.md`)**：同步最新的 A-Z 目录树，将“三条协作红线”前置。
- **优化全局配置 (`mkdocs.yml`)**：
    - 调整“伦理与边界”板块顺序，优先展示《THRD 精神共识》。
    - 启用 `navigation.footer` 扩展，支持底部的“上一页/下一页”双向导航。
    - 集成自定义 copyright 组件，替换默认版权信息。
- `pyproject.toml`: 版本号正式升级至 `1.0.0-alpha.1`。

## [0.19.0] - 2026-05-20 (UTC+8)

### Added
- **确立维护者全生命周期管理 (`maintainer-role.md`)**：
    - 新增“主动退出机制”，确立 `Emeritus`（荣誉成员）的流转路径。
    - 新增“两步走强制除名机制”：确立 24 小时内紧急挂起与 7 天内核心维护者表决裁决制衡。

### Changed
- **统一组织角色称谓**：
    - 将 `maintainer-role.md` 与 `access-control.md` 中的角色名称统一规范为“运营维护者”、“技术维护者”和“核心维护者”。
    - 在权限矩阵下方的说明中补齐了 `Dormant`（休眠）与 `Emeritus`（荣誉成员）的授权细节，完成逻辑对齐。
- `pyproject.toml`: 版本号升级至 `0.19.0`。

## [0.18.0] - 2026-05-19 (UTC+8)

### Changed
- **重构门户首页 (`index.md`)**：将“管理改革提案”与“协作指南”整合为全新的门户界面，引入卡片式网格导航。
- **优化全局配置 (`mkdocs.yml`)**：
    - 集成 Material 工业级图标 (Emoji/Icons) 解析。
    - 开启网格布局 (Grid) 与 HTML 混排支持。
- **完善决策裁决逻辑**：修改 `decision-making.md` 紧急例外情况应对办法并区分协议修正（PR 驱动）与独立提案（Issue 驱动）两条路径。
- 确立“Issue 闭环管理”：独立提案不再产生物理文件，通过 Issue 首楼更新与裁决回复实现定稿。
- `pyproject.toml`: 版本号升级至 `0.18.0`。

### Removed
- 撤销物理提案目录 (`docs/proposals/`) 及故障复盘制度。

## [0.17.0] - 2026-05-18 (UTC+8)

### Added
- 新增 `docs/action-guide/labels.md`：建立全量标准化 GitHub 标签系统参考手册。

### Changed
- **集成标签至工作流**：在 `docs/action-guide/dev-workflow.md` 中增加“标签应用参考”章节。
- **完善导航体系 (`mkdocs.yml`)**：将标签系统正式纳入“行动指南”导航板块。
- `pyproject.toml`: 版本号升级至 `0.17.0`。

## [0.16.0] - 2026-05-18 (UTC+8)

### Added
- 新增 `docs/action-guide/dev-workflow.md`: 建立完整的开发与维护工作流规范。

### Changed
- **重构决策流裁决机制 (`decision-making.md`)**：
    - 确立“审计权与裁决规范”：明确核心维护者在执行合并时的质量审计职能。
    - 在 `dev-workflow` 与 `decision-making` 中互引，明确区分组织级决策与日常维护任务。
- `pyproject.toml`: 版本号升级至 `0.16.0`。

## [0.15.0] - 2026-05-18 (UTC+8)

### Added
- 新增 `docs/ethics/data-privacy.md`：建立数据隐私与补档内容伦理规范。

### Changed
- `pyproject.toml`: 版本号升级至 `0.15.0`。

## [0.14.0] - 2026-05-18 (UTC+8)

### Changed
- **重构决策流方案 (`decision-making.md`)**：使之与运营/技术双轨职能架构对齐。
- 完善提案库（Proposals）的分类与 RFC 流程说明。
- `pyproject.toml`: 版本号升级至 `0.14.0`。

## [0.13.0] - 2026-05-18 (UTC+8)

### Changed
- **重构权限矩阵 (`access-control.md`)**：将原有的等级制（L 序列）权限逻辑重构为基于职能路径（运营/技术/核心）的授权体系。
- `pyproject.toml`: 版本号升级至 `0.13.0`。

## [0.12.0] - 2026-05-18 (UTC+8)

### Added
- 新增 `docs/action-guide/onboarding.md`：建立基于 GitHub 网页版的维护者入馆引导。

### Changed
- `pyproject.toml`: 版本号升级至 `0.12.0`。

## [0.11.0] - 2026-05-17 (UTC+8)

### Changed
- **重构技能大纲 (`tech-stack.md`)**：优化文档结构以适配“双轨制”职能架构，调整部分表述。
- `pyproject.toml`: 版本号升级至 `0.11.0`。

## [0.10.0] - 2026-05-17 (UTC+8)

### Added
- 新增 `docs/ethics/thrd-spirit.md`：建立“维护者共识”。

### Changed
- `pyproject.toml`: 版本号升级至 `0.10.0`。

## [0.9.0] - 2026-05-17 (UTC+8)

### Changed
- **重构角色定义 (`maintainer-role.md`)**：全面对接“管理改革提案”逻辑。
- 将维护者架构由等级制转为**职能制**，定义了“运营型 (Ops)”、“技术型 (Tech)”与“复合型 (Composite)”三类核心角色。
- 引入“双向演进”机制，明确了运营与技术路径之间的互补性与流动性。
- 细化了各类角色的职责范围、定位及所需的协作工具（网页端 vs 客户端）。
- `pyproject.toml`: 版本号升级至 `0.9.0`。

## [0.8.0] - 2026-05-17 (UTC+8)

### Changed
- **重构首页 (`index.md`)**：将原有的空泛愿景替换为实务性的“管理改革提案”。
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