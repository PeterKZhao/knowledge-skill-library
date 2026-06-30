# Superpowers Agentic Skills Summary

来源：

- GitHub: https://github.com/obra/superpowers

## 定位

Superpowers 是一套面向 coding agents 的软件开发方法论和技能集合。它不是单个技能，而是把需求澄清、设计、计划、TDD、执行、代码审查、验证、收尾等环节组织成一套可触发、可组合的工作流。

## 核心流程

Superpowers 的基础流程可以概括为：

1. **Brainstorming**
   - 写代码前先澄清目标。
   - 通过问题把模糊需求变成明确设计。
   - 分段展示设计，让用户确认。

2. **Writing Plans**
   - 在设计确认后写实施计划。
   - 计划要足够具体：文件、任务、验证步骤、边界条件。

3. **Executing Plans / Subagent-Driven Development**
   - 按计划分批执行。
   - 可用子代理分工。
   - 每个阶段有检查点和 review。

4. **Test-Driven Development**
   - 强调先写失败测试，再写最小实现，再重构。
   - 避免 agent 先写大量无法验证的代码。

5. **Requesting / Receiving Code Review**
   - 在任务之间主动请求代码审查。
   - 先看是否符合规格，再看代码质量。

6. **Verification Before Completion**
   - 完成前必须验证。
   - 不能只说“应该可以”，要给证据。

7. **Finishing A Development Branch**
   - 完成后处理测试、合并、PR、清理工作区。

## 对我们项目的价值

### 1. 需求分析阶段

可迁移为：

```text
requirements.txt -> 模型卡 -> 复用表判断 -> 数学建模 -> SQL 草案 -> codegen -> Java 服务
```

不要直接从 `requirements.txt` 跳到 SQL。

### 2. 复杂业务阶段

适用于：

- 门票核销
- 年卡权益
- 退款
- 座位锁定
- 会员积分
- 路线推荐
- 停车计费
- 招商租赁费用

这些都必须先有不变量、状态机和测试样例。

### 3. 技能体系阶段

Superpowers 的启发是：技能不是静态文档，而是“触发条件 + 工作流 + 验证方式”。

我们的技能应写成：

- 什么时候触发。
- 先读哪些参考资料。
- 输出什么结构。
- 何时停止。
- 怎样验证。

## 可迁移到 Knowledge Skill Library 的 Skill 模式

### Brainstorming For Requirements

用于：

- 用户给出模糊需求。
- `requirements.txt` 的某一行需要拆解。

输出：

- 业务目标。
- 参与者。
- 输入。
- 输出。
- 状态。
- 不变量。
- 未决问题。

### Reuse-First Design

用于：

- ruoyi-vue-pro 项目建表前。

输出：

- 可复用表。
- 不能复用的原因。
- 必须新增的扩展表。
- 是否适合 codegen-bot。

### Verification Before Completion

用于：

- 文档更新。
- SQL 设计。
- Java 服务实现。
- codegen 后检查。

输出：

- 已执行检查。
- 未能执行的检查。
- 剩余风险。

## 对我们已有 Skills 的调整建议

- `travel-requirement-analysis`
  - 增加 brainstorming 流程。
  - 不清楚时先问问题。

- `java-math-modeling`
  - 增加 verification-before-completion 规则。
  - 每个公式或状态机必须有测试样例。

- `ruoyi-mysql-style`
  - 增加 reuse-first 检查。
  - SQL 设计前先查已有 ruoyi 表。

- `ruoyi-codegen-bot-workflow`
  - 增加执行计划和生成后 review。
  - 多模块生成后检查目录、菜单、权限、API、前端页面。

## 可直接复用的提示词

```text
请按 Superpowers 的方式工作：先 brainstorming 澄清需求，再写设计，再写计划。没有经过我确认，不要进入实现。
```

```text
请在完成前执行 verification-before-completion：列出你检查了什么、证据是什么、还有什么风险。
```

```text
请先做 reuse-first design：查 ruoyi-vue-pro 已有表，说明哪些复用，哪些必须扩展。
```
