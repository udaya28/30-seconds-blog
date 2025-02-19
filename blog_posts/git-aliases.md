---
title: Git aliases
type: cheatsheet
tags: git,configuration,cheatsheet
authors: chalarangelo
cover: blog_images/organizer.jpg
excerpt: Increase your productivity by creating aliases for many common git operations.
---

### Creating aliases

Use the command below to create aliases, replacing `<alias>` with the name of the alias and `<command>` with the command to be aliased:

```shell
git config --global alias.<alias> <command>
```

Additionally, you can use [edit the configuration file](/git/s/edit-config) and add many aliases all at once.

### Useful aliases

```editorconfig
[alias]
  co = checkout
  cob = checkout -b
  coo = !git fetch && git checkout
  br = branch
  brd = branch -d
  st = status
  aa = add -A .
  unstage = reset --soft HEAD^
  cm = commit -m
  amend = commit --amend -m
  fix = commit --fixup
  undo = reset HEAD~1
  rv = revert
  cp = cherry-pick
  pu = !git push origin `git branch --show-current`
  fush = push -f
  mg = merge --no-ff
  rb = rebase
  rbc = rebase --continue
  rba = rebase --abort
  rbs = rebase --skip
  rom = !git fetch && git rebase -i origin/master --autosquash
  save = stash push
  pop = stash pop
  apply = stash apply
  rl = reflog
```

**Image credit:** [Renáta-Adrienn](https://unsplash.com/@bajkorenata?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) on [Unsplash](https://unsplash.com?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)
