---
name: rime-ice-install
description: (在安装完rime后)帮助用户安装rime-ice(雾凇拼音方案)的向导
---

请遵循准则skill: rime-guide-standard

## 前置依赖

首先需向用户确认，用户已经安装了 rime 本体（如果用户显式告诉你了就行；否则需要主动询问）

确认bash可用: 后面会需要用到bash. 如果是Windows，确保你测试过git bash的运行方式（如果不行则向用户说明，需要他自己去安装git）


## 阅读最新安装流程

阅读: https://raw.githubusercontent.com/iDvel/rime-ice/refs/heads/main/others/docs/Installation.md

优先使用上面链接中的 东风破 plum + bash 方式 进行安装.

注意优先在本仓库内clone一些东西，将本仓库当作Workspace.


## 询问个性化安装需求

上面链接中存在很多选项。默认我们只进行其中提到的这个: “安装或更新全部文件（初次安装先执行这个）”

根据文档梳理其他个性化安装选项，并列出执行计划，得到用户确认。对于不清楚自己在干什么的用户，我们倾向于推荐用户只执行 “安装或更新全部文件（初次安装先执行这个）”


## 进行安装

当确认后，按计划执行。


## 提醒用户手动收尾

1. 在windows右下角的rime图标右键 - 输入法设定 - 选择雾凇拼音
2. rime图标右键 - 重新部署 - 等待10-30秒
