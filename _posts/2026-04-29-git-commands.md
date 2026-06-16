---
layout: post
title: Git Commands
---

# Git
Explore Git further in [Git Website](https://git-scm.com/docs).

## Introduction
### What is Git?
Git is a VCS (Version Control System) used to track your project's status. Instead of copying your entire project folder and changing its name and version number manually and then sending that entire folder to other team members working on the project, Git can make working on the project easier because collaboration is possible where all team members can contribute simultaneously regardless of where they are located. A Git repository hosting service is needed for collaboration and assurance (so when your PC containing the project folder won't work, the project is still available online).
### What is a Repository Hosting Service?
A repository hosting service like GitHub or GitLab is where Git repositories can be stored and be used as a centralized point of getting and giving project updates for collaboration.

## Terminal
### Change Directory
`cd` - Make the terminal go to root folder.
`cd <path>` - Change directory to the relative or absolute path specified like in `cd Desktop` or `cd Desktop/new-folder`.
`cd ..` - Go back up one level in the directory.
### Create Directory
`mkdir <name>` - Create a directory.
### Create File
`touch <name>` - Create a file like in `touch file.txt`.
### List Files
`ls` - Lists files.
`ls -la` - List all files in the directory in a detailed format. `l` is table format and `a` is for hidden folders and files.
`ls -la <directory>` - List the files in the directory.
### Clear Terminal
`clear` - Clears the terminal.
### File Explorer
`start .` - Opens current folder in File Explorer. Using `explorer .` also works similarly.
### Check Current Directory
`pwd` - See what is the current directory.
### Current Directory
`.` - Alias of the current directory.
### Parent Directory
`..` - Alias of the parent directory.
### Edit File
`nano <filename>` - Use a text editor to edit a file like in `nano new-file.txt`. `ctrl + o` to write changes and `ctrl + x` to exit in nano.
### Autocomplete
Use tab key to autocomplete commands in the terminal. Press tab key twice to see choices.
### Print
`echo "string"` - Print to terminal like in `echo "Hello World"`.
### Help
`man <command>` - Help on a specific command like in `man clear`. Git Bash doesn't support `man`. Use `--help` like in `touch --help`. Press `ctrl + z` to close help from `man`.
### Open Current Directory
`open .` - Open current directory.
`open <filename>` - Open files.
### Hidden Files
Hidden files start with a `.`.
### Write
`>` - Write to file like in `echo "Hello World" > another-file.txt`.
### Append
`>>` - Append to the file like in `echo "Another Line" >> another-file.txt`.
### List File Contents
`cat <name>` - List contents of the file. `cat file.txt` will show contents of file unless it is an empty file.
### Remove
`rm <filename / directory>` - Remove file or directory like in `rm new-folder` (directory needs to be empty to be deleted).
`rm -rf <name>` - Forcibly removes files inside a folder recursively (deletes the folder) like in `rm -rf new-folder`.
### Close Git Bash
`exit` - Closes Git Bash terminal.

### Activity - Initialize a Git Repository and Create a New Commit
1. Check the current location in the terminal.
2. Go to a place where a project can be created like a different drive.
3. Check the folders and files in the current directory.
4. Clear the screen.
5. Create a new empty directory.
6. Check the contents of the current directory again.
7. Go to the new folder.
8. Initialize it as a new Git repository.
```bash
pwd
cd E:
ls -la
clear
mkdir git-basics
ls -la
cd git-basics
git init
```

## Setup
### Display Git Version Number
```bash
git -v
```
Get the version of Git. The version can also be displayed with `git --version` or `git version`. Use this command to see if Git is installed.
### Display Configuration
```bash
git config --list
```
Display the current Git configuration.
### Change Global Username
```bash
git config --global user.name "<name>"
```
Change the username globally.
### Change Global Email
```bash
git config --global user.email "<email>"
```
Change the email globally.
### Change Local Username
```bash
git config user.name "<name>"
```
Override global username per project.
### Change Local Email
```bash
git config user.email "<email>"
```
Override global email per project.

### Change Default Branch Name
```bash
git config --global init.defaultBranch <branch>
```

### Initialization
```bash
git init
```
Initialize current directory.

### Compare
```bash
git diff
```
When changes are made and they are saved but not yet staged then committed, you can use this command to see the modifications made.

## Staging
### Stage a File
```bash
git add <filename>
```
Add a file to staging area.

### Stage All Files
```bash
git add .
```
Add all files to staging area.

### Unstage a File
```bash
git rm --cached <filename>
```
Remove a file from the staging area.

### Unstage All Files
```bash
git reset .
```
Unstages all files but working directory won't be changed.

