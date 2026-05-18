# THRD Protocol

Teahouse of Recollected Dreams 管理改革大纲与行动指南。  
本项目采用 `MkDocs + Material` 主题构建，实现“管理即代码”的自动化流程。

### 1. 项目骨架结构
```
THRD-Protocol/
├── pyproject.toml          # 项目配置，定义依赖与版本
├── mkdocs.yml              # MkDocs 配置
├── README.md               # 仓库维护与本地开发引导
├── .gitignore              # 忽略编译产物与虚拟环境
└── docs/                   # 文档源码目录
    ├── index.md            # 首页：茶馆愿景与管理改革初衷
    ├── changelog.md        # 变更记录（北京时间 CST）
    ├── governance/         # 【治理逻辑】
    │   ├── maintainer-role.md  # 角色定义：三位一体维护者架构
    │   ├── decision-making.md  # 决策流：Issue-PR 异步协作流程
    │   └── access-control.md   # 权限矩阵：技能挂钩的资源分配
    ├── action-guide/       # 【行动指南 SOP】
    │   ├── dev-workflow.md     # 开发流：代码维护与提交标准
    │   ├── labels.md           # Github标签：任务流转的“语言”
    │   └── onboarding.md       # 入馆指南：维护者准入考核
    ├── skills/             # 【技能大纲】
    │   ├── tech-stack.md       # 技术栈：Python/Vue 3 二选一准入要求
    │   ├── docs-standard.md    # 文档标准：Markdown 与去富文本化规范
    │   └── communication.md    # 沟通规范：异步协作下的文明与效率
    ├── ethics/             # 【伦理与边界】
    │   ├── data-privacy.md     # 数据隐私：归档数据的处理底线
    │   └── thrd-spirit.md      # 茶馆精神：数字保存的初心
    └── assets/             # 静态资源目录
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
* **版本控制：** 版本号直接在 `pyproject.toml` 中维护。
* **变更记录：** 所有管理制度的变动必须同步更新 `docs/changelog.md`