# Builder Guide Module 00–01: Set Up Your Repos & Environment

**Time:** Day 1, 10:30 AM – 12:30 PM (2 hours)
**Feeds:** Tour of the NAIRR ecosystem, both course repos, and your Claude connection

---

## Facilitator Notes *(remove or move to course-toolkit before publishing)*

- This is the highest-risk block in the week for running long; everyone is creating accounts and troubleshooting simultaneously. Budget the first 15 min purely for triage: ask "who is stuck" before walking through steps live.
- Common failure points, in order of frequency: GitHub auth (password vs. token), org vs. personal account confusion, Git not installed despite the pre-event ask, and the Claude Code extension not connecting on the first try (especially in Antigravity; see Step 4 notes). Point people to the troubleshooting section below before doing 1:1 debugging.
- **Some participants would rather skip installing an IDE entirely.** That's fine; Option B throughout this module (GitHub Desktop + Claude Desktop) gets them to the same checkpoint with no code editor and no terminal. Steer people here proactively if they mention unfamiliarity with editors/terminals, rather than waiting for them to get stuck on Option A first.
- **This cohort spans coders and non-coders.** Both groups install the exact same tools in this module; the difference shows up in *how* they use Claude Code (Step 4 has a callout for each). Don't let non-coder instructors assume this module isn't for them; the whole point of the week is that they don't need to write Slurm scripts by hand to build HPC assignments; Claude does that part.
- Target checkpoint: by 12:00 PM everyone should have both repos created and cloned locally, with Claude Code connected, even if the "tour" portion gets compressed.

---

## Who This Is For

This program is open to instructors across disciplines and skill levels; you don't need to already know how to code. The goal of the week is to help you build courses that include real HPC-based assignments, and to use Claude to do the heavy lifting either way:

- **If you code:** Claude Code speeds up writing and debugging the actual scripts your students will run on HPC.
- **If you don't code:** Claude Code writes the scripts *for* you, in plain English, so you can still build and understand HPC assignments without becoming a programmer this week.

Everyone installs the same setup below.

---

## What You'll Need Before Starting

