---
type: source-reading
status: initial
project: directus/directus
topic: Monorepo 结构
created: 2026-07-02
updated: 2026-07-02
---

# Directus - Monorepo 结构

项目主卡：[[01-projects/directus--directus|directus/directus]]
特点卡：[[03-patterns/framework-characteristics/directus|Directus 特点]]

## 阅读目标

先理解 Directus 的包边界。Directus 不是传统后台脚手架，而是数据库优先的 Admin / API / SDK 平台，所以必须从 monorepo 结构开始读。

## 已确认结构

| 目录 | 初步职责 |
| --- | --- |
| `api` | Directus API 服务 |
| `app` | 管理端 Admin App |
| `directus` | CLI / 主包入口 |
| `sdk` | TypeScript SDK |
| `packages` | 共享包、扩展能力、内部模块 |
| `tests` | 测试 |
| `pnpm-workspace.yaml` | workspace 包管理入口 |

## 初步判断

Directus 的核心范式是“数据库 + 元数据 + 权限 + Admin + API”。它和 [[03-patterns/framework-characteristics/payload|Payload]] 的区别很关键：

| 维度 | Directus | Payload |
| --- | --- | --- |
| 起点 | 现有数据库 schema | TypeScript 配置 |
| 管理端 | 根据元数据动态渲染 | 根据配置生成 |
| API | 数据库和权限驱动的即时 API | collection 配置驱动 API |

## 读源码时要验证的问题

- CLI 如何启动 `api` 服务。
- `api` 如何读取数据库 schema 和 metadata。
- `app` 如何根据 collections / fields / relations 渲染页面。
- `sdk` 如何封装 API 契约。
- `packages` 中哪些是核心抽象，哪些是扩展能力。

## Obsidian 关联

- 框架特点：[[03-patterns/framework-characteristics/directus|Directus 特点]]
- Payload 对照：[[02-reading-notes/payloadcms--payload/monorepo-structure|Payload - Monorepo 结构]]
- 平台对比：[[04-comparisons/database-first-admin-platforms|后台/CMS/API 平台对比]]