### Stage Previously Tracked Files
```bash
git add -u
```
Stages only the files that were previously tracked.

### Repository Status
```bash
git status
```
Display information about the state of the repository.

### Create a Commit
```bash
git commit
```
Create a commit in the current branch. An editor will open to enter commit description. Use `git commit -m "<description>"` for a faster commit creation. The `-a` option (`git commit -a`) can be used to add changes to staging area and commit them then an editor will open to enter commit description but this only applies to previously tracked files. Stage and commit files with `git commit -a -m "<description>"` or `git commit -am "<description>"` (only for previously tracked files).

### Display Commit History
```bash
git log
```
Display all commits in the current branch.

### Branches

#### Show Branch List
```bash
git branch
```
Shows a list of all branches in local repository. Use the `-r` option to show remote branches only (`git branch -r`). The `-a` option (`git branch -a`) is used to show all branches in local and remote repository. The `-vv` option (`git branch -vv`) shows local branches and their remote branches (tracking branches).

#### Create a Branch
```bash
git branch <branch>
```
Create a new branch by copying all commits in the current branch. The name shouldn't conflict with currently existing branches.

#### Delete Branch
```bash
git branch -d <branch>
```
Delete merged branch. This doesn't work on a branch that wasn't merged.

#### Force Delete Branch
```bash
git branch -D <branch>
```
Forcefully delete a branch that was not merged.

#### Change Branch Name
```bash
git branch -M <branch>
```
Change name of branch to the specified name.

#### Change a Specific Branch Name
```bash
git branch -m <branch> <branch>
```
First argument is the chosen branch that will be renamed and the second argument is the new name it will have.

#### Go to a Commit or Branch
```bash
git checkout <hash or branch>
```
You can use a commit's hash or a branch to change where HEAD points to which will become the currently checked out commit or branch.

#### Create and Checkout a Branch
```bash
git checkout -b <branch>
```
Create a branch and check it out.

#### Merge a Branch
```bash
git merge <branch>
```
Merge a branch into the current branch (get changes from a branch into the receiving branch).

### Remote Repository
#### Make Git Remember Upstream Branch
```bash
git push -u <remote> <branch>
```
Make Git remember an upstream branch (`git push -u origin temp`) in remote repository and remote is the remote server which turns the local branch into a tracking branch. This is a shorter version of `git push --set-upstream <remote> <branch>`.

#### Add a Remote Server
```bash
git remote add <remote> <url>
```
Remote is the server name and URL is the URL of the remote repository (`git remote add origin <url>`). More than one remote server can be added.

#### Push Changes to Remote Repository
```bash
git push
```
After testing of changes in local repository, push them to remote repository that Git remembers.

#### Fetch Changes From Remote Repository
```bash
git fetch
```
Get changes and metadata about remote branches references from remote repository but won't merge those changes. If a remote branch is deleted then this command is used, the references of remote branches in the local repository won't be updated. The `-v` or verbose option can be used (`git fetch -v`) to see more details.

#### Pull Changes From Remote Repository
```bash
git pull
```
Fetches changes from remote repository and merges those changes behind the scenes. The `-v` or option can also be added (`git pull -v`).

#### Remove Stale Branch
```bash
git fetch --prune
```
Cleans local repository by removing references of remote branches that were deleted.

#### Clone a Remote Repository
```bash
git clone <url>
```
Create a local repository based on the remote repository by using its URL. The branch created in local repository will be automatically be a tracking branch that is connected to the remote branch. A default branch defined in the remote repository will be the branch created in local repository.

### Reset
Reset is intended for private branches and not for public branches in remote like production, release, master, dev, etc.
#### Hard Reset
```bash
git reset --hard <hash>
```
It moves to the specified commit in history, deletes the commits after the current commit and discards all changes in the working directory and staging area.

#### Mixed Reset
```bash
git reset <hash>
```
Move to a specified commit in history, deletes the commits after the current commit then unstages the changes and keeps them in the working directory. Mixed reset is the default mode of reset command.

#### Soft Reset
```bash
git reset --soft <hash>
```
Moves to a specified commit in history, deletes the commits after the current commit then keeps the changes staged and in working directory.

### Stashing

#### Stash Changes
```bash
git stash
```
Git creates a temporary commit of uncommitted and even of staged and unstaged changes made in current branch and stores it in Git repository for later use then the branch goes back to its previous state without the changes.

#### Pop Stashed Changes
```bash
git stash pop
```
Get the previous changes stored in stash then apply those changes and then the stash file will be deleted in the Git repository.

### Show References
```bash
git show-ref
```
Check remote refs and local refs.

