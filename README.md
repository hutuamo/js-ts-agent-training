# JS/TS AI Agent 工程训练营

这是一个面向 **JavaScript、TypeScript、Node.js 与 AI Agent 工程** 的分阶段训练体系，目标是帮助已经具备编程经验，尤其是有 C/C++ 背景的开发者，系统完成从基础到进阶的迁移。

它不是单纯的书单，也不是零散笔记，而是一个完整的训练系统。

## 目标

通过结构化路线，把一位有系统编程经验的开发者训练到能够独立完成 **JavaScript / TypeScript AI Agent 开发**，包括：

- **Stage 0**：环境与认知迁移
- **Stage 1**：JavaScript 基础
- **Stage 2**：TypeScript 基础
- **Stage 3**：Node.js 工程能力
- **Stage 4**：LLM 接入与工具调用基础
- **Stage 5**：Agent 核心系统设计
- **Stage 6**：检索、记忆与工作流
- **Stage 7**：生产化、评估与可靠性
- **Stage 8**：毕业项目与作品集级交付

## 适合谁

这个仓库特别适合下面这类人：

- 已经会编程，但刚进入 JavaScript / TypeScript 世界
- 有 C / C++ / Java / Go / Rust 等背景
- 想学 AI Agent 开发，而不是只学前端框架
- 更关注后端、CLI、自动化、工作流、工具调用与系统可靠性

## 仓库结构

- `00-foundations/`：环境、工具链、认知迁移
- `01-javascript/`：JavaScript 核心语言与运行时
- `02-typescript/`：TypeScript 核心与工程表达能力
- `03-nodejs/`：Node.js 后端、CLI 与自动化工程
- `04-llm-basics/`：模型 API、结构化输出、工具调用
- `05-agent-core/`：Agent loop、工具注册、状态与追踪
- `06-rag-memory-workflows/`：检索、记忆、工作流设计
- `07-production/`：评估、观测性、失败处理、部署
- `08-capstones/`：毕业项目与作品集级项目方向
- `resources/`：路线图、阅读映射、学习顺序、常见陷阱
- `templates/`：分阶段模板与最小骨架

## 使用方式

建议按阶段推进：

1. 阅读每个阶段的 `OVERVIEW.md`
2. 完成 `EXERCISES.md` 中的练习
3. 选择并完成 `PROJECTS.md` 中的项目
4. 用 `CHECKLIST.md` 判断自己是否可以进入下一阶段

## 推荐时长

- 快速路径：**10～12 周**
- 标准路径：**3～5 个月**
- 深入路径：**6 个月以上**

## 核心原则

1. **边学边做，不走纯阅读路线**
2. **优先后端 / CLI / Agent 工程，不以前端为主线**
3. **先理解运行时和边界，再谈框架和自动化**
4. **TypeScript 是工程约束层，不是炫技工具**
5. **Agent 是系统工程，不只是 prompt 技巧**
6. **可评估、可调试、可解释，比“偶尔跑通一次”更重要**

## 推荐书籍

主线书籍：

- JavaScript：*JavaScript 权威指南（第七版）*
- TypeScript：*Programming TypeScript*
- TypeScript 实践：*Effective TypeScript*
- Node.js 工程：*Node.js Design Patterns*

## 最终应达到的能力

完成本训练后，你应该能够：

- 从零创建一个 TypeScript 项目
- 接入模型 API 并完成结构化输出和工具调用
- 设计有状态、有工具边界的 Agent 系统
- 构建带检索能力的工作流
- 为系统增加日志、校验、重试与基础 eval
- 交付一个作品集级别的 AI Agent 项目

## 建议起点

先阅读：

- `resources/12-week-roadmap.md`
- `resources/study-order.md`
- `00-foundations/OVERVIEW.md`
