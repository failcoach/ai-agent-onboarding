# Getting Set Up

This page walks you through everything you need before you can start the interview. If you already have Claude Code installed, skip to step 3.

## What You'll Need

- A computer with internet access
- An Anthropic account (this is the company behind Claude). Claude Code is a paid tool. Plans start at $20/month. You can sign up at [console.anthropic.com](https://console.anthropic.com)
- About 30 minutes for the installation and the interview

That's it. No programming knowledge required.

## Step 1: Install Claude Code

Claude Code is a tool made by Anthropic that lets you work with Claude directly on your computer. It's what makes the interactive interview in this starter kit work.

You have two options:

**Option A: VS Code extension (recommended if you're not technical)**

VS Code is a free text editor from Microsoft. If you don't have it yet:
1. Download VS Code from [code.visualstudio.com](https://code.visualstudio.com)
2. Install it like any other app
3. Open VS Code
4. Click the Extensions icon on the left sidebar (it looks like four small squares)
5. Search for "Claude Code"
6. Click Install

**Option B: Terminal (if you're comfortable with it)**

Follow the official guide: [Claude Code Getting Started](https://docs.anthropic.com/en/docs/claude-code/getting-started)

## Step 2: Download This Starter Kit

Go to this project's page on GitHub. Look for the green **Code** button near the top right. Click it and choose **Download ZIP**.

Unzip the file. You'll get a folder called `ai-agent-onboarding`. Put it somewhere you can find it (your Desktop is fine).

If you're comfortable with the terminal and have git installed, you can also run:
```
git clone https://github.com/failcoach/ai-agent-onboarding.git
```

## Step 3: Open It in Claude Code

**If you're using VS Code:**
1. Open VS Code
2. Go to File > Open Folder
3. Select the `ai-agent-onboarding` folder you downloaded
4. Open the Claude Code panel (look for the Claude icon in the left sidebar)

**If you're using the terminal:**
1. Open your terminal
2. Navigate to the folder: `cd path/to/ai-agent-onboarding` (replace `path/to` with where you put it -- if it's on your Desktop, that's `cd ~/Desktop/ai-agent-onboarding`)
3. Type `claude` and press Enter

## Step 4: Start the Interview

Once Claude Code is open and you can see the chat, type:

**"Read this project and help me build my first agent"**

Claude will read the project files, understand what this starter kit is, and start walking you through the interview. The whole process takes about 20-30 minutes.

## If Something Goes Wrong

- **Claude Code asks for a login or API key:** You need an Anthropic account. Sign up at [console.anthropic.com](https://console.anthropic.com) and follow the setup instructions.
- **You can't find the Claude Code panel in VS Code:** Make sure you installed the Claude Code extension (step 1). You might need to restart VS Code.
- **Claude doesn't seem to know about the starter kit:** Make sure you opened the `ai-agent-onboarding` folder itself, not a parent folder. Claude Code reads the files in whatever folder you open.
- **Something else:** The [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/overview) has troubleshooting guides, or you can reach out to Miha (links at the bottom of the README).
