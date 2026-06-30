# Engineering Skill Patterns From Matt Pocock And Superpowers

本文件总结两个 skill 来源对我们构建可复用技能库的启发：

- Matt Pocock skills: https://github.com/mattpocock/skills
- Superpowers: https://github.com/obra/superpowers

## 共同原则

1. **先澄清，再实现**
   - 不让 agent 在需求未清楚时直接写代码。
   - 通过追问、模型卡、设计确认降低返工。

2. **技能要小而可组合**
   - 一个 skill 只解决一个稳定问题。
   - 多个 skill 串联形成工作流。

3. **共享语言很重要**
   - 业务词、领域模型、表名、状态名要统一。
   - 复杂项目需要 domain language 文档。

4. **计划必须可执行**
   - 不写空泛计划。
   - 每一步要有文件、输入、输出、验证方式。

5. **完成前必须验证**
   - 不能只交付“看起来完成”。
   - 要说明检查证据、测试结果、剩余风险。

## 推荐 Skill 骨架

```text
skill-name/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── workflow.md
    ├── checklist.md
    └── examples.md
```

## SKILL.md 应包含

- 触发场景。
- 核心工作流。
- 输出格式。
- 何时读取 references。
- 必须验证的项目。
- 禁止事项。

## References 应包含

- 详细模板。
- 示例模型卡。
- 状态机示例。
- SQL 复用矩阵。
- 测试样例。

## 用于旅游项目的下一批技能

### `travel-requirement-analysis`

借鉴：

- Matt Pocock 的需求澄清方式。
- Superpowers 的 brainstorming 流程。

职责：

- 对 `requirements.txt` 每一行追问。
- 输出模型卡。
- 标记是否需要数学建模。

### `travel-reuse-first-design`

借鉴：

- Superpowers 的 verification-before-completion。

职责：

- 查 ruoyi-vue-pro 已有表。
- 判断复用或扩展。
- 阻止重复造表。

### `frontend-typescript-engineering`

借鉴：

- Matt Pocock 的 TypeScript 教学和工程实践。

职责：

- 前端类型建模。
- API DTO 类型。
- 表单 schema。
- Vue/React 组件 props 类型设计。

## 检查清单

创建新 skill 前，先回答：

1. 这个 skill 是否解决一个高频问题？
2. 这个问题是否容易出错？
3. 是否能用现有 skill 解决？
4. 输入和输出是否稳定？
5. 是否有清晰验证方法？
6. 是否能拆成更小的 skill？
