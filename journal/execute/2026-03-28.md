# 2026-03-28 执行日志

## 收集

重构thera+实现qtadmin-cli：
- [x] 使用typer优化cli表现。和AI确认这是否为最佳实践。
- [x] 砍掉所有用不着的命令，发布0.2.0
- [ ] 照着抄一遍qtadmin-cli

src/thera/src/thera
src/qtadmin/src/cli/ROADMAP.md

## 加工

thera refresh 命令 -> qtadmin meta refresh命令
等到thera refresh稳定以后移除。
cli还是空的，要创建一个python项目才可以继续写。

## 整理

目标：src/qtadmin/src/cli/ROADMAP.md

待办：
- [ ] qtadmin-cli初始化Python项目。
- [ ] 实现命令。

参考阅读：
- src/thera/src/thera

工作资源：
- src/qtadmin/src/cli


## 执行

qtadmin-cli初始化Python项目。
- [x] 使用Opencode和Zed直接接收和处理这个工作。
这个事情很简单。只是需要讨论一下模块设计思路。
- [x] cli.py或__main__.py哪个更合适做入口模块？
保留cli.py，遵循click和typer的事实标准。

thera refresh 命令 -> qtadmin meta refresh命令
- [x] 开发者文档写到src/qtadmin/src/cli/docs/dev/meta_refresh.md
超额完成任务，顺便把代码也写了。
- [x] 用户文档写到src/qtadmin/src/cli/docs/user/meta_refresh.md
- [x] 测试写到src/qtadmin/src/cli/tests

都写在cli模块太拥挤了，未来不容易加第二个命令。采取雪花编程法的思想，从主干中不断提取分支。正好使用刚才生成的文档和测试验证重构可用性。
- [x] 分离cli.py出来一个meta/refresh.py

可以开始安在本地使用了。先发布一个alpha版本。qtadmin有provider, studio, cli三个项目，标签和版本发布规范要在现有基础上修改。
- [x] cli项目的发布规范是什么？
在同一个仓库里标签规范为`cli/v0.0.1`。验证符合社区习惯。
- [x] 更新到src/qtadmin/CONTRIBUTING.md
修改了原文中错误的地方。
- [x] 发布`cli/v0.0.1-alpha.1`，安装到本地。

## 反思

### 元执行

清晰地列举所需资源到可以直接和OpenCode待办清单对其的程度是可以最大化地提高执行效率和可控性的。

### 模块命名

cli项目选择cli是尊重我们使用的typer库的命名习惯。
类似的，provider项目遵循FastAPI官方文档的命名习惯也类似。
这样可以最大限度减少团队协作和人机协作的摩擦。

### 发布命名

单仓标签为`<app>/<version>`，如`cli/v0.0.1`。
