# 模板 - Stage 04 结构化输出 CLI

## 目的

本模板是一个 CLI 的启动蓝图，该 CLI 向模型发送一个有界任务并期望经过校验的结构化输出。

有意采用文档优先的方式。你应该作为训练的一部分自己构建实现。

## 适用场景

- 从会议记录中提取任务
- 将 issue 报告分类到严格 schema
- 把粗糙的研究笔记转换成结构化摘要
- 将运维文本正规化为带类型字段

## 构建目标

- 保持模型包装器小巧
- 为接受的输出定义一个显式 schema
- 在写入或打印最终结果之前做校验
- 保存案例用于后续回归

## 建议文件树

```text
stage-04-structured-output-cli/
  README.md
  ARCHITECTURE.md
  TODO.md
  src/
    cli.ts
    config.ts
    model.ts
    prompt.ts
    schema.ts
    run.ts
  examples/
    inputs/
    outputs/
```

## 最低接受标准

- 一个命令行入口点
- 一个模型支撑的任务
- 一个经过校验的输出 schema
- 一条无效输出处理路径
- 为至少三个代表性输入保存的案例

## 扩展想法

- 添加缓冲 vs 流式对比
- 添加 prompt 修订笔记
- 添加延迟和 token 观察日志
- 添加一个小型回归运行器，运行保存的案例
