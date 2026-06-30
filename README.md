# Knowledge Skill Library

本仓库是 President-Office 的知识与技能资产库，用于沉淀可复用的业务知识、工程方法、Agent skills、项目规划模板和研究结论。

它不是单个业务项目的 README，也不是某一次技术选型笔记。具体项目、具体仓库、具体产品的操作说明应放在对应项目仓库；本仓库只保留可跨项目复用、值得长期沉淀的知识与方法。

## 仓库定位

本仓库承载三类长期资产：

1. **Knowledge**：可复用知识、研究摘要、技术判断、业务建模经验、项目复盘结论。
2. **Skills**：可复用的 Agent/Codex/Hermes 工作方法、提示结构、检查清单、模型卡模板。
3. **Project Planning Assets**：项目规划、需求拆解、模型卡、技能结构和跨项目方法论。

不适合放在这里的内容：

- 单个项目的当前进度。
- 某个 Issue / PR 的临时状态。
- 生产密钥、账号、服务器信息。
- 未提炼的聊天记录。
- 只对一个仓库有效、不能复用的操作细节。

## 目录结构

```text
knowledge-skill-library/
├── README.md                         # 本仓库说明与使用规则
├── knowledge/                        # 可复用知识库
│   ├── README.md                     # Knowledge 索引
│   ├── ai-development/               # AI 开发、Agent 方法论
│   ├── java/                         # Java / 生命周期 / 建模实践
│   ├── model-cards/                  # 模型卡与需求表达样例
│   └── ruoyi-vue-pro/                # RuoYi/Yudao 相关复用知识
├── skills/                           # 可复用技能库
│   ├── README.md                     # Skill 索引
│   ├── project-planning/             # 项目规划、模型卡、技能结构
│   └── skill-sources/                # 外部工程技能模式整理
├── docs/                             # 面向具体主题的综合文档
└── *.json / *.xlsx / *.md            # 待归档或原始资料
```

## 快速入口

### Knowledge Library

见 `knowledge/README.md`。

当前包含：

- AI 开发与 Agent 技能总结。
- Java 生命周期与数学建模实践。
- RuoYi-Vue-Pro / Yudao 复用设计。
- 多语言站点模型卡。

### Skill Library

见 `skills/README.md`。

当前包含：

- 项目技能体系结构。
- 需求模型卡模板。
- 工程技能模式整理。

### 主题文档

当前 `docs/` 中包含：

- `docs/main-job-ai-platform.md`：主业 AI 平台相关规划沉淀。

## 内容分层规则

### Knowledge：保存“知道什么”

适合放入 `knowledge/`：

- 技术或业务判断的长期结论。
- 多项目可复用的研究摘要。
- 架构、建模、产品、业务流程的经验总结。
- 对外部项目、框架、工具的评估结论。

示例：

- `knowledge/java/java-lifecycle-modeling-github-practices.md`
- `knowledge/ruoyi-vue-pro/ticket-mall-reuse-design.md`

### Skills：保存“怎么做”

适合放入 `skills/`：

- Agent 执行流程。
- 提示模板。
- 检查清单。
- 可复用的建模步骤。
- 可迁移到 Hermes / Codex skill 的结构化方法。

示例：

- `skills/project-planning/project-skills-structure.md`
- `skills/project-planning/model-card-template.md`

### Docs：保存“某个主题的成体系说明”

适合放入 `docs/`：

- 跨多个知识条目的主题性总结。
- 业务方向规划。
- 需要连续阅读的综合文档。

## 写入原则

新增内容前先判断它属于哪一类：

```text
事实 / 研究 / 判断       → knowledge/
流程 / 方法 / 模板       → skills/
主题规划 / 综合说明      → docs/
原始资料 / 待整理数据    → 暂存根目录或后续归档
```

写入时遵守：

1. **先提炼再沉淀**：不要把聊天流水账原样放进仓库。
2. **长期有效优先**：能在多个项目复用的内容优先进入本库。
3. **项目事实回项目仓库**：具体项目当前状态、Issue、PR、部署说明应放回对应项目。
4. **方法可迁移**：流程类内容应尽量整理成可迁移的 skill、模板或检查清单。
5. **敏感信息禁止入库**：不得写入 token、密码、服务器凭据、客户隐私和未授权数据。
6. **索引同步更新**：新增 `knowledge/` 或 `skills/` 内容时，同步更新对应目录的 `README.md`。

## 推荐工作流

### 沉淀一条知识

1. 明确知识来源：讨论、研究、项目复盘、外部文档或代码实践。
2. 提炼长期结论，去掉临时过程。
3. 判断归档位置：`knowledge/`、`skills/` 或 `docs/`。
4. 写入 Markdown，并补充适用范围、限制和引用来源。
5. 更新对应索引。

### 沉淀一个 Skill

1. 识别高频、易错、需要一致执行的流程。
2. 写清触发场景、输入、步骤、输出、检查清单和反模式。
3. 把长资料放到 `references/` 或 `knowledge/`，不要塞进单个 skill 说明。
4. 如果要安装到 Hermes/Codex，再迁移为对应工具要求的 `SKILL.md` 结构。

### 归档一次项目经验

1. 项目当前状态留在项目仓库。
2. 只把跨项目可复用的方法、判断、模板沉淀到本仓库。
3. 如果是业务专属知识，优先考虑放入对应业务 Organization 的 `knowledge-base` 或 `skills-library`。
4. 只有跨业务可复用时，再上提到本仓库。

## 与其他仓库的边界

- `ai-project-operating-system`：定义 GitHub-first 的 AI 项目操作系统、Issue/PR/Spec/ADR/Harness/CI 流程。
- `knowledge-skill-library`：沉淀跨项目可复用的知识与技能资产。
- 具体业务仓库：保存该业务的代码、需求、部署、运行状态和业务专属知识。
- 业务 `knowledge-base` / `skills-library`：保存某个业务单元自己的知识和技能；成熟后再上提公共内容。

## 当前待整理项

根目录仍存在一些历史资料和原始文件，例如：

- `erpnext-vs-ruoyi-vue-pro-influencer-admin.md`
- `gaokao-skills-summary.md`
- `insurance-skills-and-rag-summary.xlsx`
- `mysql-projects.json`
- `projects.json`

这些内容可以后续按主题迁移到 `knowledge/`、`skills/` 或 `docs/`，并在迁移时更新索引。
