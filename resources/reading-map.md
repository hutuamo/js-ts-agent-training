# 阅读地图

## 目的

这份文件把书籍、官方文档和补充资料映射到本仓库的各个阶段中。

默认读者已经会编程，可能有较强的 C / C++ 系统语言习惯，希望高效进入 JavaScript / TypeScript 后端与 AI Agent 工程。

目标不是把资料全看完，而是在每个阶段读到足够支撑构建和调试的程度。

## 阅读原则

- 每一层优先保留一个主资料源，然后立刻进入实践。
- 官方文档是权威参考，但不应该是唯一学习方式。
- 阅读最好服务于当前阶段项目，而不是脱离项目空读。
- 如果一章内容不影响你怎么写、怎么调试，就可以推迟。

## Stage 00 - Foundations

### 主资料
- Node.js 官方文档：入门、模块、process 基础
- MDN JavaScript 指南：概览级刷新

### 为什么重要
这个阶段的主要任务，是修正你对运行时、包管理、模块和工具链的错误预期。

### C/C++ 迁移重点
- 运行时程序与已编译二进制的差异
- 包管理和生态习惯
- 异步模型差异
- 模块与项目结构约定

### 读到什么程度就够
- 能自信搭好工具链
- 能运行并观察一个小型 CLI
- 能用工程视角解释 event loop

## Stage 01 - JavaScript

### 主资料
- *JavaScript 权威指南（第七版）*：主线书
- MDN 文档：写代码时随查随用
- *You Don’t Know JS Yet*：可选，用于补语言机制理解

### 重点内容
- 值与类型转换
- 函数、闭包、作用域
- 对象和数组
- 原型的实用理解
- 模块
- 错误处理
- Promise 和 async/await

### 可略读内容
- 与后端 / CLI 无关的重浏览器章节

### C/C++ 迁移重点
- 动态类型与运行时转换
- 对象模型和 class-first 思维的差异
- 闭包和函数式模式
- 异步思维

## Stage 02 - TypeScript

### 主资料
- *Programming TypeScript*：主书
- TypeScript Handbook：权威语法和特性参考
- *Effective TypeScript*：最佳实践与坑点

### 重点内容
- 类型标注与推导
- 对象与函数类型
- union 与 narrowing
- 面向普通工程的泛型
- strict mode 和 tsconfig
- 运行时校验边界思维

### 应延后内容
- 高级类型体操
- 对项目实际收益不大的炫技型类型设计

### C/C++ 迁移重点
- 结构化类型
- 编译期帮助与运行时真相的差别
- 什么时候类型在帮你，什么时候它只是在制造噪音

## Stage 03 - Node.js

### 主资料
- *Node.js Design Patterns*：主工程书
- Node.js 官方文档：fs、path、process、streams、child_process、fetch/http

### 重点内容
- 文件与路径
- 配置与环境变量
- 重试、超时与外部 I/O 失败
- 流与缓冲
- 子进程集成
- 包结构、CLI 与服务结构

### C/C++ 迁移重点
- 在高层运行时里保持工程纪律
- 事件驱动 I/O 与并发模式
- 从 Node 驱动 shell / 外部工具

## Stage 04 - LLM Basics

### 主资料
- 一个模型提供商的 SDK / 文档路径
- 你选定提供商的结构化输出与工具调用官方文档
- 提供商错误处理、限流与速率限制文档

### 重点内容
- 请求 / 响应生命周期
- prompt 契约
- 结构化输出
- streaming 取舍
- 工具调用 roundtrip
- token 与延迟意识

### 不要做的事
- 同时研究 5 家 provider
- 看很多没有落地实现细节的 prompt 工程文章

### C/C++ 迁移重点
- 在确定性系统中接入概率型子系统
- 在模型边界做严格验证
- 用日志和保存样例作为调试手段

## Stage 05 - Agent Core

### 主资料
- 你自己在 Stage 04 里积累的项目笔记与 trace
- 少量关于工具编排、评估和 system design 的材料
- 框架文档应放在你能手写 loop 之后再看

### 重点内容
- loop 结构
- 状态边界
- 工具注册表设计
- planning 与 direct execution 的取舍
- trace 与 guardrails

### 不要做的事
- 先学框架，再理解系统结构
- 看大量抽象“agent 哲学”而没有系统后果

## Stage 06 - RAG / Memory / Workflows

### 主资料
- 只按需要阅读向量检索 / 检索框架文档
- 少量关于 chunking、retrieval eval、citation grounding 的材料
- 你自己实验积累的检索结果与失败案例

### 重点内容
- 数据导入
- chunking 与 metadata
- retrieval inspection
- grounded output
- memory policy
- workflow 与 autonomy 的边界

### 不要做的事
- 在没定义 corpus 质量前就上向量检索
- 把“记忆”当营销词，而不是保留状态

## Stage 07 - Production

### 主资料
- *Designing Data-Intensive Applications*：选择性阅读，用于长期系统思维
- *Designing Machine Learning Systems*：选择性阅读，用于生产 AI 系统视角
- provider 关于 rate limit、重试与运营的文档

### 重点内容
- 校验与契约
- 可观测性
- 重试、回退与降级
- eval 与回归测试
- 密钥与数据处理
- 部署形态和 operator note

### 不要做的事
- 只读系统书，不在自己的项目上做加固

## Stage 08 - Capstones

### 主资料
- 你自己的项目文档和阶段笔记
- 可对照的开源项目，带批判性阅读
- 你所采用部署方式的文档

### 重点内容
- 架构一致性
- 评估与证明能力
- 限制、范围和文档质量

## 最小有效阅读组合

如果你想走最短可用路线，保留这些就够了：

- *JavaScript 权威指南（第七版）*
- *Programming TypeScript*
- *Effective TypeScript*
- *Node.js Design Patterns*
- TypeScript Handbook
- Node.js 官方文档
- 一个模型提供商的 SDK / API 文档

## 给 C/C++ 工程师的建议

- 不要试图用 TypeScript 的复杂技巧去复制原生语言的确定感。
- 先掌握运行时和生态约定，再考虑优化它们。
- 优先写朴素、清楚的后端代码，而不是追求“看起来很高级”。
- 前端相关阅读不要进入主线，除非你的 capstone 确实需要。
- 读到足够能写下一步代码，就停下来开始构建。
