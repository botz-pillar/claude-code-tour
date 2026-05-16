# Claude Code Tour

**A friendly, no-jargon onboarding tour for people brand-new to Claude Code.**

If you work in IT or security, just heard about Claude Code (or are setting it up for the first time), and you're worried about looking dumb or breaking something — this is for you. The tour shows you the shape of the tool, gets you to your first real win, and leaves you with a cheat-sheet of things to try the next day.

**No prior experience required.** Not the terminal. Not GitHub. Not Python. Not AI tools. If you can type and read, you can do this. We'll walk you through every step below — start to finish — including signing up for the things you might not have yet.

---

## Table of contents

1. [Is this for you?](#1-is-this-for-you)
2. [Before you install anything (work-laptop check)](#2-before-you-install-anything)
3. [Set up an Anthropic account](#3-set-up-an-anthropic-account)
4. [Install Claude Code on your computer](#4-install-claude-code-on-your-computer)
5. [Install this tour (two commands)](#5-install-this-tour)
6. [Start the tour](#6-start-the-tour)
7. ["Wait, where am I?" — the most common confusion](#7-wait-where-am-i)
8. [What you'll learn](#8-what-youll-learn)
9. [What you do NOT need to learn first](#9-what-you-do-not-need-to-learn-first)
10. [Helpful links for beginners](#10-helpful-links-for-beginners)
11. [Troubleshooting](#troubleshooting)
12. [Privacy](#privacy)
13. [Feedback & contact](#feedback--contact)

---

## 1. Is this for you?

Check any of these:

- [ ] You just installed Claude Code (or are about to) and don't know where to start
- [ ] You work in IT, security, compliance, or somewhere adjacent
- [ ] You've heard "AI agents are a big deal" but every tutorial assumes you're already a developer
- [ ] You're worried about pasting the wrong thing into the wrong tool and breaking something
- [ ] You don't have a GitHub account or anything special installed and that has been a blocker

Any of those hit? Keep reading — this is built for you.

Already a developer comfortable with the terminal, MCP servers, and hooks? Skip this. Read the [official Claude Code docs](https://docs.claude.com/en/docs/claude-code/overview) instead — the tour will refuse to run for you anyway.

---

## 2. Before you install anything

A 30-second check, especially if you work in IT or security:

- **On a work laptop?** Many companies have a vendor-approval process for AI tools. Check with your IT/security team before installing. Getting permission once is cheaper than getting caught.
- **Sensitive data on your machine** (client files, PHI, classified material)? Same answer.
- **Personal machine, learning purposes?** You're fine. Keep going.

When you chat with Claude Code, your messages go to Anthropic. Your conversations are governed by [Anthropic's terms](https://www.anthropic.com/legal/consumer-terms) and the [Trust Center](https://trust.anthropic.com/). By default, your conversations are **not** used to train Anthropic's models. If your org needs zero-retention guarantees, ask them about an enterprise agreement.

---

## 3. Set up an Anthropic account

If you've never used Claude before, you'll need a free account first.

1. Go to **[claude.ai/signup](https://claude.ai/signup)**
2. Sign up with email, Google, or Apple
3. That's it — you can stop there

The **free plan** is fine to start. Claude Code works with both the free plan and the paid Pro/Max plans — paid plans just give you more usage before you hit limits.

> **Sidebar — "what's the difference between Claude and Claude Code?"**
> *Claude* is the AI itself (the chat at claude.ai). *Claude Code* is Claude with the ability to read files, run commands, and edit things on your computer — only with your permission. They share the same account. This tour is for Claude Code.

---

## 4. Install Claude Code on your computer

You have two paths. **Pick the desktop app unless you already use the terminal regularly.**

### Path A — Desktop app (recommended for everyone else)

1. Go to **[claude.com/claude-code](https://claude.com/claude-code)**
2. Download the app for your operating system (macOS or Windows)
3. Install it like any other app (double-click the download, drag to Applications on Mac, or run the installer on Windows)
4. Open the app and sign in with the Anthropic account you just made
5. You'll see a chat window. **You are now inside Claude Code.** That's the whole installation.

You do **not** need to install Node, npm, Homebrew, or anything else for the desktop app. If anyone on the internet says you do, they're talking about the terminal version (Path B).

### Path B — Terminal (only if you're already a terminal user)

If you already know what a terminal is and use it occasionally:

```bash
npm install -g @anthropic-ai/claude-code
```

This requires Node.js. On a Mac, easiest install: `brew install node` first. Then run `claude` in any terminal.

If "Node," "npm," or "brew" don't mean anything to you — close this section, go back to Path A, install the desktop app. Same product. No downside.

### Confirm Claude Code is working

After installing, you should:

1. See a chat window with a text input at the bottom
2. Be signed in (your name or email shows somewhere)
3. Be able to type `/help` and see a menu of commands pop up

If `/help` does NOT show a menu, you might be at claude.ai (the regular Claude chat) instead of Claude Code. See [section 7](#7-wait-where-am-i) below.

---

## 5. Install this tour

This is the important new bit — installing **this plugin** so the tour will run for you. There are two commands. **Run them one at a time.** Type the first, press Enter, wait for confirmation, *then* type the second.

### First command — type this, then press Enter:

```
/plugin marketplace add botz-pillar/claude-code-tour
```

Claude will confirm something like *"Marketplace 'claude-code-tour' added."*

---

### *Wait until you see that confirmation. Then* — type the second command:

```
/plugin install claude-code-tour@claude-code-tour
```

Claude will confirm the plugin is installed. You may be prompted to approve it — say yes.

That's it. The tour is installed.

> If you accidentally paste both lines at once, Claude Code will try to read them as a single command and give you an error like *"is not a valid repository name."* No harm done — just re-run them one at a time.

---

## 6. Start the tour

In the same chat (or a new one), type **any one** of these — whichever sounds like you:

- `I'm new to Claude Code, walk me through it`
- `I'm a SOC analyst, just installed Claude Code — what should I do?`
- `I work in compliance and my boss told me to look at Claude Code. Is this for me?`
- `I'm a helpdesk guy trying to break into security — help me get started`
- `Teach me Claude Code`

The tour picks up from there. It'll ask you two questions (your job, your terminal comfort), give you the safety story, and walk you through doing **one real thing** — chosen for your role. By the end of the chat you'll have a file you made, a starter-prompts cheat sheet saved to your Documents folder, and a sense of what to try next.

Default length: **about 5 minutes.** Ask for the "full tour" if you want all the concepts.

> **Magic phrase for any moment you're stuck or overwhelmed:**
> Just type *"slow down and explain like I'm new"* and the tour will reset its pace and walk you through whatever just confused you. There's no shame button on this thing — that's the whole point.

---

## 7. "Wait, where am I?"

Newcomers get tangled up between the different places "Claude" lives. Quick reference:

| If you're here… | What you can do | Does this tour work here? |
|---|---|---|
| **Claude Code — desktop app** | Chat, read your files, edit files, run commands. Slash commands work. | ✅ Yes |
| **Claude Code — terminal** (`claude` command) | Same as desktop. Slash commands work. | ✅ Yes |
| **Claude Code — VS Code or JetBrains extension** | Same as desktop, embedded in your editor. | ✅ Yes |
| **claude.ai in a web browser** | Chat only. No files. No slash commands. | ❌ No — different product |
| **Claude iPhone/Android app** | Chat only. | ❌ No |

**The decisive test:** type `/help`. If you see a menu, you're in Claude Code. If `/help` does nothing or just shows up as text, you're somewhere else.

---

## 8. What you'll learn

By the end of the tour you'll understand, *in plain English*:

- **Sessions** — what's remembered, what isn't
- **Tools** — what Claude can do on your computer
- **Permissions** — how to keep yourself safe (and a read-only "plan mode" for when you're nervous)
- **Folders & projects** — how Claude thinks about your files
- **Slash commands** — typed shortcuts like `/help` and `/clear`
- **Skills** — packaged know-how that activates automatically (like this tour)
- **MCP servers** — how Claude connects to GitHub, Notion, Splunk, etc.
- **Subagents** — focused helpers for big jobs
- **`CLAUDE.md`** — the file that teaches Claude about your project

You'll learn the names *while you use them*, not as a lecture upfront.

---

## 9. What you do NOT need to learn first

Things people *think* they need to know but absolutely don't:

- The terminal / command line
- Git or GitHub
- Python or any programming language
- Docker
- Regular expressions
- "AI prompt engineering"

You can pick those up later, on demand, when a real task forces you into them. Day one, you just need to type and read.

---

## 10. Helpful links for beginners

You don't need any of this to do the tour. Bookmark this section for the *day after* the tour, when you start wondering "what's next?"

### Official Claude Code resources

- **[Claude Code overview](https://docs.claude.com/en/docs/claude-code/overview)** — the official docs
- **[Quickstart](https://docs.claude.com/en/docs/claude-code/quickstart)** — Anthropic's own first-steps guide
- **[Anthropic Trust Center](https://trust.anthropic.com/)** — data handling, retention, compliance answers

### A nicer way to read `.md` files (Markdown)

The tour will save files to your Documents folder ending in `.md`. They're just plain text, but a real reader makes them look like proper documents:

- **[Obsidian](https://obsidian.md/)** — free, cross-platform, most popular choice
- **[Typora](https://typora.io/)** — clean and simple, free trial
- **[VS Code](https://code.visualstudio.com/)** — free, has a built-in Markdown preview (Ctrl/Cmd + Shift + V)

Any of these will work. Or just drag a `.md` file into any browser tab — it'll display as plain text.

### When you're ready for GitHub (no rush)

GitHub is where you'd eventually store your projects and detection rules in public — great for building a portfolio if you're early in your career. You don't need it for the tour, but when you're ready:

- **[Sign up for free at github.com/join](https://github.com/join)** — takes 2 minutes
- **[GitHub Hello World tutorial](https://docs.github.com/en/get-started/start-your-journey/hello-world)** — their official "your first repo" walkthrough, beginner-friendly
- **[GitHub Skills](https://skills.github.com/)** — free, interactive courses on the basics

### When you're ready for the terminal (no rush)

The terminal is where commands like `ls` and `cd` live. You don't need it for the tour, but learning a little goes far:

- **[The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)** — free MIT class on the terminal, shell, version control. Best resource on the internet.
- **[Codecademy: Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line)** — interactive, friendlier on-ramp

### Free AI/security learning that pairs well with Claude Code

- **[TryHackMe](https://tryhackme.com/)** — hands-on cybersecurity learning, free tier is generous. Pairs perfectly with Claude Code for writing up what you solved.
- **[Hack The Box Academy](https://academy.hackthebox.com/)** — same idea, more guided.
- **[SANS Cyber Aces](https://www.cyberaces.org/)** — free, no signup, foundations.
- **[Microsoft Learn — Security paths](https://learn.microsoft.com/en-us/training/browse/?roles=security-engineer)** — free, well-structured.

### Stuck on something specific?

You can always ask the Claude chat directly: **"I'm stuck on X — explain like I'm new."** Claude is good at this. Don't grind silently.

---

## Troubleshooting

**"`/plugin marketplace add` says it doesn't know that command."**
→ You're on an older version of Claude Code. Update the app (or run `npm update -g @anthropic-ai/claude-code` for the terminal version), restart, try again.

**"I typed the command and nothing happened."**
→ Check that you're in Claude Code, not claude.ai in a browser. Use the `/help` test in [section 7](#7-wait-where-am-i) above.

**"I got an error like 'is not a valid repository name.'"**
→ You probably pasted both install commands at once. Run them one at a time, with Enter between. See [section 5](#5-install-this-tour).

**"It installed but the tour won't start."**
→ Try one of the trigger phrases in [section 6](#6-start-the-tour) verbatim — exact words like *"I'm new to Claude Code, walk me through it"* work best. If still nothing, type `/claude-code-tour` directly to force it.

**"How do I uninstall the tour?"**
→ `/plugin uninstall claude-code-tour`. Nothing else stays on your machine.

**"It crashed / I got a weird error / something is broken."**
→ Two options:
  - **Open a GitHub issue** at [github.com/botz-pillar/claude-code-tour/issues](https://github.com/botz-pillar/claude-code-tour/issues) (you'll need a free GitHub account — see [section 10](#10-helpful-links-for-beginners) if you don't have one)
  - **Or just email me** at josh@pillarsecurity.io with the error and what you were doing. You don't need GitHub.

---

## Privacy

- **This plugin doesn't phone home.** It's a folder of instructions Claude reads when you start the tour. No analytics, no telemetry.
- **Your conversation with Claude is governed by Anthropic's terms** — see the [Trust Center](https://trust.anthropic.com/) for data handling, retention, and (for orgs) zero-retention agreements.
- **The tour writes one short memory note at the end** — your role, your terminal comfort, and a one-line description of what you built. No conversation content. You can delete it any time from `~/.claude/memory/user_claude_code_onboarding.md`.

---

## Feedback & contact

- **Found a bug or have an idea?** [Open a GitHub issue](https://github.com/botz-pillar/claude-code-tour/issues).
- **Never used GitHub before?** Email josh@pillarsecurity.io — happy to hear it.
- **Want to share what you built during the tour?** Same email. I love seeing first-day artifacts.

---

## License

MIT — see [LICENSE](./LICENSE). Use it, fork it, share it, remix it for your org.

## Who made this

[Josh Botz](https://github.com/botz-pillar) — cloud security practitioner, builder of [AI Cloud Security Lab](https://aicloudsecuritylab.com), occasional writer of skills like this one.

If this helped you, the kindest thing you can do is tell one other person in IT or security who's struggling to get started with AI tools. That's it.
