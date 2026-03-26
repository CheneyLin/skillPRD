# QQ产品经理PRD工作流 (QQ PRD Workflow)

## 触发方式

当用户提供一个初步的想法或需求描述时，请严格按照以下**七个步骤**引导用户。

**🚨 绝对强制指令：你必须一步一步（Step-by-Step）执行！绝不允许一次性输出所有步骤的结果。在每一个带有【等待用户确认】的步骤结束后，你必须停止输出，等待用户的回答！**

---

## 步骤一：对话式需求采集与确认

新手往往难以一次性说清需求。AI 应首先采用「灵活对话式」引导，主动评估、温和追问、并进行总结确认。在需求未明确前，**不要急于创建文件或文件夹**。

### 1.1 接收需求

- 接受用户的任意形式输入（一句话、截图、草图、大白话）。

- **不要**要求用户填写复杂的固定模板，降低认知门槛。

### 1.2 核心维度评估与反馈

当你接收到用户的初步需求后，**必须将以下 7 个关键维度的评估结果直接展示给用户**，告诉他们当前需求在哪些维度是清晰的，哪些是缺失的：

1. **背景/痛点**：为什么要做？现状有什么问题？（必须）

2. **业务目标**：做完后想达到什么效果？（必须）

3. **用户与场景**：谁在什么具体情况下使用？（必须）

4. **核心用户旅程**：用户从接触到完成目标的关键路径是怎样的？中间有什么触点和痛点？（必须）

5. **现有方案**：现在他们是怎么解决这个问题的？（重要）

6. **业务规则**：有哪些必须遵守的限制或特定流程？（重要）

7. **参考/竞品**：有没有喜欢的对标产品？（加分项）

### 1.3 深度追问与多轮确认 【等待用户确认】

**🚨 关键规则：不要急于总结，必须进行至少 3 轮深度的启发式追问！**

- **追问方式**：抛弃死板的选项（A/B/C），采用**开放式、启发式**的提问，引导用户多方面、更全面地思考这个需求。

- **追问数量**：每次追问必须在 **3 到 5 个问题**之间。

- **循环机制**：基于用户的上一次回答，挖掘出新的盲点继续追问，至少进行 3 轮对话。

- **最终确认**：只有当你通过多轮追问**完全理解**了需求的所有细节，并且用户明确表示“没有补充了，可以开始写了”之后，你才能进行结构化复述并进入下一步。

- **🛑 强制暂停：在每一轮提问后必须停止输出！等待用户回复后才能进行下一轮动作。**

---

## 步骤二：项目初始化与目录架构搭建

在需求确认无误，准备开始产出文档之前，必须先帮用户建立一个清晰、规范的项目文件夹结构，避免后期文件混乱。

### 2.1 建立标准目录树

主动为当前项目创建一个专属的根文件夹（如以项目名称命名），并在其中创建以下标准子目录：

- `prd/`：用于存放所有的产品需求文档（如 `prd_v1.0.html`）。

- `prototype/`：用于存放所有的高保真 HTML 原型文件。

- `flowcharts/`：用于存放 Mermaid 流程图或导出的图片。

- `annex/`：用于存放各种附件（如原始的 Excel/CSV 数据字典、需求原始文稿、参考资料等）。

- `templates/`：用于存放工作流模板或参考文件（如 `prd_template.md`）。

### 2.2 确认架构

向用户展示创建好的目录结构，并告知后续的产出物都将分类存放在这些对应的文件夹中。

---

## 步骤三：输出“详细的第一版初步PRD”

**🚨 关键规则：初步的 PRD 也必须非常详细，不能只是一个空框架。**

### 3.1 产出内容

根据步骤一的确认信息，直接生成一份详细的初步 **HTML 格式**文档（存放在 `prd/` 目录下）。这份初版 PRD 必须搭建好完整的文档结构骨架（参考 6.1 节的标准目录），并且必须深度填充以下部分：

1. **项目基本信息**

2. **需求背景与目标**：必须包含四列表格（目标类型、描述、衡量指标、目标值）。

3. **用户使用场景与旅程图**：必须使用表格或清晰的结构描述用户旅程（User Journey Map），包含：阶段、用户触点、用户行为、痛点/情绪、产品机会点，要具备强烈的代入感。

