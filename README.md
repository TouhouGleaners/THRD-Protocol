# THRD Protocol

Teahouse of Recollected Dreams 管理改革大纲与行动指南。
本项目采用 `MkDocs + Material` 主题构建，实现“管理即代码”的自动化流程。

### 1. 项目骨架结构
```
THRD-Protocol/
├── pyproject.toml          # 现代化项目配置，定义依赖与版本
├── mkdocs.yml              # MkDocs 核心配置（含插件、时区与导航）
├── README.md               # 仓库引导手册
├── .gitignore              # 忽略 site/ 及 Python 环境
└── docs/                   # 文档源码（MkDocs 扫描目录）
    ├── index.md            # 首页：管理改革的愿景、使命与 THRD 的核心价值观
    ├── changelog.md        # 组织管理制度的变更日志
    ├── governance/         # 【治理逻辑】
    │   ├── maintainer-role.md  # 管理层定义：是 Maintainer 而非 Manager
    │   ├── decision-making.md  # 决策流：如何通过 RFC 提出改革
    │   └── access-control.md   # 权限矩阵：服务器、仓库、API Credits 的分配
    ├── action-guide/       # 【行动指南 (SOP)】
    │   ├── dev-workflow.md     # 开发流：从 Issue 到 PR 的管理标准
    │   ├── incident-report.md  # 故障复盘：Post-mortem 的编写规范
    │   └── onboarding.md       # 成员准入：新成员如何通过考核并获得权限
    ├── skills/             # 【技能大纲】
    │   ├── tech-stack.md       # 技术要求：?
    │   ├── docs-standard.md    # 文档标准：如何写出符合“工业级”要求的文档
    │   └── communication.md    # 沟通规范：异步协作下的文明与效率
    ├── ethics/             # 【伦理与边界】
    │   ├── data-privacy.md     # 归档数据的隐私边界（如弹幕中的用户信息）
    │   └── thrd-spirit.md      # THRD 精神：非营利与数字保存的初心
    └── assets/             # 静态资源（Logo、架构图等）
```

### 2. 快速开始

**本地开发**
本项目使用 Python 3.12+ 环境：
```
# 安装依赖 (建议在 venv 下执行)
pip install .

# 启动本地实时预览服务器
mkdocs serve
```
启动后访问：[http://127.0.0.1:8000](http://127.0.0.1:8000)

**版本规范**
* **版本控制：**版本号直接在 `pyproject.toml` 中维护。
* **变更记录：**所有管理制度的变动必须同步更新 `docs/changelog.md`