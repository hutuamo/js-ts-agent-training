# 模板 - Stage 06 RAG Pipeline

## 目的

本模板是一个在有界语料库上支持检索的工作流或助手的启动蓝图。

它不是一个通用的向量搜索 demo。它是用于学习摄入、分块、检索检查和有据输出结构。

## 适用场景

- 技术笔记上的文档 QA
- 研究笔记本生成
- 事件或运维上下文查找
- 带来源依据的支持响应起草

## 构建目标

- 定义一个小型可检查语料库
- 实现摄入和元数据处理
- 让检索在生成前可检查
- 要求带来源参考的有据输出

## 建议文件树

```text
stage-06-rag-pipeline/
  README.md
  ARCHITECTURE.md
  TODO.md
  corpus/
  src/
    ingest.ts
    chunk.ts
    index.ts
    retrieve.ts
    answer.ts
    citations.ts
  eval/
    queries.json
```

## 最低接受标准

- 一个有界语料库
- 一个有文档记录且有理由的分块策略
- 一条检索检查路径
- 一条带引用的答案路径或显式拒绝
- 一个小型带标签查询集

## 扩展想法

- 对比两种分块策略
- 添加元数据过滤
- 添加工作流路径 vs 自由形式助手对比
- 添加简单检索质量指标