4. **详细的功能清单与基础逻辑**：不能只列出模块和名称，必须详细梳理出核心的操作主线、前置条件、基本业务规则和数据流向。

*（后续章节如详细方案带原型的模块、整体流程图等可先留空，并注明“待原型确认后补充”）*

### 3.2 用户确认 【等待用户确认】

询问用户：“这是产品的详细第一版架构和业务逻辑，您看方向和基础逻辑准确吗？如果没问题，我们将先进行【原型设计】，通过具体的画面来进一步理清交互细节和可能遗漏的功能。”

**🛑 强制暂停：在此处必须停止输出！等待用户回复同意后，才能进入步骤四。**

---

## 步骤四：产出高保真 HTML 原型 (核心验证阶段)

**这是本工作流最具特色的环节。** 新手往往在看到具体画面后，才能发现逻辑上的漏洞（如缺失的返回按钮、未考虑的空状态）。

### 4.1 原型规范

1. 产出 **单文件 HTML 原型**，包含完整的 CSS 样式。

2. 强制使用 **Tailwind CSS**，并采用现代、简洁的设计风格。

3. 必须包含关键的交互状态（如：默认页、展开弹窗、成功提示等）。可以通过简单的原生 JavaScript 或 URL Hash (`#page1`) 来实现页面切换。

4. **沙盒锁定支持 (Focus Mode)**：在编写原生 JavaScript 时，必须加入 URL 参数解析逻辑（如 `?focus=feature_id`）。当处于 focus 模式时，高亮或提示对应的功能点。这为了后续在 PRD 嵌入原型时，实现“高亮展示对应功能交互”的需求。

### 4.2 💡 强烈推荐使用 Impeccable Skills

在生成原型前，AI 必须主动向用户推荐业界顶级的前端设计指令集：

