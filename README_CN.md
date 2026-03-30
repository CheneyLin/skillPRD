# QQ PRD SKILL

通过对话式需求收集、PRD 骨架起草、HTML 原型生成（借助前端设计）、Mermaid 流程图绘制以及含 iframe 切片的最终 PRD，共 7 步敏捷工作流，引导新手 PM 完成全流程。

# 安装方法

## 安装 Trae IDE

中国大陆版本：https://www.trae.cn/

海外版本：https://www.trae.ai/

## 下载安装 QQ-PRD_Skill

下载 QQ-PRD_Skill 到本地。

```bash
git clone https://github.com/CheneyLin/skillPRD.git
```
也可以在本Github主页下载ZIP。

将 qq-prd_skill 文件夹复制并重命名，放到你所使用的 AI 助手的全局技能目录中。

可以将 qq-prd 文件夹重命名为 qq-prd_skill，也可以保持默认名称 qq-prd，复制到全局技能目录中。

以Mac为例：找到当前用户的文件目录，找到 .trae 文件夹，将 qq-prd_skill 文件夹复制到该文件夹中。
类似于

 - /Users/linyu/.trae/skills

 一般表述也会用～代表当前用户的文件目录，例如

 - ~/.trae/skills/qq-prd_skill

如果你使用cursor或 vs code，也可以将 qq-prd_skill 文件夹复制到全局技能目录中。
    
 - ~/.cursor/skills/qq-prd_skill
 - ~/.vscode/skills/qq-prd_skill
 
## 如何在项目中会用本技能

按照CodeX的Skill规范，建议在项目文件夹中按下面的结构组织：

```bash
├── .agents
│   ├── skills
│       ├── qq-prd_skill
├── document
│   ├── prf.md

```
# 使用方法

## 全AI启动

>在 AI 的对话框中直接输入 /qq-prd 并发送，然后告诉它你的新项目想法。AI 就会自动帮你建好标准的文件夹结构，并开始一步步引导你产出专业的需求文档了！

## PRF（产品需求收集表格）启动

提供一个初始化的产品需求收集表格让工作流高效开始：

```bash
├── document
│   ├── prf.md

```
使用MD格式编写需求文档，本模板也在Skill目录中提供（ /qq-prd/reference/prf.md ）：

```bash
# Product Requirements Form

## 项目名称

答题游戏

## 需求描述

1. **背景/痛点**

解决用户粘性问题，增加用户参与度。

2. **业务目标**

用户在答题游戏中，需要回答问题，获得奖励。

3. **用户与场景**

App中新增答题游戏模块，用户可以在模块中回答问题，获得奖励。

4. **核心用户旅程**

用户在答题游戏中，需要回答问题，获得奖励。

5. **产品范围**

运营后台新增答题游戏管理模块，用于管理答题游戏的问题、奖励等。
App中新增答题游戏模块，用户可以在模块中回答问题，获得奖励。

 6. **现有方案**

无

7. **参考/竞品**

无

## 额外要求
 
无
```

将初步填好的 PRF 文件保存到项目文件夹的 document 文件夹中。加入聊天窗口，输入 /qq-prd 并发送，AI 就会自动帮你建好标准的文件夹结构，并开始一步步引导你产出专业的需求文档了！

部分AI还是会就 PRF 文件中不完善的的地方进行提示，你需要根据提示进行完善。

## PRD工作流

### 工作文件结构

如果AI模型正常运行，会自动帮你建好标准的文件夹结构。以项目名称 QUIZGAME 为例：

```bash
├── QUIZGAME_PRD
│   ├── index.html
│   ├── v1.0
│       ├── prd_md
│       ├── prd_html
│       ├── prototype_html
│   ├── history
```
这个我命名为 PRD包，最终交付物就是这个文件夹。这个文件夹包含了项目的 PRD 文件，包括需求文档、PRD 骨架、HTML 原型、Mermaid 流程图等。

### 确认 PRD.MD 文件

如果AI模型正常运行，会自动生成 PRD.MD 文件。并让你确认细节，这时你可以手动修改 PRD.MD 文件。

确认后让 AI 生成 PRD HTML文件和 原型 HTML文件。并生成 主控制器 HTML文件 index.html 。你可以在浏览器中打开这个文件，查看 PRD包。

### 迭代 PRD.MD 文件

之后你可以继续迭代 PRD.MD 文件，直到你对 PRD 包满意为止。

每次修改完 PRD.MD 文件后，都需要确认细节，确认后让 AI 生成 PRD HTML文件和 原型 HTML文件。

如果功能调整比较大，或是与团队协作对齐，可以让AI或手工新增版本。

添加最新版本的PRD.MD到聊天窗口，通过以下AI指令，更新 PRD包。


```bash
PRD.MD 已确认，请同步更新 PRD HTML格式文件。
```

```bash
已确认，请同步更新 原型 HTML格式文件。
```

```bash
新版本已确认，请同步更新 主控 index.html 文件。
```

另外还建议在AI处理过程中，可明确要求AI将修改总结同步生成日志MD文档，存放在 history 文件夹中。


```bash
PRD.MD 已确认，请同步更新 PRD HTML格式文件。请同步更新 原型 HTML格式文件。请同步更新 主控 index.html 文件。请同步更新 history 文件夹中的日志文件。
```

# 常见问题

## 如何显示隐藏文件夹

### 在Mac上显示隐藏文件夹，可以使用快捷键Command + Shift + .（句点）来快速切换显示和隐藏状态。

 1. 打开Finder：在任意Finder窗口或桌面上。
 2. 按下快捷键：同时按下 Command + Shift + .（句点）。这将立即显示所有隐藏的文件和文件夹，隐藏的文件通常以半透明状态显示。
 3. 再次按下快捷键：如果想要隐藏这些文件，只需再次按下相同的快捷键即可。 


## 如何进入指定（隐藏）文件夹

### 在Mac上使用快捷键Command + Shift + G（G）来快速前往指定（隐藏）文件夹

 1. 打开Finder：在任意Finder窗口或桌面上。
 2. 按下快捷键：同时按下 Command + Shift + G。这将弹出一个快速前往文件夹的对话框。
 3. 输入文件夹路径：在对话框中输入要前往的文件夹路径，例如 `/Users/linyu/.trae/skills/qq-prd_skill`。
 4. 点击前往：点击对话框中的前往按钮，即可进入指定文件夹。 

