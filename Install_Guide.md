# Installation Guide: Gemini CLI & Google Antigravity

> **Workshop:** Defying Gravity — AI Agentic Vibe Coding
> **Time needed:** ~15 minutes
> **Prerequisites:** A personal Google account (Gmail)

---

## Part 1: Install Gemini CLI

Gemini CLI is an open-source AI agent that runs in your terminal. It's free to use with a personal Google account (60 requests/min, 1,000 requests/day).

### Step 1: Check for Node.js

Gemini CLI requires Node.js 18 or higher. Open your terminal and run:

```bash
node --version
```

If you see `v18.x.x` or higher, you're good — skip to Step 2.

**If Node.js is not installed or too old:**

- **macOS:** `brew install node` (if you have Homebrew) or download from https://nodejs.org
- **Windows:** Download the installer from https://nodejs.org (LTS version recommended)
- **Linux:** `sudo apt install nodejs npm` (Ubuntu/Debian) or `sudo dnf install nodejs` (Fedora)

### Step 2: Install Gemini CLI

**Option A — Run without installing (recommended for quick start):**
```bash
npx @google/gemini-cli
```

**Option B — Install globally:**
```bash
npm install -g @google/gemini-cli
```
Then launch with:
```bash
gemini
```

### Step 3: Authenticate

When you run Gemini CLI for the first time, it will ask you to sign in with your Google account.

1. Gemini CLI will display a URL — open it in your browser
2. Sign in with your personal Google account (Gmail)
3. Grant the requested permissions
4. Return to your terminal — you should see the Gemini CLI prompt

### Step 4: Verify it works

Type a simple prompt to make sure everything is connected:

```
Hello! Tell me a fun fact about space.
```

If you get a response, you're all set!

### Troubleshooting

| Problem | Fix |
|---------|-----|
| `npx` not found | Install Node.js (see Step 1) |
| Auth fails | Make sure you're using a personal Gmail, not a work/school Google account |
| Rate limit errors | You may have hit the daily limit — wait and try again, or use a Google AI Studio API key |
| Behind a firewall | Ask a mentor — corporate networks may block the auth flow |

---

## Part 2: Install Google Antigravity

Google Antigravity is an AI-powered IDE (code editor) built on VS Code. It's free during public preview.

### Step 1: Download Antigravity

Go to the official download page:

**https://antigravity.google/**

Click the download button for your operating system (Windows, macOS, or Linux).

### Step 2: Install

- **macOS:** Open the `.dmg` file, drag Antigravity to your Applications folder
- **Windows:** Run the installer `.exe` and follow the prompts
- **Linux:** Extract the archive and run the application, or use the `.deb` package:
  ```bash
  sudo dpkg -i antigravity_*.deb
  ```

### Step 3: First Launch Setup

When you open Antigravity for the first time, you'll go through a setup wizard:

1. **Import settings?** Choose "Start fresh" (or import from VS Code/Cursor if you prefer)
2. **Choose a theme:** Pick Dark or Light — your choice
3. **Agent configuration:** Select **"Agent-assisted development"** (recommended)
   - This lets the AI help while you stay in control
   - The AI will ask before making major changes
4. **Terminal policy:** Leave on **"Auto"** — the AI can run standard commands without asking
5. **Sign in:** Use your personal Google account (same one as Gemini CLI)
6. **Select model:** Choose **Gemini 3 Pro** as your default model

### Step 4: Open a workspace

1. Click "Open Folder" in the welcome screen
2. Create a new folder for your hackathon project (e.g., `~/hackathon-project`)
3. Open that folder as your workspace

### Step 5: Test the agent

In the Agent sidebar (right panel), type:

```
Create a file called hello.py that prints "Defying gravity!"
```

If the agent creates the file and you can see it in your editor, you're ready to build!

### Key Features to Know

| Feature | Where | What it does |
|---------|-------|-------------|
| Agent Sidebar | Right panel | Chat with the AI about your code |
| Plan Mode | Toggle in agent sidebar | AI creates a plan before coding (best for complex tasks) |
| Fast Mode | Toggle in agent sidebar | AI acts immediately (best for quick changes) |
| Terminal | Bottom panel | Run your scripts and commands |
| Artifacts Panel | Agent sidebar | See the AI's work trail — plans, screenshots, task lists |
| Browser Preview | Agent sidebar → Preview | AI can open and test your web apps |

### Troubleshooting

| Problem | Fix |
|---------|-----|
| Can't sign in | Use a personal Gmail account, not a work/school account |
| Agent doesn't respond | Check your internet connection; try clicking the model selector to switch models |
| Extensions missing | Antigravity supports VS Code extensions — install them from the Extensions panel |
| Slow performance | Make sure you have at least 8GB RAM; close other heavy applications |

---

## Part 3: Create Your Project

Now that both tools are installed, set up your hackathon project:

### Using Gemini CLI

```bash
# Create and enter your project folder
mkdir hackathon-project
cd hackathon-project

# Start Gemini CLI
gemini
```

Then describe your project:
```
I'm building [describe your chosen track project]. 
Create the initial file structure and a starter file for me.
```

### Using Antigravity

1. Open Antigravity
2. Open your `hackathon-project` folder
3. In the Agent sidebar, describe your project:
```
I'm building [describe your chosen track project].
Create the initial file structure and a starter file for me.
```

### Pro tip: Use both tools together!

- Use **Antigravity** for visual projects (HTML/CSS/JS) — the browser preview is invaluable
- Use **Gemini CLI** for terminal-based projects (Python scripts, CLI tools) — it's faster for iteration
- You can have both open at the same time, pointing at the same folder

---

## Quick Test: The Antigravity Easter Egg

Before we start building, try this in your terminal for a fun Python tradition:

```bash
python -c "import antigravity"
```

*(This is a real Python Easter egg — it opens a classic XKCD comic about Python!)*

---

## Need Help?

- Raise your hand and a mentor will come to you
- Check the **Prompt Guide & Cheat Sheet** for starter prompts
- Gemini CLI: `/help` for available commands
- Antigravity: `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) for the command palette

**You're ready to defy gravity. Let's build!**
