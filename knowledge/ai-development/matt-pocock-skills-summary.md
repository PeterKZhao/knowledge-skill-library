# Matt Pocock Skills Summary

来源：

- GitHub: https://github.com/mattpocock/skills
- Total TypeScript: https://www.totaltypescript.com/

## 定位

Matt Pocock 主要有两个对我们有价值的方向：

1. **TypeScript 工程知识**：来自 Total TypeScript，适合沉淀为前端、TypeScript、类型建模、React/Node 工程实践的技能资料。
2. **AI coding agent skills**：`mattpocock/skills` 是一组面向真实工程工作的 agent skills，重点不是“让 AI 多写代码”，而是修复 AI agent 在需求理解、上下文、任务拆分、交接和工程质量上的失败模式。

## 关键经验

### 1. 先对齐需求，再让 agent 写代码

Matt Pocock 的 skills repo 明确把“agent 没有真正理解需求”视为常见失败模式。对应做法是让 agent 先追问、澄清、盘清楚决策树，再进入实现。

可迁移到我们的项目：

- 对 `requirements.txt` 的每一行，先生成模型卡。
- 不直接生成 SQL 或 Java。
- 不清楚的业务词先问清楚，例如“报名”“预约”“核销”“应急信息”“实时客流”。

### 2. Skill 要小、可组合、可修改

该 repo 的 README 强调 skills 应该小、容易适配、可组合，而不是一个大而全的方法论。

可迁移到我们的项目：

- 不创建一个巨大 `travel-platform-skill`。
- 拆成 `travel-requirement-analysis`、`travel-ticketing-modeling`、`travel-map-route-modeling` 等。
- 每个 skill 只负责一个稳定流程。

### 3. 建立项目共享语言

Matt Pocock 的经验里，agent 进入项目后常常不理解团队术语，所以需要共享上下文和统一语言。

可迁移到我们的项目：

- 为旅游项目维护“业务词典”。
- 明确“活动”“公告”“应急信息”“门票产品”“权益”“核销”“售后”等词的含义。
- 对 ruoyi-vue-pro 已有表和新增扩展表建立统一命名规则。

### 4. 交接和压缩上下文是技能的一部分

`handoff` 类技能适合长任务和跨会话继续工作。

可迁移到我们的项目：

- 每次完成一个需求模型卡后，更新索引。
- 每次完成一批 SQL 设计后，记录复用表、扩展表、不变量、未决问题。
- 长任务结束前生成“下一步上下文”。

## 对我们 Skill Library 的启发

建议新增或完善这些技能：

- `travel-requirement-analysis`
  - 先问清楚业务目标。
  - 输出统一模型卡。
  - 标记 CRUD、状态模型、数学模型、外部系统集成。

- `travel-domain-language`
  - 维护旅游项目业务词典。
  - 统一中英文术语。
  - 统一 ruoyi 表复用和扩展表命名。

- `frontend-typescript-engineering`
  - 学习 Matt Pocock 的 TypeScript 教学思路。
  - 面向前端类型安全、接口 DTO、状态建模、组件 props 类型、表单 schema。

## 在本项目中的使用规则

1. 复杂需求进入实现前，先进入“grill / 澄清”阶段。
2. 每个技能要小，不要把需求、SQL、Java、前端全部写进一个 skill。
3. 对长期项目，必须维护共享语言和交接文档。
4. TypeScript/前端相关技能可参考 Total TypeScript 的“练习驱动、真实问题、类型精确”风格。

## 可直接复用的提示词

```text
请先不要写代码。请像 Matt Pocock skills 的 grill-me 流程一样，围绕这个需求追问我，直到参与者、输入、输出、状态、不变量、异常场景和复用表都清楚。
```

```text
请把这个需求拆成小型可组合 skill，而不是创建一个大而全的项目 skill。
```