> “为了让原型达到专业级的高级 UI 效果，我强烈建议您使用 [Impeccable](https://impeccable.style/) 提供的设计技能库。如果您在编辑器中（如 Trae/Cursor）已经安装了 `frontend-design` 或 `teach-impeccable` 等指令，请告诉我，我将调用这些专业的前端设计规范为您生成精美的界面。”
>
>

询问用户是否有现有原型UI参考代码可以使用；若没有，可根据产品类别选择对应UI风格，具体选项示例如下，均适配Tailwind CSS设计规范，贴合现代简洁设计要求：

- **PC端产品（后台管理/PC Web）**：提供2种主流风格选项，可直接参考适配
                 风格1：简约高效风（适配后台系统）—— 浅色系底色（#f8f9fa），卡片式布局，按钮采用圆角设计（border-radius: 4px），字体选用无衬线字体（Inter/微软雅黑），强调层级分明，操作区域与展示区域清晰分隔，适配多窗口切换场景。

- 风格2：科技质感风（适配工具类PC产品）—— 中性灰底色（#f5f7fa），轻微阴影卡片（box-shadow: 0 2px 8px rgba(0,0,0,0.08)），按钮采用渐变色（如#1677ff至#0f62fe），图标选用线性图标，整体风格简洁且具科技感。

- **手机端产品（App/Mobile Web）**：提供2种主流风格选项，适配移动端交互场景
                 风格1：清爽简约风（适配多数工具/社交App）—— 白色底色，轻量化卡片，按钮圆角适中（border-radius: 8px），字体大小适配移动端（标题18px、正文14px），操作控件间距合理（16px-20px），支持深色模式切换。

- 风格2：活力年轻化风（适配娱乐/内容类App）—— 柔和渐变色底色（如浅蓝/浅粉渐变），圆润卡片设计（border-radius: 12px），按钮采用撞色设计，图标选用填充式图标，整体视觉活泼，贴合年轻用户审美。

用户可选择上述任意风格，或提供自有UI参考，将据此优化原型界面设计，确保贴合产品定位。

### 4.3 原型审查与 PRD 双向同步更新 (核心迭代循环) 【等待用户反馈】

- 将生成的 HTML 代码或预览呈现给用户。

- 引导用户思考：“看看这个界面，您觉得用户点完这个按钮后，如果网络断了该怎么提示？这里的信息展示够全吗？”

- **🛑 强制暂停：在此处必须停止输出！等待用户反馈修改意见。**

- 根据用户的反馈修改原型。

- **🚨 关键规则（PRD 实时同步）**：每次用户提出对原型的修改（如增加功能、修改交互逻辑、调整页面流转），AI **必须**在修改 HTML 原型的同时，同步更新第二版（详细版）PRD 中对应的“详细方案”表格。不仅要更新逻辑描述，还要确保切片引用路径与最新原型保持一致。

- 只有当用户对原型表示“完全满意”、“可以进入下一步”时，才可进入步骤五。

---

## 步骤五：输出流程图 (Mermaid)

在原型跑通后，业务逻辑已经相对清晰，此时再来画流程图。

1. 使用 **Mermaid** 语法（`flowchart TD` 或 `sequenceDiagram`）。

2. 重点描绘：用户的核心操作主线，以及刚才在原型审查中发现的**异常分支**。

3. 确保代码中没有会导致渲染错误的特殊字符（如未转义的中文括号）。

---

## 步骤六：产出最终版 PRD (内嵌原型与切片)

综合前四步的所有成果，输出最终的详细产品需求文档，新增根目录下 `index.html` 作为主控文档，实现版本切换、分栏展示及左右联动功能，具体要求如下：

### 6.1 主控文档（根目录 index.html）核心要求

主控文档作为整个 PRD 与原型的入口，统一管理版本切换和分栏展示，替代原单版本 PRD 直接打开的方式，具体结构分为三个区域，需通过 HTML+CSS+原生 JavaScript 实现，无外部依赖，核心代码参考如下：

#### 主控文档（index.html）核心代码参考

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>项目名称 - PRD 主控文档</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* 顶部导航栏样式 */
        .header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            height: 60px;
            background: #fff;
            border-bottom: 1px solid #eee;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 20px;
            z-index: 999;
        }
        /* 分栏容器样式 */
        .container {
            display: flex;
            height: calc(100vh - 60px);
            margin-top: 60px;
            overflow: hidden;
        }
        /* 左侧PRD文档区 */
        .prd-area {
            flex: 50%;
            min-width: 30%;
            max-width: 70%;
            overflow-y: auto;
            padding: 20px;
            border-right: 1px solid #eee;
        }
        /* 右侧原型区 */
        .prototype-area {
            flex: 50%;
            min-width: 30%;
            max-width: 70%;
            overflow-y: auto;
            padding: 20px;
        }
        /* 分隔线拖拽样式 */
        .resizer {
            width: 5px;
            background: #eee;
            cursor: col-resize;
            height: 100%;
        }
        .resizer:hover {
            background: #ccc;
        }
        /* 原型模块高亮样式 */
        .feature-highlight {
            border: 2px solid #1677ff;
            box-shadow: 0 0 8px rgba(22, 119, 255, 0.3);
            transition: all 0.3s ease;
        }
    </style>
