# Toolbox 0: Get Your Tools Ready

Before your Quarter starts, there are a few things to set up on your computer. None of this requires coding knowledge — just following steps. Total time is about **65 minutes** if everything goes smoothly — budget closer to **90** if you're brand new to any of this. Each part below has its own time estimate so you can see how far along you are. **Part 6 (Node.js/npm) adds ~10 more minutes, but only if it applies to your track** — see that section for who needs it.

Do this **before Day 1**. If you get stuck on any step, email **talassify@gmail.com** and we'll help you sort it out — don't wait until kickoff week.

---

## What you're setting up

| Tool | Why you need it |
|---|---|
| VS Code | The program you'll write and edit code in |
| Browser DevTools | Where you'll preview and debug your HTML/CSS/JS |
| GitHub | Where your code lives and where you'll show your work |
| Git | The tool that moves your code from your computer onto GitHub |
| Discord | Where your Quarter, mentors, and toolbox help channels live |
| Node.js / npm / nvm | *(Conditional — see Part 6)* Needed to run JavaScript framework tooling like Vue |

---

## Part 1: Install VS Code — ~10 minutes

VS Code (Visual Studio Code) is free, and it's what you'll use to write every line of code in this program.

1. Go to **[code.visualstudio.com](https://code.visualstudio.com)**
2. Click the big download button — it'll automatically detect whether you're on Windows or Mac
3. Open the downloaded file and click through the installer using the default options
4. Once it's installed, open VS Code. If you see a blank window with a sidebar on the left, you're done.

**Optional but recommended:** Once you're in VS Code, click the square icon on the left sidebar (Extensions) and install:

- **Live Server** — lets you preview HTML pages in your browser as you build
- **ESLint** — flags mistakes in your code as you type

You don't need to understand these yet. Just have them installed so they're ready when your toolbox exercises need them.

---

## Part 2: Get Comfortable With Your Browser's DevTools — ~5 minutes

Every browser has built-in tools for inspecting and debugging web pages — you'll use this constantly once you start building HTML/CSS/JS, so it's worth a five-minute look now rather than discovering it mid-exercise.

1. Use **Chrome** or **Firefox** if you have a choice — both have strong DevTools. If you don't have either, download **[Chrome](https://www.google.com/chrome/)**.
2. Open any website, then right-click anywhere on the page and select **Inspect** (or press `F12` / `Ctrl+Shift+I` on Windows, `Cmd+Option+I` on Mac)
3. A panel opens showing the page's HTML. Click around a few elements — notice the page highlights whatever you're hovering over in the panel
4. Click the **Console** tab at the top of that panel. This is where error messages show up when your code breaks — you'll be looking at this a lot
5. Close the panel (same shortcut as step 2, or click the X). That's it — you don't need to do anything else here, just know it exists and how to open it

---

## Part 3: Create Your GitHub Account — ~15 minutes

GitHub is where your code gets saved, versioned, and shown off. It's also where facilitators will look at your work.

1. Go to **[github.com](https://github.com)** and click **Sign up**
2. Choose how you want to sign up — pick whichever you're most comfortable with:
   - **Email + password** — enter the email address you used for your Talassify application, then create a password and username
   - **Continue with Google** — sign up using your existing Google account
   - **Continue with Apple** — sign up using your existing Apple ID
   - If you use Google or Apple, your GitHub email will be whatever's tied to that account — that's fine, just let us know if it's different from the email on your application
3. Choose a username if you're prompted to
   - Pick something professional — this may end up on your portfolio, resume, or LinkedIn
4. Verify your email (check your inbox for a code from GitHub)
5. When asked about your experience level, answer honestly — it just personalizes GitHub's own onboarding tips, it doesn't affect your standing in the program

**Optional but recommended:** Turn on two-factor authentication (Settings → Password and authentication). It's a good habit and GitHub increasingly nudges everyone toward it anyway.

### Exercise: Create your first repository

Once your account is set up, practice the workflow you'll use throughout the program:

1. Click the **+** icon (top right) → **New repository**
2. Name it something like `toolbox-0-test`
3. Check **Add a README file**, then click **Create repository**
4. Go to **Settings → Collaborators**, click **Add people**, and enter the username `talassify`
5. Send the invite — no need to wait for it to be accepted, this just confirms the workflow works

This is a throwaway test repo, not your capstone project repo — you'll create that one later once you're matched to a Problem Brief.

---

## Part 4: Connect Your Local Machine to GitHub — ~25 minutes

Right now your test repo only exists on GitHub's website. To actually write code on your computer and get it onto GitHub, your computer needs a way to talk to it. There are two ways to do this — pick whichever feels more comfortable. You're not locked in; you can switch later.

**Both options below have you edit `README.md`. Replace its contents with this:**

```markdown
# Toolbox 0 — Setup Check

**Name:**
**GitHub username:**
**Discord username:**
**Date completed:**

## Setup checklist
- [x] VS Code installed
- [x] Created this repo and added `talassify` as a collaborator
- [x] Connected my local machine to GitHub
- [x] Joined the Talassify Discord server

This commit confirms my local-to-GitHub workflow is working. 🎉
```

Fill in your info, save, then follow the commit/push steps for whichever option you picked. This gives facilitators a quick, scannable confirmation that everything's working — not just an empty test commit.

### Option A: GitHub Desktop (no typing commands — good if you're brand new to this) — ~15 minutes

1. Download **[GitHub Desktop](https://desktop.github.com)** and install it
2. Open it and sign in with your GitHub account when prompted — this handles login for you, no extra setup needed
3. Go to **File → Clone Repository**, select your `toolbox-0-test` repo, choose a folder on your computer, and click **Clone**
4. Open that folder in VS Code (**File → Open Folder**)
5. Open `README.md`, replace its contents with the template above (filled in with your info), and save the file
6. Back in GitHub Desktop, you'll see the change listed on the left. Type a short summary (e.g. "test commit"), click **Commit to main**, then click **Push origin**
7. Refresh your repo on github.com — your change should now show up there

### Option B: Command Line Git — ~25–30 minutes

1. Install Git from **[git-scm.com/downloads](https://git-scm.com/downloads)**
   - Mac users: Git may already be installed — you can check this in a later step
2. Open VS Code's built-in terminal: **Terminal → New Terminal**
3. Tell Git who you are (this is what gets attached to every change you make):
   ```
   git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   ```
4. Clone your repo (swap in your actual GitHub username):
   ```
   git clone https://github.com/YOUR-USERNAME/toolbox-0-test.git
   ```
5. GitHub no longer accepts your account password for this — when prompted, you'll need a **Personal Access Token** instead:
   - On github.com: click your profile photo (top right) → **Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)** → **Generate new token**
   - Check the **repo** box, click generate, and copy the token somewhere safe — GitHub only shows it once
   - Paste this token in place of your password when Git asks for one
6. Open `README.md`, replace its contents with the template above (filled in with your info), save it, then in the terminal run:
   ```
   git add .
   git commit -m "test commit"
   git push
   ```
7. Refresh your repo on github.com — your change should now show up there

Both paths end at the same place: something you typed on your own computer, now visible on GitHub. That loop — **edit, commit, push** — is one you'll repeat constantly for the rest of the program, so it's worth getting comfortable with it now while the stakes are zero.

---

## Part 5: Create Your Discord Account & Join the Talassify Server — ~10 minutes

Discord is where your Quarter actually happens day to day — announcements, toolbox help channels, and check-ins all live here.

1. Go to **[discord.com](https://discord.com)** and click **Register** (or download the desktop/mobile app and sign up from there)
2. Use the **same email you used for your Talassify application**
3. Pick a username — this can be more casual than your GitHub one, but keep it recognizable so mentors know who you are
4. Verify your email
5. Join the Talassify server using this invite link: **https://discord.gg/mDYBns6Ms**
6. Once you're in, head to the **#welcome-and-rules** channel (inside the START HERE category) and follow the pinned instructions to set your nickname and pick up your toolbox role

**Also install the Discord mobile app** ([iOS](https://apps.apple.com/app/discord/id985746746) / [Android](https://play.google.com/store/apps/details?id=com.discord)) and make sure notifications are turned on. Announcements, facilitator messages, and help-forum replies all happen in Discord — having it on your phone means you're not missing something time-sensitive just because your laptop's closed.

**Stuck on any step in this guide — VS Code, GitHub, or Discord itself?** Once you're in the server, post in the **help-tools-setup** forum. That channel exists specifically for setup problems, so don't hesitate to use it before Day 1.

---

## Part 6: Install Node.js, npm, and nvm — ~10 minutes

> **Required if:** you're on the **JavaScript Framework track** (Toolbox 3 / Vue.js) or planning to pursue **Full-Stack Development**.
> **Optional for everyone else** — skip this part for now if neither applies to you. You can always come back and do it later if your track changes.

Vue's tooling (and most modern JavaScript frameworks) run through Node.js and npm, not the browser. Neither comes bundled with VS Code, so if your track needs it, set it up now rather than mid-toolbox.

1. **Check if you already have them.** Open a terminal and run:
   ```
   node -v
   npm -v
   ```
   If both print a version number, you're already set — skip to the checklist below.

2. **If you see "command not found,"** you have two options:
   - **Simplest:** install Node.js (which includes npm) directly from **[nodejs.org](https://nodejs.org)** — download the LTS version.
   - **Recommended instead:** install **nvm** (Node Version Manager), which lets you install and switch Node versions per-project rather than committing to one system-wide version. This matters because different frameworks and toolboxes can require different Node versions over time.
     - macOS/Linux: [nvm-sh/nvm](https://github.com/nvm-sh/nvm)
     - Windows: [nvm-windows](https://github.com/coreybutler/nvm-windows)
     - Then run:
       ```
       nvm install --lts
       nvm use --lts
       ```

**You're set up when:**

- [ ] `node -v` prints a version number
- [ ] `npm -v` prints a version number
- [ ] *(Optional)* `nvm -v` prints a version number, confirming nvm is installed

---

## Before You're Done: Confirm You Have

- [ ] VS Code installed and opens without errors
- [ ] Know how to open DevTools in your browser
- [ ] GitHub account created
- [ ] Test repository created with `talassify` added as a collaborator
- [ ] Connected local machine to GitHub (Option A or B) and pushed a test commit
- [ ] Discord account created (desktop and mobile) and joined the Talassify server
- [ ] Found #welcome-and-rules in the START HERE category
- [ ] *(If on JS Framework or Full-Stack track)* Node.js and npm installed and verified

Once everything above is checked, reply to your onboarding email to confirm — this is how we know you're ready for Day 1.

---

*Getting stuck is a normal part of setting all this up — it happens to everyone, not just beginners. If something's not clicking, email talassify@gmail.com. A facilitator will help you work through it — the earlier you ask, the easier it is to fix.*
