<div align="center">

# Git cheat sheet

A one-page quick reference — the commands I reach for most, grouped by what I'm doing.
Full explanations live in the [numbered sections](README.md).

</div>

> [!NOTE]
> `<thing>` means "replace this with your value." Everything here is tested on Linux.

## Setup (once per machine)

```bash
git --version                                 # check it's installed
git config --global user.name "Your Name"     # sign your commits
git config --global user.email "you@mail.com" # use your GitHub email
git config --global core.editor "nano"        # friendly default editor
git config --list --show-origin               # see every setting + which file it's in
```

## Start a repo

```bash
git init                    # turn this folder into a repo
git clone <url>             # copy an existing repo (already connected to its remote)
```

## The everyday loop

```bash
git status                  # what changed? (run this constantly)
git add <file>              # stage one file
git add .                   # stage everything changed
git commit -m "message"     # save staged changes to history
git commit -am "message"    # stage tracked changes AND commit (not new files)
git log --oneline           # compact history
```

## See what changed

```bash
git diff                    # unstaged changes (working dir vs staging)
git diff --staged           # staged changes (vs last commit)
git show <commit>           # a commit's full details + diff
```

## Undo (which area am I undoing in?)

```bash
git restore --staged <file> # unstage (keep your edits)
git restore <file>          # discard edits ⚠️ destructive
git restore --source=<commit> <file>   # pull an old version of one file forward
git rm --cached <file>      # stop tracking, keep the file on disk
```

## Browse & filter history

```bash
git log --oneline --stat          # + files changed
git log -p                        # + full diffs
git log --author="Name"           # by person
git log --after="1 week ago"      # by time
git log --grep="bug"              # search messages
git log -S"functionName"          # search the CODE that changed (pickaxe)
git log -- <file>                 # history of one file
```

## Branches

```bash
git branch                  # list branches
git switch -c <name>        # create AND switch to a branch
git switch <name>           # switch
git branch -d <name>        # delete (safe — refuses if unmerged)
git branch -D <name>        # force delete
git stash / git stash pop   # park work-in-progress / bring it back
```

## Merge & rebase

```bash
git merge <branch>          # merge <branch> into the current one
git merge --squash <branch> # collapse a feature into one commit
git rebase <base>           # replay commits onto <base> (new hashes!)
git cherry-pick <commit>    # copy one commit onto the current branch
```

## Remotes (GitHub)

```bash
git remote add origin <url>       # connect a local repo to a remote
git remote -v                     # list remotes
git push -u origin main           # first push (sets tracking)
git push                          # later pushes
git fetch                         # download, DON'T touch my files (updates origin/*)
git pull                          # fetch + merge
git push origin <tag>             # push a tag (tags don't auto-push!)
git push origin --delete <branch> # delete a remote branch
```

## Investigate

```bash
git bisect start / bad / good <commit>   # binary-search for a bug, then: git bisect reset
git blame <file>                         # who wrote each line, and when
git shortlog -n -s -e                    # contributors by commit count
git tag -a v1.0 -m "Release 1.0"         # annotated release tag
```

## Fix mistakes (rewriting history — local only!)

```bash
git commit --amend -m "new message"  # fix the last commit's message
git commit --amend --no-edit         # add a forgotten file to the last commit
git reset --soft HEAD~1              # uncommit, keep changes staged
git reset --mixed HEAD~1             # uncommit + unstage (default)
git reset --hard HEAD~1              # uncommit + discard changes ⚠️
git revert <commit>                  # safe undo of a PUSHED commit (adds an inverse commit)
git reflog                           # everywhere HEAD has been — recover "lost" commits
git rebase -i HEAD~<n>               # reword / squash / drop / reorder recent commits
```

> [!TIP]
> **The one rule:** never rewrite (amend / reset / rebase) commits you've already
> pushed or shared. For those, use `git revert`. The `reflog` is your safety net
> for everything local.

---

[🏠 Back to index](README.md)