</head>
<body>
    <!-- 顶部导航栏（项目名称+版本切换） -->
    <div class="header">
        <h1 class="text-xl font-bold">项目名称（与PRD项目信息一致）</h1>
        <select id="version-select" class="px-3 py-1 border rounded">
            <option value="v1.0">v1.0</option>
            <option value="v1.1">v1.1</option>
            <!-- 后续迭代版本可新增option -->
        </select>
    </div>

    <!-- 主体左右分栏 -->
    <div class="container">
        <div class="prd-area" id="prd-area">
            <!-- 嵌入对应版本PRD内容，每个功能模块添加唯一标识及查看原型按钮 -->
            <div class="feature-module" data-feature="feature_01">
                <h3>功能1：XXX</h3>
                <p>功能详细逻辑描述...</p>
                <button class="view-prototype-btn px-3 py-1 bg-blue-500 text-white rounded mt-2" data-feature-id="feature_01">查看原型</button>
            </div>
            <div class="feature-module" data-feature="feature_02">
                <h3>功能2：XXX</h3>
                <p>功能详细逻辑描述...</p>
                <button class="view-prototype-btn px-3 py-1 bg-blue-500 text-white rounded mt-2" data-feature-id="feature_02">查看原型</button>
            </div>
        </div>
        <div class="resizer" id="resizer"></div>
        <div class="prototype-area" id="prototype-area">
            <!-- 嵌入对应版本原型，每个功能模块添加对应标识 -->
            <div class="prototype-module" data-prototype="feature_01">
                <!-- 原型界面1 -->
                <h4>功能1原型</h4>
                <!-- 原型HTML内容或iframe嵌入原型文件 -->
            </div>
            <div class="prototype-module" data-prototype="feature_02">
                <!-- 原型界面2 -->
                <h4>功能2原型</h4>
                <!-- 原型HTML内容或iframe嵌入原型文件 -->
            </div>
        </div>
    </div>

    <script>
        // 1. 版本切换功能
        const versionSelect = document.getElementById('version-select');
        const prdArea = document.getElementById('prd-area');
        const prototypeArea = document.getElementById('prototype-area');
        let prdIframe = null; // 存储PRD iframe实例
        let prototypeIframe = null; // 存储原型iframe实例

        versionSelect.addEventListener('change', function() {
            const selectedVersion = this.value;
            // 切换PRD文档（iframe嵌入对应版本PRD）
            prdArea.innerHTML = '<iframe src="./prd/prd_' + selectedVersion + '.html" frameborder="0" width="100%" height="100%"></iframe>';
            // 切换原型（iframe嵌入对应版本原型）
            prototypeArea.innerHTML = '<iframe src="./prototype/prototype_' + selectedVersion + '.html" frameborder="0" width="100%" height="100%"></iframe>';
            // 获取iframe实例，用于后续消息通信
            prdIframe = prdArea.querySelector('iframe');
            prototypeIframe = prototypeArea.querySelector('iframe');
        });

        // 2. 分栏宽度调整功能
        const resizer = document.getElementById('resizer');
        const container = document.querySelector('.container');
        let isResizing = false;

        resizer.addEventListener('mousedown', function(e) {
            isResizing = true;
            document.body.style.cursor = 'col-resize';
        });

        document.addEventListener('mousemove', function(e) {
            if (!isResizing) return;
            const containerRect = container.getBoundingClientRect();
            const newPrdWidth = e.clientX - containerRect.left;
            // 限制宽度范围（30%-70%）
            if (newPrdWidth >= containerRect.width * 0.3 && newPrdWidth <= containerRect.width * 0.7) {
                prdArea.style.flex = `0 0 ${newPrdWidth}px`;
                prototypeArea.style.flex = `1 1 auto`;
                // 保存布局状态到localStorage
                localStorage.setItem('prdLayout', JSON.stringify({ prdWidth: newPrdWidth }));
            }
        });

        document.addEventListener('mouseup', function() {
            isResizing = false;
            document.body.style.cursor = 'default';
        });

        // 3. 左右联动（PRD滚动定位原型高亮 + 手动点击查看原型按钮联动）
        // 3.1 PRD滚动联动
        prdArea.addEventListener('scroll', function() {
            const featureModules = prdArea.querySelectorAll('.feature-module');
            const prototypeModules = prototypeArea.querySelectorAll('.prototype-module');
            featureModules.forEach(module => {
                const rect = module.getBoundingClientRect();
                // 判断模块是否在可视区域内
                if (rect.top < prdArea.clientHeight && rect.bottom > 0) {
                    const featureId = module.getAttribute('data-feature');
                    // 发送高亮指令给原型iframe
                    if (prototypeIframe) {
                        prototypeIframe.contentWindow.postMessage({
                            action: 'highlight',
                            featureId: featureId
                        }, window.location.origin);
                    }
                }
            });
        });

        // 3.2 接收PRD文档发送的手动点击联动指令，转发给原型iframe
        window.addEventListener('message', function(e) {
            // 验证消息来源，避免跨域异常
            if (e.origin !== window.location.origin) return;
            const message = e.data;
            // 接收PRD中查看原型按钮的指令，转发给原型iframe
            if (message.action === 'highlight' && message.featureId && prototypeIframe) {
                prototypeIframe.contentWindow.postMessage({
                    action: 'highlight',
                    featureId: message.featureId
                }, window.location.origin);
            }
        });

        // 4. 页面加载时恢复保存的布局状态
        window.addEventListener('load', function() {
            const savedLayout = localStorage.getItem('prdLayout');
            if (savedLayout) {
                const { prdWidth } = JSON.parse(savedLayout);
                prdArea.style.flex = `0 0 ${prdWidth}px`;
                prototypeArea.style.flex = `1 1 auto`;
            }
            // 默认加载第一个版本，获取iframe实例
            versionSelect.dispatchEvent(new Event('change'));
        });
    </script>
