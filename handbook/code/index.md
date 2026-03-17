# 编程

## 原则

交付物：无论谁怎么操作，最终我们想要什么？持续交付假设。

工作流：
1. 意图分类：这是什么任务？设计、开发、维护
2. 状态维护：交付物从什么状态到什么状态？

每次编程的 owner-reviewer 模型
1. write code
2.  review with other tools without context。确保不会因为工具盲区和上下文盲区导致问题。

每次编程要想清楚输入和输出，过程交给 AI 自己设计，可以有个大概的想法、写完以后要清楚。 

## 模式

review命令：主要作用是检查提交，这对写 commit message 很有帮助。每轮编程先自由发挥，然后使用opencode的review命令，然后再提交。不知道 opencode 触发提交的时候会不会自己用 review 命令，如果是这样的话就比较优雅了。

## 工具

先cli再IDE。IDE主要看结果。

Codex的模型能力和交互友好度高于opencode。

opencode 的透明度稍低，在 zed 里看不出来实际进行了什么操作，只有摘要。可能会出现疏漏，要特别注意人工检查。

Zed+Opencode 适合做一些稍简单和明确的开发任务。

Opencode 智商不够处理复杂问题，比如安装 Gemini 或者 Openclaw。codex 可以。

Gemini 使用 Google AI Studio 获取 API key，Oauth 登录会被拦截国家。Gemini 的额度似乎也比较有限。

openclaw 较为复杂，建议使用 code cli 操作，手动操作得慢慢扒文档。

## 提交

比如，丢了些本该提交到云端的 meta 的更新。不过影响没有特别大，只是感觉要特别注意一小段小段整理。

人的核心分工是会维护会用，AI 的执行力是不稀缺的，丢了错了都可以尽快重来。这是很不一样的一个设计原则，云原生的粒度更低了，从版本到了 commit 甚至每次编辑的级别，得把云原生的习惯更多拉到 Vibe coding。

## 内容

docs/default：收集流
1. 收集：和AI聊天，让AI写笔记记录。docs/default/default 是默认模式的默认模式。
2. 整理：在 default内部整理
3. 提取：
4. 表达：离开 default 区域。
这个区域空白的时候就可以进行一次发布了，说明一段时间的想法暂时处理完了，可以停顿一下进行下一次。

docs/meta：元认知流
1. 收集：docs/default/meta 移动到 docs/meta/default，从收集进入元认知流。也可以 docs/default 生成 docs/meta/docs/default。
 
 
examples：示例
不要创建完整项目，一个一个模块独立实现，以验证想法和对齐认知为主。
 
 
Agents.md

这个文档可以作为AI学习的主要经验。当AI和人的理解不符的时候，就可以塞一个文档进去让 AI 改进。

产生新经验的方法：当 AI 出问题的时候，问 AI 为什么错了，怎么改。然后给记录到 Agent.md 里。


## 密钥

目前只能一个一个平台收集。未来考虑逐步变成一个平台统一收集管理。