### Tags
#### Show Tag List
```bash
git tag
```
Show list of current lightweight and annotated tags. Lightweight and annotated tags can't be distinguished with this command.

#### Add a Lightweight Tag
```bash
git tag <name>
```
Add a lightweight tag to the current commit (`git tag v1.0.0`).

#### Add an Annotated Tag
```bash
git tag -a <name> -m "<description>"
```
Create an annotated tag (better tag) with tag name and tag description to the current commit.

#### Display Annotated Tag Details
```bash
git tag -v <name>
```
Show details of an annotated tag (`git tag -v v1.0.0`). This command won't work on lightweight tags.

#### Display Commit Details
```bash
git show <tag>
```
Get the commit with the specific tag (`git show v1.0.0`).

#### Push Local Tags to Remote
```bash
git push --tags
```
Push tags to remote. Use `-v` option for more details (`git push -v --tags`).

#### Push One Tag to Remote
```bash
git push <remote> <tag>
```
Push tag to remote (`git push origin v1.0.1`). The `-v` option can be used (`git push -v origin v1.0.1`).

#### Delete a Tag

### Show Changes in Commit
```bash
git show <hash>
```
See the changes made in the specified commit.

### Show Summary of All Commits
```bash
git shortlog
```
Show summary of all commits sorted by author name. Use `-n` to sort by number of commits (`git shortlog -n`). Suppress showing of commits with `-s` (`git shortlog -s`). The `-e` option is to show email (`git shortlog -e`). Options can be combined (`git shortlog -n -s -e`).

### Revert
```bash
git revert <hash>
```
Revert the changes made by one specific commit when changes were already pushed to remote by creating a new commit that inverses the changes made by the specified commit. (`git revert HEAD`). Can be used on public branches in remote like master, release, dev, production, etc. When the commit specified is not the last commit, conflicts might appear that should be resolved to continue revert operation. Works on only one commit. History of commits won't be changed.

### Rebasing
```bash
git rebase <branch>
```
Rebasing Steps:
1. `git checkout <branch>` - Go to feature branch to be rebased on top of base or main branch (`git checkout feature1`).
2. `git rebase <branch>` - Rebase feature branch on top of base or main branch (`git rebase main`). Git creates brand new commits that are copies of the old commits.
3. `git checkout <branch>` - Checkout base or main branch (`git checkout main`).
4. `git merge <branch>` - Merge feature branch into base or main branch (`git merge feature1`). Old commits from feature branch will be garbage collected because there's no more pointers there and feature branch pointer now points to brancd new commits.

A two step process to make commit history look linear. This command rewrites commit history and doesn't keep the entire history of all commits.

### Reflog
Reflog can be used in:
1. `git log` - Select an old commit that is not the last commit.
2. `git reset --hard <hash>` - Use the selected old commit.
3. `git log` - Check commits history.
4. `git reflog` - You will see the operation in the output of reflog.
5. `git reset --hard <hash>` - Use the commit previously show by reflog with HEAD@{1} counter to make repository go back to its previous state.
Show the entire history of all operations made in repository. Use `git reflog show <branch>` to see operations done in a branch. Only changes made in local repository can be seen in reflog. Instead of hash, you can use the references from the output of reflog (`git checkout HEAD@{6}`). perations in reflog are stored for only 90 days by default.

### Cherry Pick

## Git Concepts
### .gitignore
The first file that should be created after initializing a Git repository. Rules can be created inside that will help Git to know which files to ignore.

### Initialization
When a directory is initialized, a hidden .git folder will be created.

### Local Repository
A copy of remote repository that a team member or collaborator can work on in their own computer.

### HEAD
The current commit or branch.

### Detached HEAD State
Detached HEAD state happens when HEAD is pointing to a commit.

### Merging
Combine the changes from a feature branch into a receiving branch (which can be main branch).

### Remote
The remote server where the remote repository is. Usually named origin.

### Origin
The default name of remote server.

### Pull Request
Changes you want to be applied to a branch (usually main) that will undergo review by other team members and can be accepted or not.

### Commits
A state of a project in a specific moment of time.

### Branches
Contains their own commit history that are differnt from other branches. Allows team members to work on different features simultaneously. Branches can be merged to other branches.

### Merge Conflict
An error that appears when there are files that are in conflict with one another when trying to merge branches. The conflicts should be resolved first to proceed with merging.

### Stale Branch
When a tracking branch loses its corresponding upstream remote branch.

### Tracking Branch
A local branch becomes a tracking branch when it is paired with its corresponding remote branch.

- Git Objects
- Git Areas
  - Working Directory
  - Staging Area
  - Git Repository
- File Status Types
- Relative Refs
- Alias

## Git Experiments