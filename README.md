<div align="center">

<img src="assets/banner.svg" alt="Git Notes" width="100%">

</div>

## About these notes

My notes on Git and GitHub, from `git init` to interactive rebase, written as I learned the tool and kept in the order it finally made sense to me.

They're really for one person: future me. When I haven't touched a command in a while, I open the right page here and follow along until it's back in my head. So the pages go deep on purpose — I'd rather have the detail and not need it than come back in six months and find a summary that assumes I remember the rest.

> [!NOTE]
> **Every command's output on these pages is real.** Git runs on my own machine (Linux Mint), so I actually ran everything shown — the output is what my terminal printed, not something I made up to illustrate a point.

If you're not me and you found these useful, great — and if you spot a mistake, open an issue, I'd like to fix it.

## What's covered

Each part builds on the one before it, so read top to bottom the first time; after that, jump straight to whatever you came for.

### Part 1 — Foundations

| # | Section | What's inside |
|:-:|---|---|
| 01 | [What is Git](01-what-is-git/README.md) | Version control, centralized vs distributed, snapshots (not diffs), install & config |

### Part 2 — The everyday workflow

| # | Section | What's inside |
|:-:|---|---|
| 02 | [Creating Snapshots](02-creating-snapshots/README.md) | `init`, the three areas, `add`/`commit`, the commit object, atomic commits |
| 03 | [Inspecting & Undoing](03-inspecting-and-undoing/README.md) | `diff` vs `--staged`, `rm --cached` + `.gitignore`, `mv`, the three undos |

### Part 3 — Browsing history

| # | Section | What's inside |
|:-:|---|---|
| 04 | [Reading & Filtering History](04-reading-and-filtering-history/README.md) | Shaping `log`, `--author`/`--grep`/`-S`, commit ranges, aliases |
| 05 | [Investigating History](05-investigating-history/README.md) | `HEAD~n`, detached HEAD, `bisect`, `blame`, restoring deleted files, tags |

### Part 4 — Branching & merging

| # | Section | What's inside |
|:-:|---|---|
| 06 | [Branches](06-branches/README.md) | Branches as movable pointers, create/switch/delete, compare, stash |
| 07 | [Merging](07-merging/README.md) | Fast-forward vs 3-way, conflicts, squash, rebase, cherry-pick |

### Part 5 — Working with other people

| # | Section | What's inside |
|:-:|---|---|
| 08 | [Remotes & GitHub](08-remotes-and-github/README.md) | `origin/main`, clone/fetch/pull/push, SSH, the rejected-push fix |
| 09 | [Pull Requests & Open Source](09-pull-requests-and-open-source/README.md) | PRs, issues/labels/milestones, the fork → upstream → PR flow |

### Part 6 — Rewriting history

| # | Section | What's inside |
|:-:|---|---|
| 10 | [Rewriting History](10-rewriting-history/README.md) | The golden rule, `reflog`, `reset`, `revert`, `amend`, interactive rebase |

### Appendix

| Section | What's inside |
|---|---|
| [Recovery — I screwed up, now what?](appendix-recovery/README.md) | Symptom → fix for every common disaster, marked safe vs needs-care on shared history |

## How the pages are written

Plain English, short sentences, the way I'd explain it to a friend. Every command sits in a code block with its real output underneath, the one idea worth remembering is in **bold**, and most pages end with a short note on whatever actually tripped me up — because the thing that confused me once will probably confuse me again.

Diagrams are a mix of hand-made **SVG** for the bigger pictures and **Mermaid** (which GitHub renders natively) for the smaller flows. There's also a one-page [CHEATSHEET](CHEATSHEET.md) for when I just need the command and not the explanation.

## Repo layout

```
Git/
├── README.md          ← you are here
├── CHEATSHEET.md      ← one-page command reference
├── assets/            ← the banner
├── 01-what-is-git/
│   ├── README.md      ← the notes (GitHub opens this automatically)
│   └── images/        ← the diagrams for this section
├── 02-creating-snapshots/
│   └── … each section is its own folder, same shape
└── appendix-recovery/ ← the "I screwed up, now what?" guide
```
