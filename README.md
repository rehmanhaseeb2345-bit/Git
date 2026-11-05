<div align="center">

<img src="assets/banner.svg" alt="Git Notes" width="100%">

<br><br>

![Git](https://img.shields.io/badge/Git-F05133?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Sections](https://img.shields.io/badge/sections-11-blue?style=for-the-badge)
![Progress](https://img.shields.io/badge/written-0%20%2F%2011-orange?style=for-the-badge)

</div>

## 👋 Hey, welcome to my notes

I went deep on **Git & GitHub** — the whole thing, from `git init` to interactive rebase — and I wrote it all down here, in my own words, explained the way it finally clicked for me.

This repo is two things for me:

- **My own documentation.** When I forget a flag or how something works, I come here before I google it.
- **A record of what I've learned.** From what a snapshot is, all the way to rebasing, the fork workflow, and recovering from mistakes.

> [!NOTE]
> **Every command's output in these notes is real.** Git runs entirely on my own machine (Linux Mint), so unlike tools that need a cluster or a paid account, I actually ran everything here — the output you see is what my terminal printed, not illustrative.

These are student notes, written while learning. If you spot a mistake, please open an issue — I'd genuinely love to learn from it.

## 🧭 How I write every page

Every topic follows the same structure (my template is in [TEMPLATE.md](TEMPLATE.md)):

| Part | What it gives you |
|---|---|
| **What it is** | A plain-English definition |
| **Why it exists** | The problem it solves |
| **Key points** | The core ideas, broken down, with real commands |
| **Visual** | A hand-made diagram (SVG) + Mermaid where it helps |
| **⚠️ Watch out** | Mistakes and misconceptions to avoid |
| **🔧 Fix it** | If you hit this, run that — the recovery one-liner |
| **🧪 Try it** | A small exercise, with a collapsible answer |
| **🤔 What confused me** | The thing that tripped me up |

## 🗺️ What's covered

**Progress:** `░░░░░░░░░░░░░░░░░░░░░░░░░░░` 0 / 11

**Legend:** ✅ written · 🚧 being written · ⬜ not yet

### Part 1 — Foundations

What Git is and how it thinks, before any command.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 01 | [What is Git](01-what-is-git/README.md) | VCS, centralized vs distributed, snapshots not diffs, install & config | 🚧 |

### Part 2 — The Core Workflow

The everyday loop: snapshotting your project and undoing when needed.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 02 | [Creating Snapshots](02-creating-snapshots/README.md) | `init`, the three areas, `add`/`commit`, the commit object, atomic commits | 🚧 |
| 03 | [Inspecting & Undoing](03-inspecting-and-undoing/README.md) | `diff` vs `--staged`, `rm --cached` + `.gitignore`, `mv`, the three undos | 🚧 |

### Part 3 — Browsing History

Reading history like a search engine, and investigating it like a detective.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 04 | [Reading & Filtering History](04-reading-and-filtering-history/README.md) | `log` shaping, `--author`/`--grep`/`-S`, ranges, aliases | 🚧 |
| 05 | [Investigating History](05-investigating-history/README.md) | `HEAD~n`, detached HEAD, `bisect`, `blame`, restoring deleted files, tags | 🚧 |

### Part 4 — Branching & Merging

Parallel work, and bringing it back together.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 06 | [Branches](06-branches/README.md) | Branches as movable pointers, create/switch/delete, compare, stash | 🚧 |
| 07 | [Merging](07-merging/README.md) | Fast-forward vs 3-way, conflicts, squash, rebase, cherry-pick | 🚧 |

### Part 5 — Collaboration

Working with a remote, and with other people.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 08 | [Remotes & GitHub](08-remotes-and-github/README.md) | `origin/main`, clone/fetch/pull/push, SSH, the rejected-push fix | 🚧 |
| 09 | [Pull Requests & Open Source](09-pull-requests-and-open-source/README.md) | PRs, issues/labels/milestones, the fork → upstream → PR flow | 🚧 |

### Part 6 — Rewriting History

Cleaning up before you share — and getting out of any mistake.

| # | Section | What's inside | Status |
|:-:|---|---|:-:|
| 10 | [Rewriting History](10-rewriting-history/README.md) | The Golden Rule, `reflog`, `reset`, `revert`, `amend`, interactive rebase | 🚧 |

### Appendix

| Section | What's inside | Status |
|---|---|:-:|
| [⛑ Recovery Guide — I Screwed Up, Now What?](appendix-recovery/README.md) | Symptom → fix for every common disaster, tagged safe vs shared-history care | 🚧 |

## 📁 How this repo is organized

```
Git/
├── README.md          ← you are here
├── TEMPLATE.md        ← the structure every page follows
├── CHEATSHEET.md      ← one-page command reference
├── assets/            ← the banner
├── 01-what-is-git/
│   ├── README.md      ← the notes (GitHub opens this automatically)
│   └── images/        ← the hand-made diagram for this section
├── 02-creating-snapshots/
├── 03-inspecting-and-undoing/
├── 04-reading-and-filtering-history/
├── 05-investigating-history/
├── 06-branches/
├── 07-merging/
├── 08-remotes-and-github/
├── 09-pull-requests-and-open-source/
├── 10-rewriting-history/   ← each with its own README.md + images/
└── appendix-recovery/      ← the "I screwed up, now what?" guide
```

---

<div align="center">

Made while learning, one commit at a time. 📸 → 🌿 → ☁️ → ⏪

</div>
