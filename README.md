# fyj1233

2026 届 · 求职方向：AI 应用 / Agent 开发 · 意向城市：武汉

主要写 Python 后端，最近在把大模型接进真实业务流程里——让 AI 提数、查账、写报告，同时把数字牢牢锁在数据库这一侧。

## 代表项目 · 一纸成账 Paper2Ledger

**[→ 仓库地址：fyj1233/paper2ledger-ai](https://github.com/fyj1233/paper2ledger-ai)**

把中小型工厂手写的生产日报、出货单、退货记录、盘点表、小票照片，自动变成能查能算的台账。

- **三级提取兜底**：模板正则 → 大模型 → 内置规则，每条结果都带来源标记与置信度，可回溯到原文证据；没配 API Key 时全程走规则模式，流程照常可用。
- **台账问答智能体**：LangGraph 自主调用 8 个查询工具，会话记忆持久化，切页不丢上下文。
- **AI 不编数字**：周报 / 月报的卡片与图表数据全部由后端 SQL 算好落库，大模型只负责写文字分析。
- **主备双模型自动降级**：主服务商超时、报错或欠费时自动切备用重试一次，无需人工干预。
- **本地离线 OCR**：不联网也能识别小票照片；配套每日自动备份与跨机还原脚本。
- **权限与安全**：三级 RBAC、JWT + bcrypt、操作审计日志、首次登录服务端强制改密。

| 生产看板 | AI 台账问答 |
| --- | --- |
| ![生产看板](https://raw.githubusercontent.com/fyj1233/paper2ledger-ai/main/docs/images/02-dashboard.png) | ![AI 台账问答](https://raw.githubusercontent.com/fyj1233/paper2ledger-ai/main/docs/images/05-assistant.png) |

技术栈：FastAPI · SQLAlchemy 2 · SQLite · LangGraph · Vue 3 · Vite · Element Plus · Docker

规模：后端 45 个 Python 文件 / 约 5,100 行，前端约 4,500 行；98 项冒烟回归可离线运行，不依赖真实 Key。

## 其他项目

- [portal-game-demo](https://github.com/fyj1233/portal-game-demo) — Three.js 网页版「传送门」玩法：双门动量守恒、全表面放门、Render-to-Texture 实时透视、5 个解谜关卡，完全离线自包含。
- [biyesheji](https://github.com/fyj1233/biyesheji) — Django 校园学习资源共享平台：资料上传去重、AI 摘要与标签生成、积分 / 评论 / 推荐。

## 现在在做什么

刷算法题、补计算机基础，同时继续深挖 Agent 工程这条线：提取链路的成本与确定性怎么权衡、怎么从架构上防止模型编数据、主备降级怎么做到不断链。

## 联系我

直接开 [issue](https://github.com/fyj1233/paper2ledger-ai/issues) 最方便。