</body>
</html>
```
#### PRD文档功能标识设置代码参考（prd_v1.0.html）

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>项目PRD - v1.0</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <h1>项目PRD（v1.0）</h1>
    <!-- 详细方案章节，每个功能模块添加唯一data-feature标识，与原型对应，新增查看原型按钮 -->
    <section id="detailed-plan">
        <div class="feature-module" data-feature="feature_01">
            <h3>功能1：用户登录</h3>
            <p>前置条件：用户已注册账号...</p>
            <p>业务逻辑：1. 输入账号密码；2. 验证账号密码合法性；3. 登录成功跳转首页...</p>
            <!-- 可嵌入原型切片截图 -->
            <img src="../prototype/slices/login_slice.png" alt="用户登录原型切片" class="w-full my-2">
            <!-- 新增查看原型按钮，点击触发联动 -->
            <button class="view-prototype-btn px-3 py-1 bg-blue-500 text-white rounded mt-2" data-feature-id="feature_01">查看原型</button>
        </div>
        <div class="feature-module" data-feature="feature_02">
            <h3>功能2：数据查询</h3>
            <p>前置条件：用户已登录...</p>
            <p>业务逻辑：1. 输入查询条件；2. 点击查询按钮；3. 展示查询结果...</p>
            <img src="../prototype/slices/query_slice.png" alt="数据查询原型切片" class="w-full my-2">
            <!-- 新增查看原型按钮，点击触发联动 -->
            <button class="view-prototype-btn px-3 py-1 bg-blue-500 text-white rounded mt-2" data-feature-id="feature_02">查看原型</button>
        </div>
    </section>
    <script>
        // PRD文档中查看原型按钮的联动逻辑，向主控文档发送指令
        document.querySelectorAll('.view-prototype-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const featureId = this.getAttribute('data-feature-id');
                // 向主控文档发送联动指令，触发原型高亮定位
                window.parent.postMessage({
                    action: 'highlight',
                    featureId: featureId
                }, window.location.origin);
            });
        });
    </script>
</body>
</html>
```

#### 原型适配联动代码参考（prototype_v1.0.html）

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <title>项目原型 - v1.0</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <h1>项目原型（v1.0）</h1>
    <!-- 每个原型模块添加data-prototype标识，与PRD的data-feature一一对应 -->
    <div class="prototype-module" data-prototype="feature_01">
        <h3>用户登录界面</h3>
        <!-- 原型界面HTML实现，模拟登录表单 -->
        <div class="w-64 mx-auto p-4 border rounded">
            <input type="text" placeholder="账号" class="w-full p-2 border rounded mb-2">
            <input type="password" placeholder="密码" class="w-full p-2 border rounded mb-2">
            <button class="w-full p-2 bg-blue-500 text-white rounded">登录</button>
        </div>
    </div>
    <div class="prototype-module" data-prototype="feature_02" style="margin-top: 40px;">
        <h3>数据查询界面</h3>
        <!-- 原型界面HTML实现，模拟查询功能 -->
        <div class="w-80 mx-auto p-4 border rounded">
            <input type="text" placeholder="输入查询条件" class="w-full p-2 border rounded mb-2">
            <button class="p-2 bg-blue-500 text-white rounded">查询</button>
            <div class="mt-2 p-2 border rounded">查询结果展示区</div>
        </div>
    </div>

    <script>
        // 接收主控文档指令，实现高亮定位
        window.addEventListener('message', function(e) {
            const { type, featureId } = e.data;
            if (type === 'highlightFeature') {
                // 移除所有高亮，给目标模块添加高亮
                document.querySelectorAll('.prototype-module').forEach(module => {
                    module.classList.remove('feature-highlight');
                });
                const targetModule = document.querySelector(`.prototype-module[data-prototype="${featureId}"]`);
                if (targetModule) {
                    targetModule.classList.add('feature-highlight');
                }
            }
        });
    </script>
