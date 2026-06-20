# THRD Protocol

Teahouse of Recollected Dreams 管理改革大纲与行动指南。  
本项目采用 `MkDocs + Material` 主题构建，实现“管理即代码”的自动化流程。

我们通过将组织规范文件化、流程工具化，彻底消除单点故障风险，确保那些珍贵的东方资源得以长久安全地留存。

---

### 1. 协议目录结构 (A-Z)
```plaintext
THRD-Protocol/
├── .gitignore              # 忽略本地编译产物与虚拟环境
├── README.md               # 仓库引导手册（本文件）
├── mkdocs.yml              # MkDocs 核心配置文件
├── pyproject.toml          # 项目元数据与依赖配置
└── docs/                   # 文档源码目录（MkDocs 扫描目录）
    ├── getting-started/    # 【入门】
    │   └── onboarding.md       # 入馆指南：维护者 PR 准入实操
    ├── governance/         # 【成员分类】
    │   ├── access-control.md   # 权限矩阵：技能挂钩的资源分配标准
    │   ├── lifecycle.md        # 维护者生命周期：退出、休眠与除名机制
    │   └── maintainer-role.md  # 角色定义：运营/技术/核心三轨架构
    ├── action-guide/       # 【行动指南】
    │   ├── communication.md    # 沟通规范：GitHub 与即时通讯的流转红线
    │   ├── decision-making.md  # 决策流程：Issue-PR 异步决策与裁决规范
    │   ├── dev-workflow.md     # 开发工作流：从 Issue 到 PR 的协作规范
    │   └── labels.md           # 标签系统：任务流转与状态控制的标准化语言
    ├── skills/             # 【技能大纲】
    │   ├── docs-standard.md    # 文档标准：去富文本化的 Markdown 排版礼仪
    │   └── tech-stack.md       # 技术要求：Python/Vue 3 二选一准入标准
    ├── ethics/             # 【伦理与边界】
    │   ├── data-privacy.md     # 数据隐私：归档数据的处理底线与净化标准
    │   └── thrd-spirit.md      # 茶馆精神：对抗数字遗忘的维护者共识公约
    ├── assets/             # 静态资源目录（Logo、架构图等）
    ├── about.md            # 关于协议：历史致谢与版本记录
    ├── changelog.md        # 变更记录
    ├── index.md            # 首页：欢迎页与导航
    └── proposal.md         # 改革白皮书
```

---

## 2. 核心协作红线

在参与茶馆维护之前，请全体维护者（Maintainer）牢记以下三条硬性红线：

1.  **严禁直接推送主分支**：除了紧急状态下的核心维护者外，任何改动必须通过创建独立分支并提交 **Pull Request (PR)**，经评审通过后，由核心维护者执行 **Squash and Merge** 归档。
2.  **独立提案 Issue 闭环**：临时活动（如周年庆）、新项目立项等非制度性事务统一通过新建标签为 `Type: Proposal` 的 **GitHub Issue** 进行讨论、定稿与归档。
3.  **未记录即未达成**：任何口头或群聊达成的共识，若未最终转化为 Protocol 仓库中的 PR 提交或 Issue 总结，一律不具备官方效力。

---

## 3. 本地预览开发

本项目使用 Python 构建。在修改文档并提交 PR 之前，请务必在本地预览渲染效果。

### **步骤 1：安装依赖**
推荐在 Python 虚拟环境（venv）下进行安装：
```bash
# 克隆仓库
git clone https://github.com/TouhouGleaners/THRD-Protocol.git
cd THRD-Protocol

# 安装本地包及全部依赖
pip install -e .
```

### **步骤 2：启动预览服务器**
```bash
mkdocs serve --livereload
```
启动后访问本地回环地址：[http://127.0.0.1:8000](http://127.0.0.1:8000) 进行实时调试。

---

## 4. 自动化与基础设施

- **分支保护规则**：本仓库 `main` 分支已开启 Ruleset 保护，未通过 Review 的 PR 将被系统自动拒绝。
- **权限流转**：权限分配与 [权限矩阵](./docs/governance/access-control.md) 挂钩，通过 Git 历史记录进行公开审计。