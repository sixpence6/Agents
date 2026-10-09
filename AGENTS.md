# 项目约定

- 遇到不知道的知识去联网搜索。
- 动手前先思考。
- 若用户中途打断，停止旧任务，只执行用户最新的 prompt。
- 问的问题不要过于发散、细分。
- 使用 skills 时，先读取并纳入其完整规则。
- 遵循《代码整洁之道》：函数命名清晰，变量命名有意义，
  避免魔法数字和硬编码。
- 上传范围限定为本工程目录。提交前检查文件清单，
  排除密钥、凭据和其他敏感信息。

## Agent skills

### Issue tracker

问题和规格记录在 sixpence6/Agents 的 GitHub Issues。
创建或读取任务前，阅读 docs/agents/issue-tracker.md。

### Triage labels

使用五个默认 triage 标签。
分类或调整任务状态前，阅读 docs/agents/triage-labels.md。

### Domain docs

采用 single-context 布局。
探索代码或讨论领域术语、架构决策前，阅读 docs/agents/domain.md。
