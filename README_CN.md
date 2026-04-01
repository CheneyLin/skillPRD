# QQ PRD SKILL

通过对话式需求收集、PRD 骨架起草、HTML 原型生成（借助前端设计）、Mermaid 流程图绘制以及含  iframe 联动导航结构的最终 PRD，共 7 步敏捷工作流，引导新手 PM 完成全流程。

# 快速了解

1. 创建一个项目
2. 创建 PRF.MD 文件，并确认项目信息和基本的需求描述
3. 调用Skill，生成 PRD.MD 文件，确认 PRD.MD 文件的内容是否完整准确
4. 继续执行Skill，生成 HTML 原型文件，确认 HTML 原型文件的内容是否完整准确
5. 迭代 PRD.MD 文件，直到满意为止

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

```bash
/qq-prd
```
如果IDE或工具不支持SKILL，需要手动调用SKILL。引入 PRF.MD 文件和 SKILL.MD，加入聊天窗口：

```bash
调用 skill /qq-prd 重新开始工作流
```

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
### 纠正 AI 错误 或切换 AI 模型

在实际使用过程中，AI 可能会出现文档错误、PRD 与原型不同步、或某些模型在特定任务上表现不佳的情况。以下是针对不同场景的标准化提示词指令，帮助你快速纠正问题。

#### 1. 文档内容错误纠正

**场景**：AI 生成的 HTML 格式 PRD 文档包含错误（如格式错乱、内容缺失、表格损坏等）。

**提示词**：
```bash
请根据 Markdown 格式 PRD 源文档（prd_v1.0.md），重新生成 HTML 格式 PRD 文档（prd_v1.0.html）。

要求：
1. 严格使用 /assets/prd_template.html 模板样式和结构
2. 确保 HTML 内容与 Markdown 内容完全一致
3. 保留所有功能标识（id）和"查看原型"按钮
4. 检查并修复所有表格、卡片、按钮等 UI 元素
```

#### 2. 原型文件错误纠正

**场景**：HTML 格式原型文件存在问题（如交互失效、样式错误、缺少页面等）。

**后台/PC Web 原型纠正提示词**：
```bash
请重新生成后台管理原型文件（admin_v1.0.html）。

要求：
1. 严格参考 /assets/admin_prototype_template.html 模板结构和样式
2. 实现所有子页面的原型展示和交互模拟
3. 支持全局视图切换和指定界面高亮定位（Focus 模式）
4. 保留 postMessage 通信逻辑，确保与主控文档联动正常
5. 使用 Element UI 组件库，保持 Material Design 风格
```

**移动端/H5 原型纠正提示词**：
```bash
请重新生成移动端原型文件（h5_v1.0.html 或 app_v1.0.html）。

要求：
1. 严格参考 /assets/app_prototype_template.html 模板结构和样式
2. 手机尺寸固定为 390x844px，模拟真实手机比例
3. 默认采用响应式网格布局（全局视图），支持切换至单页交互模式
4. 必须包含【全局视图】和【重置】悬浮按钮
5. 支持 URL 锚点自动高亮定位（如 #home、#quiz）
6. 使用 Tailwind CSS，保持现代简洁设计风格
7. 所有页面防溢出，严禁使用超出容器宽度的绝对定位
```

#### 3. PRD 与原型不同步纠正

**场景**：PRD 文档已更新，但原型未同步；或原型调整后，PRD 未实时更新。

**双向同步提示词**：
```bash
PRD 与原型需要同步更新，请执行以下操作：

1. 基于最新 prd_v1.0.md，更新 prd_v1.0.html
2. 基于最新原型调整，更新 admin_v1.0.html
3. 确保 PRD 功能标识与原型 data-prototype 属性一一对应
4. 测试左右联动功能：滚动 PRD 时原型自动高亮定位
5. 更新 index.html 主控文档的版本切换配置

检查清单：
- [ ] PRD 中每个功能模块都有"查看原型"按钮
- [ ] 原型中每个功能模块都有 data-prototype 属性
- [ ] Focus 模式正常生效
- [ ] 所有文件路径符合目录架构规范
```

#### 4. 切换 AI 模型

**场景**：当前 AI 模型在特定任务上表现不佳（如前端设计能力弱、逻辑理解差），需要切换到更强的模型。

**通用切换提示词**：
```bash
基于 qq-prd skill 工作流规范，请完成以下任务：

[具体任务描述，例如：完成 admin_v1.0.html，实现全部子项目的原型展示和交互模拟]

要求：
1. 严格遵循 /assets 目录下的对应模板
2. 保持与 prd_v1.0.md 内容一致
3. 确保所有交互功能和联动逻辑正常
```

**针对前端设计的模型切换提示词**：
```bash
我需要切换到擅长前端设计的 AI 模型，完成高保真原型开发。

任务：基于 qq-prd skill，严格参考 ./qq-prd/assets/admin_prototype_template.html 模板，重新生成 admin_v1.0.html。

技术要求：
1. 使用 Element UI 组件库（或我指定的 UI 库：Ant Design/Element Plus 等）
2. 实现完整的列表页、表单页、弹窗等交互
3. 支持 URL Hash 路由切换页面
4. 添加 Focus 模式支持（?focus=feature_id 参数）
5. 保留 postMessage 通信接口，支持与 PRD 联动

UI 风格要求：
[选择一种风格]
- 简约高效风：浅色系底色，卡片式布局，圆角设计
- 科技质感风：中性灰底色，轻微阴影，渐变色按钮
```

