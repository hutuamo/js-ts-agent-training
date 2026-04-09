# 模板 - Stage 05 工具注册表 Agent

## 目的

本模板是一个具有可见循环和受控工具注册表的小型 agent 启动蓝图。

重点不是建造一个通用助手。重点是让工具使用、状态和停止条件显式化。

## 适用场景

- 有界研究助手
- 本地仓库检查助手
- 运维摘要助手
- 带一两个动态选择的小型多步工作流

## 构建目标

- 定义一个带校验参数的小工具注册表
- 保持循环状态显式和可检查
- 为每步添加 trace 日志
- 强制停止条件和上报路径

## 建议文件树

```text
stage-05-tool-registry-agent/
  README.md
  ARCHITECTURE.md
  TODO.md
  src/
    agent.ts
    loop.ts
    state.ts
    tools/
      index.ts
      tool-a.ts
      tool-b.ts
    trace.ts
    stop-rules.ts
```

## 最低接受标准

- 至少两个带显式契约的工具
- 一个带步骤计数和终止原因的循环
- 一种保存的 trace 格式
- 一条无效工具请求路径
- 一条人工交接或拒绝路径

## 扩展想法

- 规划 vs 直接执行对比
- 工具副作用分类
- Trace 查看器或 trace 摘要器
- 基于场景的循环评估
