# Journal - 提炼

从清洗后的日记中提取结构化的事件记忆。

## 前提

先完成 [清洗](./clean.md) 步骤，获得清洗后的日记。

## 步骤

### 步骤 1：读取清洗后的日记

从 `default/journal/` 读取当天清洗后的日记。

文件命名格式：`YYYY-MM-DD.md`

示例：`2026-03-12.md`

### 步骤 2：提取事件记忆

使用 AI 从清洗后的日记中提取事件。

**Prompt**：

```
这是清洗后的日记，我们现在要提取其中的事件记忆

定义 Event 模型：
- id: uuid
- title: str
- description: str
```

**输出格式**：JSONL（每行一个 JSON 对象）

### 步骤 3：保存文件

保存到 `default/memory/episode/YYYY-MM-DD.jsonl`

## EpisodicMemory 模型

```json
{
  "id": "uuid",
  "title": "string",
  "description": "string",
  "tense": "past | present | future",
  "type": "decision | plan | report | evaluation | retrospective"
}
```

### `tense` 枚举值
- **`past`**：过去发生的事件，用于回顾、总结、复盘。
- **`present`**：当前正在发生或刚刚发生的事件。
- **`future`**：计划中或预期发生的事件，用于规划、目标设定。

### `type` 枚举值
- **`decision`**：做出的决策，记录决策背景和理由。
- **`plan`**：制定的计划，包含步骤、时间安排等。
- **`report`**：工作汇报或阶段性总结。
- **`evaluation`**：对某个事物、工具或自身的评估和反思。
- **`retrospective`**：对过去一段时间的回顾，提炼经验教训。

## 示例

### 清洗后日记

```markdown
# 2026-03-12

今天梳理了几个关于工作方式和工具链的想法，记录一下。

文档体系调整

手机端写东西越来越频繁，发现用 essay 的形式比 handbook 顺手多了。essay 更适合倾诉和捕捉灵感，不需要太正式；而 handbook 还是应该作为团队的正式参考文档，保持结构化和权威性。

另外，bylaws 也可以开始动笔了。规章制度需要给团队清晰的示范。

工作流与技术配置

一直在想怎么打通内部知识库和外部代码仓库。理想的工作流是：在本地把飞书知识库的数据同步下来，同时拉取 GitHub 仓库，然后半自动化编辑内容，最后让 AI 帮忙自动提交 PR。

今天就记这些，明天继续推进。
```

### 事件记忆（JSONL）

```json
{"id": "550e8400-e29b-41d4-a716-446655440000", "title": "文档策略调整", "description": "手机端用 essay 代替 handbook，essay 更适合倾诉和灵感记录，handbook 作为团队正式参考文档。", "tense": "past", "type": "decision"}
{"id": "550e8400-e29b-41d4-a716-446655440001", "title": "bylaws 编写启动", "description": "计划逐步编写 bylaws，为团队提供清晰的行为准则和操作示范。", "tense": "future", "type": "plan"}
{"id": "550e8400-e29b-41d4-a716-446655440002", "title": "飞书 GitHub 工作流", "description": "打通飞书知识库和 GitHub 仓库，半自动化编辑，AI 自动提交 PR。", "tense": "future", "type": "plan"}
```