From the pre-event checklist, you should already have:
- [ ] A GitHub account
- [ ] **Option A:** Git installed (`git --version` works in your terminal) and VS Code or Antigravity installed — **or** — **Option B:** GitHub Desktop and Claude Desktop installed (no IDE, no terminal)
- [ ] Morehouse Supercomputing Facility account + MFA set up (not used in this module, but confirm it's done)

**If any of these are missing, stop and fix them first**; trying to debug Git installation *and* repo setup at the same time is the #1 way this block runs over.

---

## Step 0.5: Confirm the Semester and Year

Before anything gets named or written, settle this: **what semester and year is this course for** (Fall/Spring/Summer + year)? It touches almost everything downstream — the syllabus's term line, the schedule's actual calendar dates, any semester-specific policy language, and later (Module 10) exactly what has to change when you reuse this template for your next offering. Write it down somewhere durable now (a note in `CLAUDE.md`, or the first line of `course-site/schedule.md`) rather than leaving it to get inferred later.

## Step 1: Create Your Two Repos from the Template

You're not starting from a blank repo; you're using the pre-built template.

1. Go to the template repos:
   - [`course-site`](https://github.com/whitneynelson/course-site) (this becomes your **public** repo)
   - [`course-toolkit`](https://github.com/whitneynelson/course-toolkit) (this becomes your **private** repo)
2. On each, click the green **"Use this template"** button (top right) → **"Create a new repository"**
3. Name it whatever you'll actually use going forward (e.g., `intro-to-ml-course-site`)
4. Set visibility:
   - `course-site` → **Public**
   - `course-toolkit` → **Private**
5. Click **Create repository**

You now have your own copy of both, under your GitHub account, with no shared history tying back to the template.

Only building a single assignment (Track II)? Name the repo something like `my-assignment-site` instead of `my-course-site`; everything downstream still works, it's just a folder name.

---

## Step 2: Clone Both Repos Locally

**Option A (Git + editor):** open your terminal (or the terminal inside VS Code / Antigravity):

```bash
git clone https://github.com/YOUR-USERNAME/your-course-site.git
git clone https://github.com/YOUR-USERNAME/your-course-toolkit.git
```

Open both folders in your editor. You should see the full file structure already in place; `syllabus.md`, `schedule.md`, `modules/`, `builder-guide/` in course-site; `grading-scale.md`, `rubrics/`, `exams/` in course-toolkit.

**Option B (GitHub Desktop, no terminal):** open GitHub Desktop → **File → Clone Repository** → pick each repo from your account → choose where to save them. You should see the same file structure on disk; you just won't be editing it directly, since Claude Desktop handles reads/writes for you in Step 4.

---

## Step 3: Walk the Environment

Before building anything, orient yourself:

- **course-site** = everything a student will eventually see. Nothing goes in here until you're ready for it to be public.
- **course-toolkit** = grading, exams, attendance, your real prep notes. Never gets published.
- **builder-guide/** (inside course-site) = this walkthrough itself, numbered 00–10, one module per accelerator session.

Take 5 minutes to open a few files in each repo and skim the placeholder structure; you'll be filling these in over the rest of the week.

### Why repo structure matters

These two folders aren't just storage; they're the environment Claude works inside all week, and a well-organized one makes every prompt you write from here forward more effective. Notice that `course-site` already ships with a `CLAUDE.md` (root instructions for how Claude should operate in that repo) and a `skills/` folder (step-by-step guides Claude reads before walking you through each module). That's deliberate: a README stating intent, docs explaining decisions, and clear guardrails give Claude the same context a new collaborator would need, so it plans and writes better with less back-and-forth. Keep that same discipline as you build out your own course content; the more your repo documents itself, the less you'll have to re-explain to Claude in every session.

---

## Step 4: Connect Claude

### Option A: Claude Code (VS Code or Antigravity)

Claude Code is the extension that lets you talk to Claude directly inside your editor; it can read your files, write and edit code, and run commands, all from a sidebar panel.

**In VS Code:**
1. Open the Extensions view: `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows/Linux)
2. Search **"Claude Code"** and click **Install** (look for the official Anthropic publisher)
3. Open any file in your project; a small orange spark icon (✱) will appear in the top-right of the editor toolbar
4. Click it, then sign in with your Anthropic account when prompted. A Claude Pro, Max, Team, or Enterprise plan works; no separate API key needed.

**In Antigravity:**
1. Open the Extensions panel with the same shortcut (`Cmd+Shift+X` / `Ctrl+Shift+X`)
2. Search **"Claude Code"** and install the official Anthropic extension (Antigravity installs extensions from the Open VSX registry, not the Microsoft Marketplace; this should still find it)
3. Open the Claude Code panel from the Spark icon in the sidebar
4. Sign in when prompted. Note: Antigravity's integration currently expects a Claude Pro/Max/Team/Enterprise account **or** an Anthropic API key with credits; if sign-in doesn't work smoothly, the API key route is the more reliable fallback right now, since this integration is newer than the VS Code one.

**If the extension won't connect in either editor** (this happens more often in Antigravity, which is still in preview), fall back to the command-line version, which works the same everywhere:
```bash
npm install -g @anthropic-ai/claude-code
```
Then run `claude` in your editor's integrated terminal.

### Option B: Claude Desktop (no IDE)

For participants who'd rather not install a code editor: Claude Desktop is the standalone chat app, paired with a filesystem connector so Claude can read and write your course files directly, the same job Claude Code does inside an editor.

1. Download Claude Desktop from [claude.ai/download](https://claude.ai/download) and sign in. A Claude Pro, Max, Team, or Enterprise plan works.
2. Go to **Settings → Connectors** and enable the **Filesystem** connector.
3. Point it at the folder containing your cloned `course-site` and `course-toolkit` repos (from Step 2, Option B).
4. Claude can now read and write files in that folder from a normal chat conversation; there's no sidebar panel or spark icon, since there's no editor involved.

Git operations (creating, committing, publishing) go through GitHub Desktop instead of the command line; see Step 2.

### Using it; coders vs. non-coders

Once connected, everyone uses the same chat panel, but the prompts look different depending on your comfort level:

- **If you code:** you can ask Claude to write, refactor, or debug directly; e.g., *"Refactor this data-loading function to run in parallel across nodes."*
- **If you don't code:** describe what you want in plain language and let Claude produce the script; e.g., *"Write a Slurm batch script that runs my Python script `analyze.py` on 4 nodes for 2 hours, and explain each line so I understand what it's doing."*

Either way works. The point of this week is that "building an HPC assignment" doesn't require you to already know Slurm, Python, or bash; it requires knowing what you want the assignment to *do*, and letting Claude handle the syntax.

---

## Troubleshooting

These are the exact issues most likely to come up in this block; if you hit one, check here before flagging a facilitator.

### Option A (Git/terminal)

**"Password authentication is not supported for Git operations"**
GitHub no longer accepts your account password for `git push`/`git clone` over HTTPS. You need a Personal Access Token instead:
1. Go to [github.com/settings/tokens](https://github.com/settings/tokens) → **Generate new token (classic)**
2. Check the **`repo`** scope
3. Generate it and **copy it immediately**; GitHub only shows it once
4. When Git prompts for a password, paste the token instead

**"Repository not found"**
Almost always a typo or mismatch in the URL. Check:
- Does the repo actually exist yet under your account? (github.com/YOUR-USERNAME)
- Is it under your personal account, or did it get created under an organization? The URL differs (`github.com/your-username/...` vs. `github.com/org-name/...`)

**403 error when pushing**
Usually a stale cached credential from before you had a token. Clear it and let Git re-prompt:
- **Mac:** Keychain Access → search "github.com" → delete the entry
- **Windows:** Control Panel → Credential Manager → Windows Credentials → remove the `git:https://github.com` entry
- **Any OS:** `git credential-cache exit`

Then check your remote URL is exact (no stray trailing slash):
```bash
git remote -v
git remote set-url origin https://github.com/YOUR-USERNAME/your-repo.git
```

**Claude Code extension doesn't show up, or the Spark icon is missing**
- Make sure you have an actual *file* open, not just a folder; the icon only appears with a file active.
- Try **"Developer: Reload Window"** from the Command Palette.
- In Antigravity specifically, there's a known issue where the CLI doesn't recognize the extension is installed. If this happens, use the standalone CLI fallback above instead of troubleshooting the extension further; it's faster and works identically.

### Option B (GitHub Desktop / Claude Desktop)

**GitHub Desktop won't sign in, or can't find the repo**
Confirm it's signed into the same GitHub account that owns the repo (**File → Options** on Windows, **GitHub Desktop → Preferences** on Mac → **Accounts**), and that the repo was actually created from the template in Step 1 before trying to clone it.

**Claude Desktop can't read the files, or says the folder is empty**
Check **Settings → Connectors → Filesystem** is enabled and pointed at the exact folder holding the cloned repos, not a parent folder or a different location. If you moved the repos after connecting, you'll need to re-point the connector.

---

## Checkpoint

By the end of this block, you should have:
- [ ] Semester and year confirmed (Fall/Spring/Summer + year) and noted somewhere durable
- [ ] `course-site` repo created (public) and cloned locally
- [ ] `course-toolkit` repo created (private) and cloned locally
- [ ] Both folders open in your editor and briefly explored, or visible to Claude Desktop via the Filesystem connector
- [ ] Claude Code installed and connected (Option A), or Claude Desktop with the Filesystem connector enabled (Option B)
- [ ] One test prompt sent successfully; coders can try asking it to explain a file in the repo; non-coders can try asking it to write a one-line Slurm script and explain what it does

If you're not there by 12:00 PM, flag it now rather than trying to catch up during lunch; the afternoon sessions build directly on this.
