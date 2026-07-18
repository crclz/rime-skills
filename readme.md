# rime-skills

本仓库以一种半黑盒的方式，让有技术小白也能0学习成本地安装rime输入法本体，以及rime-ice雾凇拼音。


## 前置依赖
- 必须：安装git
- 必须：有能访问github的工具。并且合理配置git的proxy端口，让git也能通过这个工具访问GitHub
- 可选：包管理器，例如Windows的winget


## 步骤

首先，在本仓库打开opencode/claudecode等类似工具(下文称为coding agent)

然后，可以按照以下流程运行如下几个skill `skill位于本仓库的 .agents/skills`


### skill: rime-install

告诉coding agent

> 使用rime-install skill帮我安装rime输入法


### skill: rime-ice-install

告诉coding agent

> 我已经安装完成了rime输入法。请使用rime-ice-install 帮我安装rime输入法的rime-ice方案


### skill: rime-configure

告诉coding agent

> 我已经完成了 rime-install 和 rime-ice-install，帮我使用rime-configure
