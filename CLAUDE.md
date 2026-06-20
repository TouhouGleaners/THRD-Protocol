# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在本仓库中工作时提供指引。

## 项目概述

THRD-Protocol 是拾遗梦茶馆（Teahouse of Recollected Dreams）的治理文档站点，隶属于 TouhouGleaners GitHub 组织，专注于东方 Project 资源的归档与保存。站点使用 MkDocs Material 构建，部署至 GitHub Pages。

这是一个**纯文档仓库**——不含任何应用源代码。核心理念是"管理即代码"，将组织规则、角色和流程定义为版本控制中的 Markdown 文件，通过 Git PR 工作流驱动变更。

## 常用命令

```bash
# 本地预览（提交 PR 前必须运行）
mkdocs serve

# 安装依赖
pip install .

# 部署（推送到 main 时由 CI 自动执行）
mkdocs gh-deploy --force
```

## 架构说明

```
docs/                   # MkDocs 源文件——所有治理文档在此
├── index.md            # 首页：改革方案白皮书
├── governance/         # 组织规则（权限控制、决策机制、维护者角色）
├── action-guide/       # 协作 SOP（开发流程、标签规范、入职指南）
├── skills/             # 维护者技能要求（沟通、文档标准、技术栈）
├── ethics/             # 伦理与原则（数据隐私、THRD 精神）
├── about.md            # 协议历史与致谢
└── changelog.md        # Keep a Changelog 格式，SemVer 版本管理
mkdocs.yml              # 站点配置：主题、导航、插件、扩展
overrides/              # MkDocs Material 主题覆盖（自定义版权页脚）
pyproject.toml          # Python 依赖（mkdocs、mkdocs-material、git-revision-date 插件）
.github/workflows/      # CI：推送到 main 且 docs/ 或 mkdocs.yml 变更时自动部署
```

导航结构定义在 `mkdocs.yml` 中——更新导航必须修改该文件，而非仅添加文件。

## 文档写作规范

`docs/` 中的所有文档必须遵循以下规则（详见 `docs/skills/docs-standard.md`）：

- **Kebab-case 文件命名**：全小写加连字符（如 `dev-workflow.md`）
- **盘古排版**：中文与英文/数字/标点之间需加半角空格（如 `使用 MkDocs 构建`，而非 `使用MkDocs构建`）
- **空行要求**：标题、有序列表、无序列表、admonition 前后必须有空行，否则 MkDocs 无法正常渲染
- **代码块**：必须指定语言（python、yaml、bash 等）
- **禁止使用检查列表**：`- [ ]` 语法在 `docs/` 中被禁用（MkDocs 渲染不稳定），改用普通无序列表
- **链接和图片**：仅使用相对路径
- **Admonition 语法**：使用 `!!! tip/info/danger` 格式
- **本地预览**：提交 PR 前必须运行 `mkdocs serve` 验证渲染效果

## Git 规范

- **禁止直接推送到 `main`**——所有变更通过 PR 以 Squash and Merge 方式合并
- **分支命名**：`type/description`（如 `feat/labels-docs`、`ci/deploy-workflow`、`style/custom-logo`）
- **提交信息**：Conventional Commits 格式——`type(scope): 中文描述`（如 `feat(gov): 规范维护者晋升与退出机制`）
- **非常规提案**：通过 GitHub Issues 提交，使用 `Type: Proposal` 标签
- **核心原则**："没有记录就没有发生"——口头约定不具有官方效力

## 三轨维护者体系

文档中定义了三种维护者角色：
- **运营维护者**：内容审核、社区管理——使用 GitHub 网页端
- **技术维护者**：工具开发、脚本、自动化——Python 或 Vue 3
- **核心维护者**：兼具运营和技术能力的跨职能领导者
