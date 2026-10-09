# Issue tracker: GitHub

- Issue 仓库：sixpence6/Agents。
- 工作看板：sixpence6 的 Project #3，名称 Agents。
- 问题和规格以仓库 Issue 为准；看板用于跟踪工作。
- 使用 gh CLI；Issue 命令显式传入 --repo sixpence6/Agents。

## 常用操作

- 创建：
  gh issue create --repo sixpence6/Agents --title "..." --body "..."
  多行正文使用 --body-file <正文文件>。

- 读取：
  gh issue view <number> --repo sixpence6/Agents
  --json number,title,body,labels,comments

- 列表：
  gh issue list --repo sixpence6/Agents --state open
  --json number,title,body,labels,comments
  按任务需要增加 --label、--state 和 --limit。

- 评论：
  gh issue comment <number> --repo sixpence6/Agents --body "..."

- 添加或移除标签：
  gh issue edit <number> --repo sixpence6/Agents --add-label "..."
  gh issue edit <number> --repo sixpence6/Agents --remove-label "..."

- 关闭：
  gh issue close <number> --repo sixpence6/Agents --comment "..."

以上换行仅用于排版，每条命令执行时合并为一行。

## 加入工作看板

创建 Issue 后，将返回的 Issue URL 加入看板：
gh project item-add 3 --owner sixpence6 --url <issue-url>

如果加入看板失败，保留已创建的 Issue，只重试关联操作，
不要重复创建 Issue。

## Pull requests as a triage surface

PRs as a request surface: no.

## Skill 操作映射

- “publish to the issue tracker”：创建仓库 Issue，再加入看板。
- “fetch the relevant ticket”：读取对应 Issue 的正文、标签和评论。

## Wayfinding

- Map：使用 wayfinder:map 标签的 Issue，
  正文包含 Notes、Decisions-so-far 和 Fog。
- 子任务：使用 wayfinder:research、wayfinder:prototype、
  wayfinder:grilling 或 wayfinder:task 标签。
  创建时使用 --parent <map-number> 关联父 Issue。
- 阻塞：优先使用原生依赖，通过 gh issue edit 的
  --add-blocked-by 建立关系。
  无法使用原生关系时，在正文记录 Part of #<parent>
  和 Blocked by: #<number>。
- Frontier：按 Map 顺序选择未关闭、无未关闭阻塞且未被认领的任务。
- 认领：gh issue edit <number> --repo sixpence6/Agents
  --add-assignee "@me"。
- 解决：评论结论并关闭任务，将结论摘要和链接补入 Map。
- 使用额外标签前，检查是否存在，只补建缺失标签。
