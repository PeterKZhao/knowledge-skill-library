---
type: source-reading
status: initial
project: flipped-aurora/gin-vue-admin
topic: Go 后端项目结构
created: 2026-07-02
updated: 2026-07-02
---

# gin-vue-admin - Go 后端项目结构

项目主卡：[[01-projects/flipped-aurora--gin-vue-admin|flipped-aurora/gin-vue-admin]]
特点卡：[[03-patterns/framework-characteristics/gin-vue-admin|gin-vue-admin 特点]]

## 阅读目标

先建立 Go 后端目录地图，理解 Gin / GORM / Casbin / JWT 在后台脚手架中的落点，再继续追启动链路和权限链路。

## 已确认结构

`server/` 是后端主目录：

| 目录 / 文件 | 初步职责 |
| --- | --- |
| `main.go` | 后端启动入口 |
| `core` | 配置、日志、服务启动等核心初始化 |
| `initialize` | 数据库、路由、定时任务、表注册等初始化 |
| `global` | 全局对象和配置 |
| `config` | 配置结构 |
| `router` | Gin 路由注册 |
| `middleware` | JWT、Casbin、跨域、日志等中间件 |
| `model` | GORM 模型 |
| `service` | 业务服务 |
| `api` | HTTP API 层 |
| `mcp` | AI / MCP 辅助能力相关入口 |

## 初步判断

`gin-vue-admin` 的目录分层比 Java 后台轻，但边界清楚：

- `api` 接收 HTTP 请求。
- `service` 承载业务逻辑。
- `model` 对应数据模型。
- `router` 将模块 API 注册到 Gin。
- `middleware` 统一处理认证、权限和横切逻辑。

这很适合和 [[02-reading-notes/zhijiantianya--ruoyi-vue-pro/maven-module-structure|ruoyi-vue-pro Maven 多模块结构]] 对照：一个是 Go 的轻量分层，一个是 Java 的多模块分层。

## 读源码时要验证的问题

- `main.go` 到 `core.RunServer()` 的完整调用链。
- 路由是按模块手动注册，还是通过代码生成器生成。
- JWT 和 Casbin 中间件的执行顺序。
- `model`、`request`、`response` 的结构如何组织。
- 代码生成器如何生成 api / router / service / model / web 页面。

## Obsidian 关联

- 框架特点：[[03-patterns/framework-characteristics/gin-vue-admin|gin-vue-admin 特点]]
- 后台脚手架对比：[[04-comparisons/admin-scaffold-comparison|后台脚手架对比]]
- 一对一对比：[[04-comparisons/pairwise-backend-comparisons|后端项目一对一对比]]

