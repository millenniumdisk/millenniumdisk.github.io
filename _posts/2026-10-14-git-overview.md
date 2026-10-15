---
layout: post
title: Git Overview
---

# Git Overview

## Low Level
- Create Tree - `git mktree`
- Create Object
  - Create Git Object - `git hash-object` (ex. `echo "Hello, Git" | git hash-object --stdin -w`, `git hash-object`)
  - Create Git Object From File - `git hash-object <filename> -w` (ex. `git hash-object ../new-file.txt -w`)
- Read Git Object
  - Show Object Contents - `git cat-file -p <hash>`
  - Show Object Size - `git cat-file -s <hash>`
  - Show Object Type - `git cat-file -t <hash>`
- Check Staging Area
  - Check Files in Staging Area - `git ls-files`
  - Check Files in Staging Area in Table Format - `git ls-files -s`
- Load Files in Git Repository to Staging Area - `git read-tree <hash>`
- Load All Files in Staging Area to Working Directory - `git checkout-index -a` (`-a` means all files)
- Unpack Pack File - `cat <file> | git unpack-objects` (put the pack file in `.git` folder then delete it after unpacking - `cat pack-bf7eaf2ba9af7da56f3a874b2483b00dba0e8a98.pack | git unpack-objects`)

## Setup
- Show Git Version Number - `git --version` / `git -v` / `git version`
- Show Configuration - `git config --list`
- Display Global / Local Username - `git config user.name` (use outside / inside Git repository for global / local username)
- Show Global / Local User Email - `git config user.email` (use outside / inside Git repository for global / local email)
- Change Global Username - `git config --global user.name "<name>"`
- Change Global Email - `git config --global user.email "<email>"`
- Change Local Username - `git config user.name "<name>"` (use inside Git repository)
- Change Local Email - `git config user.email "<email>"` (use inside Git repository)
- Check Config File - `cat .git/config`
- Change Default Branch Name - `git config --global init.defaultBranch <branch>`
- Initialization - `git init`

## Inspect
- Show Status of Git Repository - `git status`
  - Verbose Option - `-v`
- Show Commit History - `git log`
  - Short Output Option - `--oneline`
  - Additional Info Option - `--stat`
  - Show File Changes Option - `-p`
  - Show N Commits Option - `-<number>`
  - Show Branch Connections Option - `--graph`
  - Show Merge Commits Only - `--merges`
  - Show Non-merge Commits Only - `--no-merges`
  - Filter Option - `--author="<name>"`
  - Find Specific String - `--grep="<query>"`
- Formatted Commit History - `git log --pretty=format:"%H"`
  - `H` - Complete commit hash.
  - `cn` - Committer names (`git log --pretty=format:"%cn %H"`).
  - `h` - Short hash (`git log --pretty=format:"%cn %h"`).
  - Strings can also be added as in `git log --pretty=format:"Author of commit: %cn Commit SHA1 hash: %h"`.
  - `cd` - Date (`git log --pretty=format:"Author of commit: %cn; Commit SHA1 hash: %h; Date: %cd"`).
- Show Files Differences - `git diff` (`-` is old file followed by starting line number and amount of lines while `+` is new file followed by starting line number and amount of lines)
- Show Changes in Specific Commit - `git show <hash>`
- Show Summary of All Commits - `git shortlog`
  - `-n` - Sort by number of commits.
  - `-s` - Suppress showing of commits.
  - `-e` - Shows email.
- Create Alias - ``git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%C(bold blue)<%an>%Creset' --abbrev-commit"``
  - Creates `git lg` alias.
- Show Remote and Local References - `git show-ref`
- Compare References for a Specific Branch - `git show-ref <branch>`

## Staging
- Stage a File - `git add <filename>`
- Stage Multiple Files - `git add <filename1> <filename2>`
- Stage All Files - `git add .`
- Stage Previously Tracked Files Only - `git add -u`
- Unstage a File - `git rm --cached <filename>` (`git restore --staged <filename>` can also unstage a file)
- Unstage All Files - `git reset .`

