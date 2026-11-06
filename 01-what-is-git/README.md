# 01 · What is Git

> Before I run a single command, this is what Git actually is: a tool that saves the history of my project so I can go back to any point, see what changed, and work with other people without copies flying around. Everything else in these notes sits on top of this page.

**On this page:** [What Git is](#what-git-is) · [Life without it](#life-without-it) · [Centralized vs distributed](#centralized-vs-distributed) · [Why Git won](#why-git-won) · [Installing it](#installing-it-on-linux) · [My identity setup](#my-identity-setup) · [Getting help](#getting-help)

---

## What Git is

Git is a **version control system** — a tool that saves **snapshots** of my project as I work. Each snapshot is a **commit**. Once something is committed I can jump back to it, compare it with another commit, or undo work I did last week.

The part that took me a while to really get: a commit isn't a list of *changes*, it's a full picture of every file at that moment. The history is just the row of those pictures, and I can walk back to any one of them.

![Each commit is a full snapshot of my project; I can check out any one of them](images/snapshots.svg)

It's also **distributed**, which means the full history lives on my own machine, not on a server. I can commit, read history, and branch with no internet at all — the network only matters when I want to share.

> **Git is not GitHub.** This is the thing I mixed up at the start. Git is the tool on my computer. GitHub is a website that stores a copy of my repo online so I can share it. Git is the app; GitHub is one place I can upload to. I only need GitHub when I go online — that's Part 5. Everything in Parts 1–4 works with no account and no internet.

## Life without it

Before version control, the way I "saved versions" was copying the whole folder:

```
project/
project-final/
project-final-v2/
project-FINAL-actually/
```

Three problems showed up fast, and I've hit all of them: I lose track of which folder is current, I can't see what actually changed between two of them, and if someone else edits their own copy, merging the two by hand is miserable. Git fixes all three — one folder, full history, and it does the merging for me.

## Centralized vs distributed

There are two ways a version control system can be built, and the difference is the reason Git feels the way it does day to day.

![Centralized keeps the history on one server; distributed gives every machine the full history](images/centralized-distributed.svg)

With a **centralized** system (SVN, TFS), the history lives on **one server**. Every action needs the network, and if the server is down, nobody can commit or even read history. With a **distributed** system (Git, Mercurial), **every person has the full history** on their own machine. I work offline and only talk to a server when I actually want to share something.

The way it finally clicked for me: centralized is one shared whiteboard everyone has to stand at; distributed gives everyone their own copy of the whole book, and you sync up when you feel like it.

## Why Git won

The reasons it beat the alternatives, and the ones I actually feel:

- **It's fast** — most commands run locally, so there's no network wait.
- **It works offline** — I can commit on a plane and sync later.
- **Branches are cheap** — making one is instant (that's Part 4, and it changes how I work).
- **It's free and open source** — which is why it's everywhere, including every job posting I've looked at.

## Installing it (on Linux)

I'm on Linux Mint, so it's `apt`:

```bash
sudo apt update
sudo apt install git
git --version
# git version 2.43.0   (any 2.x is fine)
```

## My identity setup

Git stamps every commit with a name and email, so I set those once per machine before doing anything else. These are the exact settings I run on a fresh install:

```bash
git config --global user.name "Haseeb Rehman"
git config --global user.email "me@example.com"   # same email as my GitHub
git config --global core.editor "nano"            # friendlier than the default (Vim)
git config --global core.autocrlf input           # line endings — see note below
git config --list --show-origin                   # check it, and see which file each setting lives in
```

> **On Linux, `core.autocrlf` is `input`, not `true`.** `true` is the Windows value. `input` fixes Windows-style line endings on the way in and leaves my files alone on the way out. I copied `true` from a tutorial once and it was wrong for my setup.

The reason `--global` matters is that Git reads settings from three places, and the most specific one wins:

```mermaid
flowchart LR
  S["system<br/>every user on the machine"] -->|beaten by| G["global<br/>all my repos"] -->|beaten by| L["local<br/>this repo only ✅ wins"]
  style S fill:#F3F4F6,stroke:#9AA3AF,stroke-width:1.5px,color:#5A6B85
  style G fill:#D9EEEB,stroke:#19857C,stroke-width:1.5px,color:#196E67
  style L fill:#E8E2FB,stroke:#6B4FD8,stroke-width:2.5px,color:#6B4FD8
  linkStyle default stroke:#9AA3AF,stroke-width:1.5px
```

So I keep my personal email global, and if I ever need a work email I set it with `--local` *inside that one repo* and it overrides the global one there. If I set the wrong email, one line fixes it for all future commits:

```bash
git config --global user.email "right@email.com"
```

(Commits I've already made keep the old email — fixing those means rewriting history, which is Part 6.)

## Getting help

Three ways to read Git's own manual for any command, and I use all three depending on how much I need:

```bash
git config --help     # full manual page (press q to quit)
man git-config        # the same manual, the classic way
git config -h         # short one-screen summary of the options
```

The pattern that makes this easy to remember: long flag (`--help`) → long manual, short flag (`-h`) → short summary.

---

**What tripped me up:** that Git and GitHub are different things. I genuinely thought I needed an online account to use Git at all, and I almost signed up before installing anything. I didn't — Git runs entirely on my machine, and GitHub is just one place I can push a copy to later. Realising I could do everything in the first four parts of these notes with no account and no internet is what made the rest make sense.

---

[🏠 Index](../README.md) · [02 · Creating Snapshots ➡](../02-creating-snapshots/README.md)
