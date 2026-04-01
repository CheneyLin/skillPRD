# QQ PRD SKILL

Through a 7-step agile workflow including conversational requirement collection, PRD skeleton drafting, HTML prototype generation (with frontend design), Mermaid flowchart drawing, and the final PRD with an iframe linked navigation structure, guide new PMs to complete the entire process.

# Quick Start

1. Create a new project
2. Create a PRF.MD file and confirm project information and basic requirement descriptions
3. Invoke the Skill to generate a PRD.MD file, and verify that the content is complete and accurate
4. Continue executing the Skill to generate HTML prototype files, and verify that the content is complete and accurate
5. Iterate on the PRD.MD file until you are satisfied

# Installation

## Install Trae IDE

- Mainland China: [https://www.trae.cn/](https://www.trae.cn/)

- International: [https://www.trae.ai/](https://www.trae.ai/)

## Download and Install QQ-PRD_Skill

Download QQ-PRD_Skill to your local machine.

```Bash
git clone https://github.com/CheneyLin/skillPRD.git
```

You can also download the ZIP file from the GitHub homepage.

Copy and rename the `qq-prd_skill` folder, then place it in the global skills directory of your AI assistant.

You may rename the `qq-prd` folder to `qq-prd_skill` or keep the default name `qq-prd` before copying it to the global skills directory.

### For Mac:

Locate your user directory, find the `.trae` folder, and copy `qq-prd_skill` into it.

Example:

```Plain Text
/Users/linyu/.trae/skills
```

The tilde `~` represents the current user directory:

```Plain Text
~/.trae/skills/qq-prd_skill
```

### For Cursor or VS Code:

```Plain Text
~/.cursor/skills/qq-prd_skill
~/.vscode/skills/qq-prd_skill
```

# Usage in Projects

Following the CodeX Skill specification, organize your project folder structure as follows:

```Bash
├── .agents
│   ├── skills
│       ├── qq-prd_skill
├── document
│   ├── prf.md
```

## How to Use

### Full AI Startup

In the AI chat dialog, type `/qq-prd` and send it, then describe your new project idea. The AI will automatically create the standard folder structure and guide you step-by-step to produce professional requirements documents!

```bash
/qq-prd
```
If your IDE does not support SKILL, you need to manually invoke the SKILL. Add the PRF.MD file and SKILL.MD file to the chat window:

```bash
call skill /qq-prd start with prf.md
```

### PRF (Product Requirements Form) Startup

Start efficiently with an initialized product requirements collection template:

```Bash
├── document
│   ├── prf.md
```

Write requirements in Markdown format. The template is available in the Skill directory: `/qq-prd/reference/prf.md`.

```Bash
# Product Requirements Form

## Project Name
Quiz Game

## Requirements Description
1. **Background/Pain Points**
Solve user retention issues and increase user engagement.

2. **Business Goals**
Users answer questions in the quiz game to earn rewards.

3. **Users & Scenarios**
Add a quiz game module in the app where users can answer questions and earn rewards.

4. **Core User Journey**
Users answer questions in the quiz game to earn rewards.

5. **Product Scope**
- Add a quiz game management module in the admin backend to manage questions, rewards, etc.
- Add a quiz game module in the app where users can answer questions and earn rewards.

6. **Existing Solutions**
None

7. **References/Competitors**
None

## Additional Requirements
None
```

Save the completed PRF file to the `document` folder in your project. Add it to the chat window, type `/qq-prd`, and send it. The AI will automatically create the standard folder structure and guide you step-by-step to produce professional requirements documents.

Some AI models may prompt you to完善 incomplete sections in the PRF file; follow the prompts to refine it.

## PRD Workflow

### Working File Structure

If the AI model runs correctly, it will automatically create the standard folder structure. Using project name `QUIZGAME` as an example:

```Bash
├── QUIZGAME_PRD
│   ├── index.html
│   ├── v1.0
│       ├── prd_md
│       ├── prd_html
│       ├── prototype_html
│   ├── history
```

This is called a **PRD Package**, which is the final deliverable. It contains all project PRD files: requirements document, PRD skeleton, HTML prototype, Mermaid flowcharts, etc.

### Confirm [PRD.MD](PRD.MD) File

The AI will automatically generate the `PRD.MD` file and ask you to confirm details. You may manually edit `PRD.MD` at this stage.

After confirmation, ask the AI to generate:

- PRD HTML file

- Prototype HTML file

- Main controller HTML file (`index.html`)

Open `index.html` in a browser to view the PRD Package.

### Iterate [PRD.MD](PRD.MD) File

Continue iterating on `PRD.MD` until you are satisfied with the PRD Package.

After each modification to `PRD.MD`, confirm the details and ask the AI to regenerate the PRD HTML and Prototype HTML files.

For significant feature changes or team alignment, create new versions (AI-assisted or manual).

Add the latest version of `PRD.MD` to the chat window and use these AI commands to update the PRD Package:

```Bash
PRD.MD confirmed. Please update the PRD HTML file.
```

```Bash
Confirmed. Please update the Prototype HTML file.
```

```Bash
New version confirmed. Please update the main index.html file.
```

It is recommended to ask the AI to generate a summary log of changes in MD format and save it to the `history` folder during AI processing:

```Bash
PRD.MD confirmed. Please update the PRD HTML file, Prototype HTML file, main index.html file, and the log file in the history folder.
```

# AI Prompt Commands

## Standard Workflow Commands

### Complete PRD Package Update

When confirming PRD.MD and needing to update all related files:

```bash
PRD.MD confirmed. Please update the PRD HTML file, Prototype HTML file, main index.html file, and the log file in the history folder.
```

---

## Error Correction & Model Switching

During actual usage, AI may generate documents with errors, PRD and prototype may become out of sync, or certain models may perform poorly on specific tasks. Below are standardized prompts for different scenarios to help you quickly correct issues.

### 1. Document Content Error Correction

**Scenario**: The HTML format PRD document generated by AI contains errors (such as formatting issues, missing content, broken tables, etc.).

**Prompt**:
```bash
Please regenerate the HTML format PRD document (prd_v1.0.html) based on the Markdown format PRD source document (prd_v1.0.md).

Requirements:
1. Strictly use /assets/prd_template.html template style and structure
2. Ensure HTML content matches Markdown content exactly
3. Preserve all feature identifiers (id) and "View Prototype" buttons
4. Check and fix all tables, cards, buttons, and other UI elements
```

### 2. Prototype File Error Correction

**Scenario**: The HTML format prototype file has issues (such as interaction failures, styling errors, missing pages, etc.).

**Backend/PC Web Prototype Correction Prompt**:
```bash
Please regenerate the admin management prototype file (admin_v1.0.html).

Requirements:
1. Strictly reference /assets/admin_prototype_template.html template structure and style
2. Implement all sub-page prototype display and interaction simulation
3. Support global view switching and specific interface highlight positioning (Focus Mode)
4. Preserve postMessage communication logic to ensure normal linkage with master document
5. Use Element UI component library, maintain Material Design style
```

**Mobile/H5 Prototype Correction Prompt**:
```bash
Please regenerate the mobile prototype file (h5_v1.0.html or app_v1.0.html).

Requirements:
1. Strictly reference /assets/app_prototype_template.html template structure and style
2. Fixed phone size 390x844px, simulating real phone proportions
3. Default to responsive grid layout (global view), support switching to single-page interaction mode
4. Must include [Global View] and [Reset] floating buttons
5. Support URL anchor automatic highlight positioning (e.g., #home, #quiz)
6. Use Tailwind CSS, maintain modern minimalist design style
7. All pages prevent overflow; strictly avoid absolute positioning exceeding container width
```

### 3. PRD and Prototype Synchronization Correction

**Scenario**: PRD document has been updated but prototype is not synchronized; or prototype has been adjusted but PRD is not updated in real-time.

**Bidirectional Synchronization Prompt**:
```bash
PRD and prototype need to be synchronized. Please execute the following operations:

1. Update prd_v1.0.html based on the latest prd_v1.0.md
2. Update admin_v1.0.html based on the latest prototype adjustments
3. Ensure PRD feature identifiers match prototype data-prototype attributes one-to-one
4. Test left-right linkage function: prototype automatically highlights when scrolling PRD
5. Update version switch configuration in index.html master document

Checklist:
- [ ] Each PRD functional module has a "View Prototype" button
- [ ] Each prototype functional module has a data-prototype attribute
- [ ] Focus mode works normally
- [ ] All file paths comply with directory architecture specification
```

### 4. Switching AI Model

**Scenario**: The current AI model performs poorly on specific tasks (such as weak frontend design capability, poor logic understanding), requiring a switch to a more capable model.

**General Switch Prompt**:
```bash
Based on qq-prd skill workflow specification, please complete the following task:

[Specific task description, e.g., Complete admin_v1.0.html to implement all sub-project prototype display and interaction simulation]

Requirements:
1. Strictly follow corresponding templates in /assets directory
2. Maintain consistency with prd_v1.0.md content
3. Ensure all interaction functions and linkage logic work normally
```

**Frontend Design Model Switch Prompt**:
```bash
I need to switch to an AI model proficient in frontend design to complete high-fidelity prototype development.

Task: Based on qq-prd skill, strictly reference ./qq-prd/assets/admin_prototype_template.html template, regenerate admin_v1.0.html.

Technical Requirements:
1. Use Element UI component library (or my specified UI library: Ant Design/Element Plus, etc.)
2. Implement complete list page, form page, popup, and other interactions
3. Support URL Hash routing for page switching
4. Add Focus Mode support (?focus=feature_id parameter)
5. Preserve postMessage communication interface to support PRD linkage

UI Style Requirements:
[Choose one style]
- Minimalist Efficient Style: Light color background, card layout, rounded corner design
- Tech Texture Style: Neutral gray background, slight shadows, gradient color buttons
```

**Logic Understanding Model Switch Prompt**:
```bash
I need to switch to an AI model proficient in business logic understanding to improve PRD documentation.

Task: Based on preliminary requirements, complete the detailed solution chapter of prd_v1.0.md.

Requirements:
1. Organize document according to /assets/prd_template.md structure
2. Add unique identifier for each functional module (e.g., feature_01, strategy_create)
3. Supplement complete business rules, prerequisites, exception handling
4. Draw Mermaid flowcharts (flowchart TD or sequenceDiagram)
5. Ensure logical closure without ambiguity
```

### 5. Master Document Linkage Failure Correction

**Scenario**: The left-right linkage function of index.html master document fails, version switching doesn't work, or iframe paths are incorrect.

**Master Document Repair Prompt**:
```bash
Please regenerate the master document index.html to fix the linkage function.

Requirements:
1. Strictly reference /assets/index_template.html template structure and style
2. Top navigation bar includes: project name, version switch dropdown menu, product type switch buttons
3. Main area left-right split at 50% each, supports drag-to-adjust width (30%-70%)
4. Left iframe embeds PRD document, right iframe embeds prototype
5. Implement left-right linkage function:
   - Listen to PRD scroll events, automatically highlight prototype corresponding module
   - Click "View Prototype" button to manually trigger prototype positioning
   - Communicate between iframes via postMessage
6. Update both iframe src paths synchronously when switching versions
7. Use localStorage to save split layout state

File Path Examples:
- v1.0 PRD: ./v1.0/prd_html/prd_v1.0.html
- v1.0 Prototype: ./v1.0/prototype_html/admin_v1.0.html
```

### 6. Version Iteration Specification

**Scenario**: Upgrading from v1.0 to v1.1, need to preserve historical versions while creating new versions.

**Version Iteration Prompt**:
```bash
The project needs to iterate to version v1.1. Please execute the following operations:

1. Copy historical version files (do not overwrite):
   - Copy prd_v1.0.html → prd_v1.1.html
   - Copy admin_v1.0.html → admin_v1.1.html
   - Copy h5_v1.0.html → h5_v1.1.html

2. Add to prd_v1.1.html [Version History] table:
   | Version | Date | Content |
   | v1.1 | 2026-03-31 | [Details of this iteration's changes] |

3. Update index.html master document:
   - Add v1.1 option to version switch dropdown menu
   - Configure iframe paths for v1.1 version

4. Generate iteration log:
   - Filename: history/ai_2026_03_31_v1.1_update.md
   - Content: Change summary, impact scope, test results

Note: Preserve v1.0 as historical snapshot; all modifications only in v1.1 files.
```

### 7. Complete PRD Package Rebuild

**Scenario**: PRD package is chaotic, files are missing, or there are multiple inconsistencies requiring complete rebuild.

**Complete Rebuild Prompt**:
```bash
Please completely rebuild the PRD package based on qq-prd skill workflow specification.

Input File: document/prf.md (or latest prd_v1.0.md)

Output Structure:
├── QUIZGAME_PRD
│   ├── index.html          (Master Document)
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

Execution Steps:
1. Confirm PRD.MD content is complete and accurate
2. Generate prd_v1.0.html (using prd_template.html template)
3. Generate admin_v1.0.html (using admin_prototype_template.html template)
4. Generate h5_v1.0.html (using app_prototype_template.html template)
5. Generate index.html (using index_template.html template)
6. Configure all feature identifiers and linkage logic
7. Generate delivery checklist

Delivery Checklist:
- [ ] All HTML files can run independently
- [ ] index.html opens normally with left-right split display
- [ ] Version switch function works normally
- [ ] Left-right linkage function works (automatic + manual)
- [ ] Prototype Focus mode works normally
- [ ] All file paths are correct
```

---

## Best Practice Recommendations

1. **Timely Confirmation**: After completing each step, immediately open it in a browser to check and correct issues promptly.

2. **Small Iterations**: Do not ask AI to complete all work at once; confirm each step before proceeding to the next.

3. **Preserve History**: Copy a historical version for each iteration to facilitate comparison and backtracking.

4. **Manual Verification**: After AI generation, manually check key functions (such as linkage, version switching) to ensure they work properly.

5. **Log Recording**: Ask AI to generate modification logs and save them to the history folder for team collaboration and tracing.

6. **Template Priority**: All documents must use corresponding templates under /assets to ensure uniform formatting.

---

# FAQ

## How to Show Hidden Folders

### On Mac: Use the shortcut `Command + Shift + .` (period) to toggle hidden files/folders.

1. Open Finder (any window or desktop).

2. Press `Command + Shift + .` – hidden files/folders will appear (semi-transparent).

3. Press the same shortcut again to hide them.

## How to Access a Specific (Hidden) Folder

### On Mac: Use `Command + Shift + G` to quickly navigate to a specific (hidden) folder.

1. Open Finder (any window or desktop).

2. Press `Command + Shift + G` – a "Go to Folder" dialog will appear.

3. Enter the folder path, e.g., `/Users/linyu/.trae/skills/qq-prd_skill`.

4. Click **Go** to access the folder.