**针对逻辑理解的模型切换提示词**：
```bash
我需要切换到擅长业务逻辑理解的 AI 模型，完善 PRD 文档。

任务：基于初步需求，完成 prd_v1.0.md 的详细方案章节。

要求：
1. 按照 /assets/prd_template.md 结构组织文档
2. 为每个功能模块添加唯一标识（如 feature_01、strategy_create）
3. 补充完整的业务规则、前置条件、异常处理
4. 绘制 Mermaid 流程图（flowchart TD 或 sequenceDiagram）
5. 确保逻辑闭环，无歧义
```

#### 5. 主控文档联动失效纠正

**场景**：index.html 主控文档的左右联动功能失效、版本切换不生效、或 iframe 路径错误。

**主控文档修复提示词**：
```bash
请重新生成主控文档 index.html，修复联动功能。

要求：
1. 严格参考 /assets/index_template.html 模板结构和样式
2. 顶部导航栏包含：项目名称、版本切换下拉菜单、产品形态切换按钮
3. 主体区域左右分栏各占 50%，支持拖拽调整宽度（30%-70%）
4. 左侧 iframe 嵌入 PRD 文档，右侧 iframe 嵌入原型
5. 实现左右联动功能：
   - 监听 PRD 滚动事件，自动高亮原型对应模块
   - 点击"查看原型"按钮，手动触发原型定位
   - 通过 postMessage 在 iframe 间通信
6. 版本切换时同步更新左右 iframe 的 src 路径
7. 使用 localStorage 保存分栏布局状态

文件路径示例：
- v1.0 PRD: ./v1.0/prd_html/prd_v1.0.html
- v1.0 原型：./v1.0/prototype_html/admin_v1.0.html
```

#### 6. 版本迭代规范

**场景**：从 v1.0 升级到 v1.1，需要保留历史版本并创建新版本。

**版本迭代提示词**：
```bash
项目需要迭代到 v1.1 版本，请执行以下操作：

1. 复制历史版本文件（不覆盖）：
   - 复制 prd_v1.0.html → prd_v1.1.html
   - 复制 admin_v1.0.html → admin_v1.1.html
   - 复制 h5_v1.0.html → h5_v1.1.html

2. 在 prd_v1.1.html 的【版本记录】表格中添加：
   | 版本 | 日期 | 内容 |
   | v1.1 | 2026-03-31 | [本次迭代变更详情] |

3. 更新 index.html 主控文档：
   - 在版本切换下拉菜单新增 v1.1 选项
   - 配置 v1.1 版本的 iframe 路径

4. 生成本次迭代日志：
   - 文件名：history/ai_2026_03_31_v1.1_update.md
   - 内容：变更总结、影响范围、测试结果

注意：保留 v1.0 作为历史快照，所有修改仅在 v1.1 文件中进行。
```

#### 7. 完整重建 PRD 包

**场景**：PRD 包混乱、文件丢失、或多处不一致，需要彻底重建。

**完整重建提示词**：
```bash
请基于 qq-prd skill 工作流规范，完整重建 PRD 包。

输入文件：document/prf.md（或最新的 prd_v1.0.md）

输出结构：

├── QUIZGAME_PRD
│   ├── index.html          (主控文档)
│   ├── v1.0
│   │   ├── prd_md
│   │   │   └── prd_v1.0.md
│   │   ├── prd_html
│   │   │   └── prd_v1.0.html
│   │   ├── prototype_html
│   │   │   ├── admin_v1.0.html
│   │   │   └── h5_v1.0.html
│   │   └── assets
│   └── history


执行步骤：
1. 确认 PRD.MD 内容完整准确
2. 生成 prd_v1.0.html（使用 prd_template.html 模板）
3. 生成 admin_v1.0.html（使用 admin_prototype_template.html 模板）
4. 生成 h5_v1.0.html（使用 app_prototype_template.html 模板）
5. 生成 index.html（使用 index_template.html 模板）
6. 配置所有功能标识和联动逻辑
7. 生成交付检查清单

交付检查：
- [ ] 所有 HTML 文件可独立运行
- [ ] index.html 可正常打开，左右分栏显示
- [ ] 版本切换功能正常
- [ ] 左右联动功能正常（自动 + 手动）
- [ ] 原型 Focus 模式正常
- [ ] 所有文件路径正确
```

---

## 最佳实践建议

1. **及时确认**：每完成一个步骤，立即在浏览器中打开查看，发现问题及时纠正。

2. **小步迭代**：不要一次性让 AI 完成所有工作，分步骤确认后再推进下一步。

3. **保留历史**：每次迭代都复制一份历史版本，方便对比和回溯。

4. **手动校验**：AI 生成后，手动检查关键功能（如联动、版本切换）是否正常。

5. **日志记录**：要求 AI 生成修改日志存放到 history 文件夹，方便团队协作和追溯。

6. **模板优先**：所有文档必须使用 /assets 下的对应模板，确保格式统一。

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

