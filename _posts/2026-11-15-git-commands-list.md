---
layout: post
title: Git Commands List
---

## Git Commands
### Basics
- `git init` - Initialize a project directory as a Git repository.
- `git ls-files` - Low level command that shows all files in staging area.
- `git status` - Show status of Git repository.
- `git config --global user.name "<name>"` - Set global name.
- `git config --global user.email <email>` - Set global email.
- `git config --list` - Show Git configuration.
- `git commit -m "<description>"` - Create a commit.
- `git log` - Show commit history.
- `git add <filename>` - Add a file from working directory to staging area.
- `git add .` - Add all files from working directory to staging area.
- `git rm --cached <filename>` - Remove a file in staging area only.
- `git checkout <arg1>` - Go to `arg1` (`arg1` can be a hash or branch).

### Branches
- `git branch` - Show all local branches.
- `git branch <name>` - Create a new branch based on the current branch.
- `git branch -d <name>` - Delete a merged branch.
- `git branch -m <old_name> <new_name>` - Rename a branch.
- `git branch -D <name>` - Force delete a non-merged branch.
- `git checkout -b <name>` - Create and chekcout a branch.

### 
- `git clone` - Clone a remote repository and create a new folder.
- `cat <file> | git unpack-objects` - Low level command to unpack a pack file to objects folder (move the pack file to .git folder first then go inside .git folder).
- `git diff` - Show old and modified versions of every changed file.
- `git commit -am "<description>"` - Automatically stage modified and deleted files to staging area and commit them.
- `git merge <arg1>` - Updates current branch with changes from `arg1` branch.