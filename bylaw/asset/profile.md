# Profile 维护章程

本文件定义 quanttide-founder 仓库中 `meta/profile/` 目录的维护规范和流程。

## 维护流程

### 步骤 1: 从 journal 收集事件记忆

**目标**：从 `meta/report/` 目录的日志文件中提取事件记忆，收集到 `meta/profile/default.md`

**操作流程**：
1. 遍历 `meta/report/` 目录下的所有日志文件
2. 提取每个日志文件的"事件记忆"部分
3. 将提取的内容追加到 `meta/profile/default.md`

**示例**：
```markdown
# 事件记忆收集

## 2026-03-17

### 元数据重构任务
- 将 `meta/IDENTITY.md` 中的 Release 信息移到 `meta/profile/release.md`
- ...

## 2026-03-16

### 子模块管理
- 添加 paper 子模块（工作论文）
- ...
```

### 步骤 2: 分类整理到其他文件

**目标**：将 `meta/profile/default.md` 中的内容分类整理到对应的文件

**分类规则**：

| 内容类型 | 目标文件 | 整理内容 |
|---------|---------|---------|
| 仓库结构规范 | `repo.md` | 元数据重构原则、文件职责分离 |
| 版本管理流程 | `release.md` | Release 流程规范、版本控制原则 |
| 记忆建模知识 | `memory.md` | 日志编写规范、知识管理原则 |
| 子模块工作流 | `submodule.md` | 工作流程优化、子模块分类原则 |

**操作流程**：
1. 分析 `default.md` 中的每个章节
2. 根据内容性质选择目标文件
3. 将内容移动到目标文件
4. 从 `default.md` 中删除已移动的内容

### 步骤 3: 清理 default.md

**检查条件**：
- 如果 `default.md` 被清空（无内容或只有标题），则移除文件
- 如果 `default.md` 还有未分类的信息，则保留并通知用户

**操作流程**：
1. 检查 `default.md` 文件内容
2. 如果为空或只有标题：
   - 删除 `meta/profile/default.md`
   - 提交删除操作
3. 如果还有内容：
   - 保留文件
   - 通知用户："meta/profile/default.md 还有未分类的信息，请检查"

## 文件职责规范

### meta/profile/repo.md
- 仓库结构规范
- 元数据管理原则
- 文件职责分离

### meta/profile/release.md
- Release 列表
- 版本管理流程
- 版本控制原则

### meta/profile/memory.md
- 记忆建模知识
- 日志管理规范
- 元数据规范

### meta/profile/submodule.md
- 子模块列表
- 子模块分类原则
- 工作流程优化

### meta/profile/default.md
- 临时收集的事件记忆
- 待分类的信息
- 分类完成后应清空或删除

## 检查清单

### 收集阶段
- [ ] 遍历所有 journal 文件
- [ ] 提取事件记忆部分
- [ ] 追加到 default.md

### 分类阶段
- [ ] 分析内容性质
- [ ] 选择目标文件
- [ ] 移动内容到目标文件
- [ ] 从 default.md 删除已移动内容

### 清理阶段
- [ ] 检查 default.md 内容
- [ ] 如果为空则删除文件
- [ ] 如果有内容则通知用户

## 错误处理

### 错误 1: journal 文件不存在
**处理**：跳过该文件，继续处理其他文件

### 错误 2: 目标文件不存在
**处理**：创建目标文件，然后移动内容

### 错误 3: 内容分类不明确
**处理**：保留在 default.md，标记为"待分类"

## 参考文件
- `meta/bylaw/report.md`：日志规范
- `meta/profile/repo.md`：仓库结构
- `meta/profile/release.md`：版本管理
- `meta/profile/memory.md`：记忆建模
- `meta/profile/submodule.md`：子模块管理
