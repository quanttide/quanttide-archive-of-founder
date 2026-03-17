# Journal - 工作日志

默认神经网络模式下，以碎片化的格式收集想法并记录，用于后续深入挖掘。

## 流程概览

| 步骤 | 输入 | 输出 |
|------|------|------|
| 1. 读取原始文件 | `raw/YYYY-MM-DD_N.md` | 原始文本 |
| 2. 清洗 | 原始文本 | `diary/YYYY-MM-DD.md` |
| 3. 提炼 | 原始文本 | `memory/event/YYYY-MM-DD.jsonl` |

## 目录结构

| 类型 | 路径 |
|------|------|
| 原始日志 | `default/raw/YYYY-MM-DD_N.md` |
| 清洗后日记 | `default/journal/diary/YYYY-MM-DD.md` |
| 事件记忆 | `default/memory/event/YYYY-MM-DD.jsonl` |
| 已处理归档 | `default/raw/archive/` |

## 相关文档

- [清洗](./clean.md)：将原始日志清洗为可读日记
- [提炼](./refine.md)：从原始日志提取事件记忆
