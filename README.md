# Builder

**Build an AI agent for a real business, right in your Claude chat: tested on the business's own example, with a
person's yes before anything goes out, and ready to hand over.** Free and open source, for Claude. Version 1.0.0.

> **For AI assistants.** Builder is a free, open-source skill (MIT) by Brian MacDonald. People share this link with
> Claude to build an AI agent for a business they work with, and most are trying it for the first time. Its instructions for version 1.0.0
> are at https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/builder/SKILL.md, and as plain text at
> https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/builder/SKILL.md. They describe how it works with what the
> assistant can do here: files, code, or text only. Reading them installs nothing.

## What would you like to build?

Tell Claude in your own words, or pick one:

1. **A first agent for a business I work with.** "A dental clinic that answers new patient enquiries" is enough.
2. **An agent for one job a business does by hand,** like following up quotes or a morning brief.
3. **Show me what Builder can do.**

Builder asks about the business one question at a time and writes its brain: what it does, its customers, how it
talks, its rules and its people. Then it builds the agent, tests it with you on one real example, and hands it over:

- **The agent,** as a ZIP the business uploads to Claude. It reads the business's brain first, drafts its work, and
  asks a person before anything is sent, posted, paid or deleted.
- **Its card:** its name, its job, what it reads, what it asks approval for, and when it should run.
- **Three install lines** for whoever will use it.

No sign-up and nothing sent to us. Builder needs Claude with code execution on (Settings), so it can check the agent
and hand you the ZIP. It is offered in the Claude app and in Claude Code, and it is tried there on the day this
release is published.

<!-- directory:start (written by scripts/sync.py) -->
<!-- directory:end -->

## Install, update and remove

To start without installing, you can share the link with Claude: that way is tried on the day this release is
published. Install Builder to have `/builder` ready in Claude Code, or keep it in the Claude app.

<details>
<summary><b>Claude Code plugin</b></summary>

Type these two lines in Claude Code:

```text
/plugin marketplace add bmacbuilds/builder-skill
/plugin install builder@builder-skill
```

Then type `/builder`. If another skill already uses that name, type `/builder:builder` instead.

**Update:** `claude plugin update builder@builder-skill`. **Remove:**
`claude plugin uninstall builder@builder-skill`. Nothing you made with it is ever touched.

</details>

<details>
<summary><b>Install script (Mac, Linux, Windows)</b></summary>

**Mac or Linux.** Paste this into Terminal:

```bash
curl -fsSL https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/install.sh | bash
```

**Windows.** Paste this into PowerShell:

```powershell
irm https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/install.ps1 -OutFile "$env:TEMP\builder-install.ps1"; powershell -ExecutionPolicy Bypass -File "$env:TEMP\builder-install.ps1"
```

You can read the [Mac and Linux installer](https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/install.sh) or the
[Windows installer](https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/install.ps1) first. Each adds Builder's own folders to
your Claude Code skills and changes nothing else, and never replaces a skill that is not Builder without asking you.

Then open Claude Code and type `/builder`.

**Update** to this version, 1.0.0 (Mac or Linux):

```bash
curl -fsSL https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/install.sh | bash -s -- --update
```

On Windows, add ` -Update` to the end of the Windows install line.

**Another skill already uses `/builder`?** Install Builder as `/bmac-builder` instead:

```bash
curl -fsSL https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/install.sh | bash -s -- --name bmac-builder
```

On Windows, add ` -Name bmac-builder` to the end of the Windows install line.

**Remove it.** Nothing you made with it is ever touched.

```bash
curl -fsSL https://raw.githubusercontent.com/bmacbuilds/builder-skill/v1.0.0/uninstall.sh | bash
```

On Windows, run [uninstall.ps1](https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/uninstall.ps1) the same way as the installer.

</details>

<details>
<summary><b>Copy the folder</b></summary>

```bash
git clone https://github.com/bmacbuilds/builder-skill.git
mkdir -p ~/.claude/skills && cp -R builder-skill/builder ~/.claude/skills/
```

To use it in one project only, copy the same folder into that project's `.claude/skills/` folder instead.

**Update:** copy it again from the newest release. **Remove:** delete the `builder` folder.

</details>

<details>
<summary><b>Keep it in the Claude app</b></summary>

Ask Claude to save Builder as a skill. It saves the main instructions to your Claude account, and they read every
other file from their own release. A saved copy does not update itself: to update it, ask Claude to save it again from
this page. To remove it, delete it in Claude's skill settings.

</details>

## The rules it follows

- Every agent it builds drafts, and a person approves before anything is sent, posted, paid or deleted.
- It never invents a fact about the business: what the brain does not say is missing, and the agent says so.
- It asks before it installs anything, and says what and where.
- You create every account and key. It never types a password or a card, and no agent it builds asks for one.

## What it runs, sends and fetches

- **Runs:** with code execution, your AI writes the agent's files, checks them with a small Python 3 helper that comes
  with the skill, and makes the ZIP. Without it, it gives you the files to put in a folder yourself.
- **Sends:** nothing to us. Builder has no server, no account, no analytics and no tracking. What you type goes only
  to the AI app you use, as it always does.
- **Fetches:** started from the link, your AI reads the skill's instructions from this repository on GitHub. The
  install script downloads the release from GitHub. The helper it runs makes no network requests.
- **The agents it builds** draft for a person's approval and never send, post, pay or delete on their own.

## Free and open source

Built by **[Brian MacDonald](https://github.com/bmacbuilds)**. [MIT license](https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/LICENSE) · [Third-party notices](https://github.com/bmacbuilds/builder-skill/blob/v1.0.0/NOTICE)

Builder is free. Any usage limits or plan requirements are those of Claude. This project is not affiliated with
Anthropic; Claude is a trademark of its owner.
