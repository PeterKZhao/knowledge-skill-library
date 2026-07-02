---
type: pattern-index
status: draft
created: 2026-07-02
updated: 2026-07-02
---

# 框架特点总览

这个目录用于快速理解当前知识库已收录框架的核心特点。每张卡片回答三个问题：

- 这个框架最突出的特点是什么？
- 适合学习什么能力？
- 不适合把它误解成什么？

## 后端 / 后台平台

| 框架 | 核心特点 | 适合学习 | 特点卡 |
| --- | --- | --- | --- |
| RuoYi/Yudao | 国内 Java 企业后台和业务中台样本 | RBAC、多租户、代码生成、业务模块化 | [[03-patterns/framework-characteristics/ruoyi-vue-pro|RuoYi/Yudao 特点]] |
| Yudao Cloud | Yudao 体系的 Spring Cloud 微服务版本 | Gateway、Nacos、服务治理、分布式组件 | [[03-patterns/framework-characteristics/yudao-cloud|Yudao Cloud 特点]] |
| ERPNext | 基于 Frappe 的完整 ERP 业务套件 | DocType、业务单据、账务和库存闭环 | [[03-patterns/framework-characteristics/erpnext|ERPNext 特点]] |
| gin-vue-admin | Go + Vue 前后端分离后台脚手架 | Gin、GORM、Casbin、JWT、代码生成 | [[03-patterns/framework-characteristics/gin-vue-admin|gin-vue-admin 特点]] |
| JeecgBoot | Java AI 低代码 / 零代码后台平台 | 在线表单、报表、流程、代码生成、AI Skills | [[03-patterns/framework-characteristics/jeecgboot|JeecgBoot 特点]] |
| Directus | 数据库优先 Headless CMS / Admin / API 平台 | 元数据、权限、即时 API、Admin App | [[03-patterns/framework-characteristics/directus|Directus 特点]] |
| Payload | TypeScript / Next.js 全栈后台与 CMS 框架 | Collection 配置、Admin Panel、插件、数据库适配 | [[03-patterns/framework-characteristics/payload|Payload 特点]] |

## 前端后台框架

| 框架 | 核心特点 | 适合学习 | 特点卡 |
| --- | --- | --- | --- |
| yudao-ui-admin-vue3 | Yudao 单应用 Vue3 管理端 | 业务页面组织、权限路由、Element Plus 后台页面 | [[03-patterns/framework-characteristics/yudao-ui-admin-vue3|yudao-ui-admin-vue3 特点]] |
| yudao-ui-admin-vben | 基于 Vben Admin 5 的平台化前端底座 | monorepo、多 UI app、共享 packages、偏好配置 | [[03-patterns/framework-characteristics/yudao-ui-admin-vben|yudao-ui-admin-vben 特点]] |

## 快速选择

| 目标 | 优先看 |
| --- | --- |
| 学国内 Java 常规企业后台 | [[03-patterns/framework-characteristics/ruoyi-vue-pro|RuoYi/Yudao]] |
| 学 Java 微服务后台 | [[03-patterns/framework-characteristics/yudao-cloud|Yudao Cloud]] |
| 学 Java 低代码平台 | [[03-patterns/framework-characteristics/jeecgboot|JeecgBoot]] |
| 学 Go 后台脚手架 | [[03-patterns/framework-characteristics/gin-vue-admin|gin-vue-admin]] |
| 学完整 ERP 业务系统 | [[03-patterns/framework-characteristics/erpnext|ERPNext]] |
| 已有数据库要快速变后台/API | [[03-patterns/framework-characteristics/directus|Directus]] |
| TypeScript / Next.js 项目要内嵌后台和 CMS | [[03-patterns/framework-characteristics/payload|Payload]] |
| 快速二开 Yudao 管理端页面 | [[03-patterns/framework-characteristics/yudao-ui-admin-vue3|yudao-ui-admin-vue3]] |
| 评估长期后台前端平台底座 | [[03-patterns/framework-characteristics/yudao-ui-admin-vben|yudao-ui-admin-vben]] |

