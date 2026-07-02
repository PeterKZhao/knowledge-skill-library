---
type: practice-lab
project: zhijiantianya/yudao-cloud
status: todo
created: 2026-07-01
updated: 2026-07-01
---

# yudao-cloud - 本地运行实验

## 目标

- clone 仓库。
- 确认分支和运行环境。
- 跑通 Nacos、Redis、数据库等基础依赖。
- 跑通 `yudao-gateway`。
- 跑通至少一个后端业务服务。
- 跑通管理端前端。
- 记录 Gateway 到业务服务的第一条完整请求链路。

## 待确认环境

| 项 | 内容 |
| --- | --- |
| OS | Windows |
| 分支 | 待确认：`master` / `master-jdk17` / `master-jdk25` |
| JDK | 待确认 |
| Maven | 待确认 |
| Node | 待确认 |
| 数据库 | 待确认 |
| Redis | 待确认 |
| Nacos | 待确认 |
| Seata | 待确认 |
| Sentinel | 待确认 |
| XXL-Job | 待确认 |
| MQ | 待确认是否必须 |

## 操作记录

```bash
# 待实际执行后补充
git clone https://gitee.com/zhijiantianya/yudao-cloud.git
```

## 验证标准

- [ ] Nacos 控制台可访问，服务注册正常。
- [ ] 数据库初始化脚本执行成功。
- [ ] Redis 连接成功。
- [ ] `yudao-gateway` 启动成功。
- [ ] 至少一个业务服务启动成功。
- [ ] 管理端登录页可访问。
- [ ] 登录请求能经过 Gateway 并到达后端服务。
- [ ] 能定位一个菜单对应的前后端代码路径。

## 问题记录

| 问题 | 原因 | 解决 |
| --- | --- | --- |
|  |  |  |

