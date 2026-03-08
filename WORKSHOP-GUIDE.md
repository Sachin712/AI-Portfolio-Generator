# Workshop Guide — Build & Deploy Your Portfolio with AI

Welcome! In this workshop you will use an **AI coding assistant** to build a personal portfolio website from scratch — without writing code yourself. You will guide the AI with prompts, and it will write all the code for you. By the end, your portfolio will be **live on the internet** with a real URL you can share.

**No coding experience needed.** Seriously.

---

## What You Will Need

| Tool | What It Is | How to Get It |
|---|---|---|
| **A code editor with AI** | Where you edit your files with AI help | See "Choose Your AI Assistant" below |
| **A web browser** | To preview your site | Chrome, Firefox, Edge — anything works |
| **A GitHub account** | To store your code and host your site for free | You already have one! |
| **Git** | Version control tool (used behind the scenes) | [Download Git](https://git-scm.com/downloads) — you may already have it |

### Choose Your AI Assistant

Pick **one** of these — they all work with this workshop:

| Option | Best For | Setup |
|---|---|---|
| **VS Code + GitHub Copilot** | Students with Copilot access | Install [VS Code](https://code.visualstudio.com/), sign in with GitHub, enable Copilot Chat |
| **Cursor** | Free AI-powered editor | Download from [cursor.com](https://www.cursor.com) |
| **VS Code + ChatGPT/Claude** | If you don't have Copilot | Use VS Code for editing + a browser tab with [chatgpt.com](https://chatgpt.com) or [claude.ai](https://claude.ai) |
| **Windsurf** | Another free AI editor | Download from [windsurf.com](https://windsurf.com) |

> **Don't overthink this choice.** If you already have VS Code with Copilot, use that. Otherwise, Cursor is the easiest to get started with.

---

## Part 1 — Set Up Your Project (10 minutes)

### Step 1: Create a GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. **Repository name:** `my-portfolio` (or whatever you like)
3. **Description:** "My personal portfolio website"
4. Select **Public**
5. Check **"Add a README file"**
6. Click **Create repository**

### Step 2: Open It in Your Editor

**If using VS Code / Cursor / Windsurf:**

1. On your new repo's page, click the green **"<> Code"** button
2. Copy the HTTPS URL
3. Open your editor
4. Open the terminal (`` Ctrl + ` `` or View > Terminal)
5. Type these commands (replace the URL with yours):
   ```
   cd Desktop
   git clone https://github.com/YOUR-USERNAME/my-portfolio.git
   cd my-portfolio
   ```
6. Open the folder in your editor: **File > Open Folder** and select `my-portfolio`

### Step 3: Create the File Structure

In your editor's terminal, run these commands to create the folders and files:

**Windows (PowerShell):**
```
New-Item -ItemType Directory -Path "css", "js", "assets/images" -Force
New-Item -ItemType File -Path "index.html", "css/styles.css", "js/main.js" -Force
```

**Mac / Linux:**
```
mkdir -p css js assets/images
touch index.html css/styles.css js/main.js
```

Your project should now look like this:
```
my-portfolio/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── assets/
│   └── images/
└── README.md
```

---

## Part 2 — Give the AI Its Instructions (5 minutes)

### Step 4: Set the Context

Open the file called **`chatGPT-prompt-v2.md`** (provided by your instructor). This file tells the AI *what* you are building and *how* it should write the code.

**How to use it depends on your tool:**

| Tool | How to Set Context |
|---|---|
| **GitHub Copilot Chat** (VS Code) | Open the Chat panel (Ctrl+Shift+I), paste the entire contents of chatGPT-prompt-v2.md as your first message |
| **Cursor** | Open the Composer (Ctrl+I), paste the chatGPT-prompt-v2.md contents, or add it as a file reference using @chatGPT-prompt-v2.md |
| **ChatGPT / Claude** | Open a new chat, paste the entire contents of chatGPT-prompt-v2.md as your first message |
| **Windsurf** | Open Cascade (Ctrl+L), paste the contents as your first message |

> **Important:** Do this FIRST before any other prompts. It sets up the "rules" for the entire conversation — things like color palette, fonts, file structure, and design style.

---

## Part 3 — Build Your Portfolio (60–90 minutes)

### Step 5: Follow the Prompts

Open the **`PROMPTS.md`** file (provided by your instructor). It contains a series of prompts organized in phases.

**The workflow is simple:**

1. **Copy** a prompt from PROMPTS.md
2. **Replace** anything in `[brackets]` with your own info (or leave the placeholders for now)
3. **Paste** the prompt into your AI assistant
4. **Wait** for the AI to generate the code
5. **Copy** the generated code into the correct file (`index.html`, `css/styles.css`, or `js/main.js`)
6. **Save** the file (Ctrl+S)
7. **Preview** in your browser (see below)
8. **Repeat** with the next prompt

### How to Preview Your Site

**Easiest way:** Find `index.html` in your file explorer (not the code editor) and double-click it. It opens in your browser.

**Better way (live reload):**

- **VS Code:** Install the "Live Server" extension → right-click `index.html` → "Open with Live Server"
- **Cursor:** Same as VS Code — install Live Server from Extensions
- **Any editor:** Install the Live Server extension or use the terminal:
  ```
  npx live-server
  ```

> **Tip:** Keep your browser and editor side by side so you can see changes instantly.

### What If Something Goes Wrong?

| Problem | Solution |
|---|---|
| The page is blank | Check that `index.html` has content. Make sure the CSS and JS file paths are correct in the HTML. |
| Styles aren't showing | Make sure the `<link>` tag in HTML points to `css/styles.css` (not just `styles.css`) |
| AI gave partial code | Tell the AI: "Give me the COMPLETE file, not just the changes" |
| Something looks broken | Tell the AI: "The [section] looks broken. Here is what I see: [describe the problem]. Fix it and give me the complete updated files." |
| AI is confused or off track | Start a new conversation and paste chatGPT-prompt-v2.md again |
| The code is too complex | Tell the AI: "Simplify this. Use only basic HTML, CSS, and JavaScript. No frameworks." |

---

## Part 4 — Deploy to GitHub Pages (15 minutes)

Your portfolio is about to go live on the internet!

### Step 6: Push Your Code to GitHub

In your editor's terminal:

```
git add .
git commit -m "My portfolio site"
git push
```

> If asked to log in, follow the prompts. You may need to create a [Personal Access Token](https://github.com/settings/tokens) if using HTTPS.

### Step 7: Enable GitHub Pages

1. Go to your repository on github.com (e.g., `github.com/YOUR-USERNAME/my-portfolio`)
2. Click **Settings** (tab at the top)
3. In the left sidebar, click **Pages**
4. Under **"Source"**, select **"Deploy from a branch"**
5. Under **"Branch"**, select **main** and **/ (root)**
6. Click **Save**
7. Wait 1–2 minutes, then refresh the page

You'll see a message like:

> **Your site is live at** `https://YOUR-USERNAME.github.io/my-portfolio/`

**That is your live portfolio URL!** Open it. Share it. Put it on your resume.

---

## Part 5 — Personalize & Polish (Remaining Time)

### Step 8: Add Your Real Content

Go back to **PROMPTS.md → Phase 8** and use the personalization prompt to replace all placeholder content with your real:

- Name and bio
- Profile photo (drop your photo into `assets/images/`)
- Project images and descriptions
- Skill list
- Social media links

### Step 9: Try the Bonus Prompts

If you have extra time, check out the **Bonus Prompts** at the bottom of PROMPTS.md. Fun options like:

- Dark/Light mode toggle
- Custom animated cursor
- Project detail modals
- Typing animation effect

### Step 10: Push Your Updates

Every time you make changes you're happy with:

```
git add .
git commit -m "Update portfolio with my content"
git push
```

GitHub Pages automatically redeploys. Your live site updates in about a minute.

---

## Quick Reference

| Action | Command / Step |
|---|---|
| Preview locally | Double-click `index.html` or use Live Server |
| Save your work | `git add .` → `git commit -m "message"` → `git push` |
| See your live site | `https://YOUR-USERNAME.github.io/my-portfolio/` |
| Reset the AI | Start a new conversation, paste chatGPT-prompt-v2.md again |
| Ask AI to fix something | "This section looks broken. Here's what I see: [describe]. Fix it." |
| Ask AI to change design | "Change the accent color to [color]" or "Make the layout more [adjective]" |

---

## You're Done!

You just used AI to build and deploy a professional portfolio website. The site is live, it's yours, and you can keep improving it anytime.

**What you demonstrated today:**
- How to guide an AI assistant to write code for you
- How to structure and deploy a web project
- How prompt engineering shapes the output you get
- That you don't need to be a programmer to build on the web