</body>
</html>
```

说明：以上代码可直接复制使用，需根据实际项目名称、版本及功能标识调整对应内容；所有文件路径需严格遵循目录架构（index.html在根目录，PRD在prd/目录，原型在prototype/目录），确保联动功能正常生效。

1. **顶部区域（导航栏）**：


    - 左侧显示项目名称（与 PRD 项目信息一致），字体加粗、尺寸适中，清晰可辨。

    - 右侧设置版本切换下拉菜单，支持选择所有已迭代版本（如 v1.0、v1.1），点击对应版本后，左侧 PRD 文档区和右侧原型区同步切换至该版本内容，无页面刷新。

    - 样式要求：导航栏固定在页面顶部，不随滚动消失，背景色与 PRD 主色调统一，边框底部简洁，避免冗余装饰，适配所有主流屏幕尺寸。

2. **主体区域（左右分栏）**：


    - 默认布局：左右各占 50% 宽度，高度为页面剩余高度（扣除顶部导航栏），均支持独立滚动，避免内容挤压。

    - 分栏调整：支持拖拽分栏中间的分隔线，调整左右区域宽度（范围限制：左侧最小 30%、最大 70%；右侧最小 30%、最大 70%），调整后实时保存布局状态（通过 localStorage 实现，刷新页面后保留调整结果）。

    - 左侧区域（PRD 文档区）：嵌入当前选中版本的 PRD 文档（路径如 `./prd/prd_v1.0.html`），通过 iframe 实现，确保 PRD 原有排版、目录导航、流程图等功能正常展示，无样式错乱。

    - 右侧区域（原型区）：嵌入当前选中版本的高保真原型（路径如 `./prototype/prototype_v1.0.html`），通过 iframe 实现，保留原型原有交互功能和 Focus 模式，支持后台/PC Web、App/Mobile Web 原型的正常展示。

3. **左右联动功能（核心）**：


    - 关联规则：为 PRD 文档中每个“详细功能逻辑”模块设置唯一标识（如 `feature_01`），对应原型中该功能/界面模块的唯一标识，确保一一对应。

    - 联动效果：当用户在左侧 PRD 文档区滚动，且当前可视区域包含某个“详细功能逻辑”模块时，右侧原型区自动定位到该功能对应的界面模块，并通过 Focus 模式高亮该模块（如添加边框、阴影，或轻微放大），同时滚动原型区至该模块居中位置，无需手动操作；新增手动触发方式，每个“详细功能逻辑”模块添加“查看原型”按钮，点击按钮可直接触发右侧原型区对应模块的定位与高亮。

    - 实现方式：通过原生 JavaScript 监听左侧 iframe 的滚动事件，解析当前可视区域的功能标识，再通过 postMessage 向右侧 iframe 发送指令，触发原型区的定位和高亮操作；手动点击联动通过为“查看原型”按钮绑定点击事件，向主控文档发送功能标识指令，由主控文档转发至原型 iframe，确保联动流畅无延迟。

### 6.2 最终版 PRD 文档（prd/ 目录下）规范

prd/ 目录下的各版本 PRD 文档（如 prd_v1.0.html），需配合主控文档实现联动，在原有结构基础上补充以下要求，整体仍采用 HTML 格式，确保独立运行可用：

1. **排版与 UI 规范**：


    - **动态 UI 升级 (Impeccable Skills)**：如果用户在工作流执行期间安装了 Impeccable Skills，必须在生成或更新 PRD 时调用相关指令（如 `/typeset`, `/arrange`, `/colorize`），对 PRD 的排版和色彩进行高级 UI 升级。

    - **目录导航 (TOC)**：页面顶部提供固定目录导航，方便快速跳转至各章节，与主控文档联动后不影响原有导航功能。

    - **字体层级与间距**：严格区分 H1（页面标题）、H2（章节标题）、H3（模块标题），设置合适的 `line-height` (如 1.6) 和段落间距（如 `margin-bottom: 1.5rem`），确保阅读体验舒适。

2. **功能标识设置**：


    - 在“详细方案”章节中，每个功能点的容器标签（如 div、section）添加唯一 `id` 属性（即功能标识，格式如 `feature_01`、`feature_02`），与原型中对应模块的标识一致；同时为每个功能模块添加“查看原型”按钮，按钮需绑定功能标识，用于手动触发原型联动。

    - 功能标识需在 PRD 文档开头的“功能清单”中同步标注，方便后续维护和关联核对。

3. **标准目录结构**：严格遵循以下目录组织，确保与主控文档适配，不遗漏核心内容：


    1. **项目信息与版本记录** (包含版本迭代详情，配合主控文档版本切换功能)

    2. **一、需求背景** (现状问题、为什么现在做)

    3. **二、需求目标** (目标类型、描述、衡量指标、目标值)

    4. **三、用户与使用场景** (典型用户与 User Journey)

    5. **四、需求功能清单** (骨架与优先级，标注各功能唯一标识)

    6. **五、详细方案** (带功能标识，与原型模块一一对应)

    7. **六、业务流程图** (Mermaid 格式)

    8. **七、异常与边界处理** (断网、空状态、无权限等)

    9. **八、数据追踪与埋点** (可选)

    10. **九、未来演进规划** (Roadmap)

    11. **十、附件** (数据字典/工艺标准等)

### 6.3 原型适配要求（prototype/ 目录下）

各版本原型需配合主控文档的联动功能，补充以下适配规则，确保定位和高亮正常，核心代码参考如下，与原有规范保持一致：

```javascript
// 原型接收主控文档联动指令的核心代码（嵌入prototype各版本HTML中）
// 用于接收主控文档发送的定位高亮指令，实现PRD与原型联动
window.addEventListener('message', function(e) {
    // 验证消息来源，避免跨域异常
    if (e.origin !== window.location.origin) return;
    const message = e.data;
    // 接收主控文档的高亮指令
    if (message.action === 'highlight' && message.featureId) {
        // 移除所有原型模块的高亮状态
        document.querySelectorAll('.prototype-module').forEach(module => {
            module.classList.remove('feature-highlight');
        });
        // 定位并高亮对应功能模块
        const targetModule = document.querySelector(`.prototype-module[data-prototype="${message.featureId}"]`);
        if (targetModule) {
            targetModule.classList.add('feature-highlight');
            // 滚动原型区至目标模块居中，提升体验
            targetModule.scrollIntoView({ behavior: 'smooth', block: 'center' });
        }
    }
});
```

补充说明：原型中所有功能模块需添加 `data-prototype` 属性，属性值与 PRD 文档中对应功能模块的 `data-feature` 属性值完全一致，确保联动无偏差；若原型为多页面，需在每个页面中嵌入上述代码，保证切换原型页面后联动功能仍正常。

```javascript
// 原型接收主控文档联动指令的核心代码（嵌入prototype各版本HTML中）
// 用于接收主控文档发送的定位高亮指令，实现PRD与原型联动
window.addEventListener('message', function(e) {
    // 验证消息来源，避免跨域异常
    if (e.origin !== window.location.origin) return;
    const message = e.data;
    // 接收主控文档的高亮指令
    if (message.action === 'highlight' && message.featureId) {
        // 移除所有原型模块的高亮状态
        document.querySelectorAll('.prototype-module').forEach(module => {
            module.classList.remove('feature-highlight');
        });
        // 定位并高亮对应功能模块
        const targetModule = document.querySelector(`.prototype-module[data-prototype="${message.featureId}"]`);
        if (targetModule) {
            targetModule.classList.add('feature-highlight');
            // 滚动原型区至目标模块居中，提升体验
            targetModule.scrollIntoView({ behavior: 'smooth', block: 'center' });
        }
    }
});

