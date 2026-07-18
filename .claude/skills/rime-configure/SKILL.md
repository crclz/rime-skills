---
name: rime-configure
description: (在安装完rime后)帮助用户安装rime-ice(雾凇拼音方案)的向导
---

遵循准则skill: rime-guide-style


## 流程

1. 阅读 完备reference
2. 根据"高频常用"为用户梳理选项，对用户做出询问。优先让用户聚焦于"高频常用"
3. 如果用户遇到"高频常用" 以外的问题，则使用 “完备reference”的知识进行修改
4. 修改完成后，都需引导用户进行重新部署



## 完备reference

https://raw.githubusercontent.com/wiki/rime/home/CustomizationGuide.md


## 高频常用

高频常用代表了用户可能非常需要的个性化配置。

default.custom.yaml 是采用patch语法对default.yaml进行增量配置的文件.

```yaml 
customization:
  distribution_code_name: Weasel
  distribution_version: 0.17.4
  generator: "Rime::SwitcherSettings"
  modified_time: "Fri Jul 17 21:53:47 2026"
  rime_version: 1.13.1
patch:
  # 配置含义: shift从中文切换到输入法直接保留英文. rime_ice下不需要
  # "ascii_composer/switch_key/Shift_L": commit_code
  "key_binder/bindings/+": # 一定要有+，不然会覆盖掉方案的所有
    - {accept: "Control+BackSpace", send: Escape, when: composing} # ctrl+backspace快速清空输入框
    - {accept: bracketleft, send: Page_Up, when: has_menu} # [ 键上翻页. 需配合 unset 以词定字使用，不然不起作用
    - {accept: bracketright, send: Page_Down, when: has_menu} # ] 键下翻页 同理unset
  # 这两个unset是去除以词定字的
  "key_binder/select_first_character": !unset
  "key_binder/select_last_character": !unset
  schema_list:
    - {schema: rime_ice}
  "switcher/hotkeys": # ctrl + ~ 冲突解决. vscode用户强烈推荐
    - F4
```

weasel.custom.yaml

```yaml
# weasel.custom.yaml 是外观配置
customization:
  distribution_code_name: Weasel
  distribution_version: 0.17.4
  generator: "Weasel::UIStyleSettings"
  modified_time: "Sun Mar 22 12:55:49 2026"
  rime_version: 1.13.1
patch:
  "style/color_scheme": google
  "show_notifications": false # notification就是按shift切换时的那个方块. 我反正不喜欢
  show_notifications_time: 500
  # "style/horizontal": true  # 横排显示
```

