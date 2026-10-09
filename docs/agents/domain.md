# Domain Docs

## 布局

采用 single-context：
- 工程根目录的 GLOSSARY.md：领域词汇表。
- docs/adr/：架构决策记录。

## 阅读规则

探索代码前，读取已有的 GLOSSARY.md，
并阅读与当前工作相关的 ADR。

文档不存在时直接继续，不主动补建空文件。
由 domain-modeling skill 在术语或决策明确后按需创建。

## 术语规则

Issue 标题、设计讨论、代码和测试中的领域概念，
使用词汇表定义的名称。

发现真实的术语缺口时，记录供 domain-modeling 处理。

## 决策冲突

方案与现有 ADR 冲突时，明确指出对应 ADR 及重新讨论的理由，
不要静默覆盖已有决策。