// 可选：反向联动（点击原型模块，定位PRD对应功能）
document.querySelectorAll('.prototype-module').forEach(module => {
    module.addEventListener('click', function() {
        const featureId = this.getAttribute('data-prototype');
        // 向主控文档发送反向联动指令
        window.parent.postMessage({
            action: 'scrollToFeature',
            featureId: featureId
        }, window.location.origin);
    });
});
```

补充说明：原型中所有功能模块需添加 `data-prototype` 属性，属性值与 PRD 文档中对应功能模块的 `data-feature` 属性值完全一致，确保联动无偏差；若原型为多页面，需在每个页面中嵌入上述代码，保证切换原型页面后联动功能仍正常。

1. 为每个功能/界面模块添加唯一标识，与 PRD 文档中对应功能的标识一致（如 `feature_01`），可通过给模块容器添加 `id` 或 `data-feature` 属性实现。

2. 完善 Focus 模式逻辑，新增接收主控文档指令的接口，当收到定位高亮指令时，自动高亮对应模块（如添加 2px 红色边框、5px 阴影，持续 3 秒后恢复正常，或保持高亮至切换功能模块）。

3. 确保原型支持通过 postMessage 接收外部指令（如定位标识、切换 Focus 模式），兼容不同版本原型的联动逻辑，无跨域问题。

4. 后台/PC Web、App/Mobile Web 原型的原有规范不变，需确保嵌入主控文档右侧区域后，界面完整、交互正常，适配分栏宽度调整。

### 6.4 交付检查

- [ ] 根目录 `index.html` 主控文档已创建，包含顶部导航（项目名称+版本切换）、主体左右分栏，支持分栏宽度调整。

- [ ] 主控文档版本切换功能正常，切换版本时，左侧 PRD 区和右侧原型区同步更新，无页面刷新。

- [ ] PRD 文档各功能模块已添加唯一标识，与原型对应模块标识一致。

- [ ] 包含清晰的**用户旅程图**（User Journey Map），详细方案中每个功能点都有对应的**Mermaid流程图**。

- [ ] 左右联动功能正常：左侧滚动至某功能逻辑模块时，右侧原型自动定位并高亮对应模块；点击左侧PRD功能模块的“查看原型”按钮，可手动触发右侧原型对应模块的定位与高亮。

- [ ] 后台/PC Web 原型实现完整框架和全交互功能，App/Mobile Web 原型嵌入纯 HTML 实现的手机模拟外框，适配主控文档右侧区域。

- [ ] 原型 Focus 模式正常，可接收主控文档指令实现高亮定位。

- [ ] 异常情况（断网、空数据、权限不足）已补充到 PRD 文档中。

- [ ] 手机模拟外框包含状态栏、底部导航等视觉元素，支持多界面切换/多外框并列展示。

---

## 步骤七：版本迭代与管理 (Version Control)

当项目进入后续迭代阶段（例如从 `v1.0` 升级到 `v1.1`）时，必须执行严格的结构化版本控制，确保历史可追溯，且不破坏过往版本，同时适配主控文档的版本切换功能。

### 7.1 文件物理隔离与复制

- **绝对不要直接覆盖历史版本**。

- 在进行 `v1.1` 迭代时，需进入 `prd/` 和 `prototype/` 文件夹，将 `prd_v1.0.html` 和 `prototype_v1.0.html` 复制一份，并重命名为 `prd_v1.1.html` 和 `prototype_v1.1.html`。

- 后续所有的修改仅在 `v1.1` 文件中进行，保留 `v1.0` 作为历史快照。

### 7.2 主控文档版本切换更新

- 迭代新版本后，需更新根目录 `index.html` 主控文档的版本切换下拉菜单，新增新版本选项（如 v1.1），确保菜单选项与 `prd/`、`prototype/` 目录下的版本文件一一对应。

- 优化版本切换逻辑，确保切换至新版本时，左右分栏的 iframe 路径同步更新（如切换至 v1.1 时，PRD 路径为 `./prd/prd_v1.1.html`，原型路径为 `./prototype/prototype_v1.1.html`），联动功能不受影响。

- 提示：如果当前查看的是历史版本，可在主控文档顶部导航栏下方加一条明显的警告横幅（如：“您正在查看历史版本 v1.0，点击此处前往最新版 v1.1”），点击可快速切换至最新版本。

### 7.3 变更日志与双向联动

- 在新版 PRD 的【版本记录】表格中，详细记录本次迭代新增、修改或下线的具体功能点，标注对应功能标识，方便关联核对。

- **PRD 与原型必须强联动**：在 `prd_v1.1.html` 中，所有功能标识需与 `prototype_v1.1.html` 中对应模块的标识保持一致；主控文档切换至 v1.1 版本后，左右联动功能需正常生效。

- 确保新版 PRD 和原型嵌入主控文档后，样式、交互、联动均正常，无错乱或失效问题。
> （注：文档部分内容可能由 AI 生成）
