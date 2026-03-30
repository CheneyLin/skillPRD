# QQ PRD SKILL

Through a 7-step agile workflow including conversational requirement collection, PRD skeleton drafting, HTML prototype generation (with frontend design), Mermaid flowchart drawing, and the final PRD with an iframe linked navigation structure, guide new PMs to complete the entire process.

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
