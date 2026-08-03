---
layout: post
title: Git Commands
---

# Git

## Introduction

### Git Website
More information in [Git Website](https://git-scm.com/docs).

### What is Git?
Git is used to track your project and its old versions. When combined with an online repository like GitHub, it is possible to collaborate with two or more people simultaneously. Working on the same project is possible regardless of time or place.

### What is a Repository Hosting Service?
A repository hosting service like GitHub or GitLab is where Git repositories can be stored and be used as a centralized point of getting and giving project updates for collaboration.

## Terminal Basics (Git Bash)
Git Bash terminal or the terminal (bash) in VS Code can be used.

### Escaped Characters
`!` is used for history expansion in bash so it should be escaped with `\` as in `\!` or single quotes.

### Case Sensitivity
In Windows OS, using an uppercase or lowercase letter in the path both works like in `cd E:` and `cd e:` but creating a folder with uppercase letter like in `mkdir folder1` will clash with another command containing an uppercase letter like in `mkdir Folder1` since the folder already exists.

### Go to Root Directory
```bash
cd
```

Make the terminal go to root folder.

#### Activity - Go to Root Directory
1. Check current directory.
2. Go to a different drive.
3. Check current directory.
4. Go to root folder.
5. Check current directory.

```bash
pwd
cd E:
pwd
cd
pwd
```

### Move to a Specific Directory
```bash
cd <path>
```

Change directory to the relative or absolute path specified like in `cd Desktop` or `cd Desktop/new-folder`.

#### Activity - Move to a Created Folder
1. Check current directory.
2. Go to a different drive.
3. List folders and files in current directory.
4. Clear terminal.
5. Create a folder.
6. Go to the newly created folder.

```bash
pwd
cd E:
ls -la
clear
mkdir images
cd images
```

#### Activity - Move to a Nested Folder
1. Check current directory.
2. Go to a different drive.
3. List folders and files in current directory.
4. Clear terminal.
5. Create a folder.
6. Go to the newly created folder.
7. Create another folder.
8. Go to the created folder.
9. Go back one level (to go to images folder).
10. Go back another level (to go to the drive like [E:]).
11. Go to the last created folder by using a relative address (short address).

```bash
pwd
cd E:
ls -la
clear
mkdir images
cd images
mkdir company-logos
cd company-logos
cd ..
cd ..
cd images/company-logos
```

#### Activity - Move to an Absolute Address
1. Check current directory.
2. Go to another drive.
3. List folders and files in current directory.
4. Clear terminal.
5. Create a new folder.
6. Go to new folder.
7. List folders and files in the new folder.
8. Clear terminal.
9. Go to another drive.
10. List folders and files.
11. Clear terminal.
12. Go to the folder with an absolute address (complete address).

```bash
pwd
cd E:
ls -la
clear
mkdir images
cd images
ls -la
clear
cd C:
ls -la
clear
cd E:\images
```

### Go Back One Level
```bash
cd ..
```
Go back up one level in the directory.

#### Activity - Go Back One Level
1. Check current directory.
2. Go to another drive.
3. Check folders and files in current directory.
4. Create a new folder.
5. Go back one level.

```bash
pwd
cd E:
ls -la
mkdir images
cd ..
```

### Create Directory
```bash
mkdir <name>
```
Create a directory.

#### Activity - Create a Directory
1. Check current directory.
2. Go to another drive.
3. Check folders and files in current directory.
4. Clear terminal.
5. Create a new folder.
6. List folders and files in current directory.

```bash
pwd
cd E:
ls -la
clear
mkdir images
ls -la
```

### Create File
```bash
touch <name>
```
Create a file like in `touch file.txt`. Create two or more files by separating filenames with a space like in `touch file1.txt file2.txt`.

#### Activity - Create a File
1. Display current directory.
2. Go to another drive.
3. List folders and files in current directory.
4. Clear terminal.
5. Create a file.
6. List folders and files again.

```bash
pwd
cd E:
ls -la
clear
touch wishlist.txt
ls -la
```

#### Activity - Create Multiple Files
1. Go to another drive.
2. Show files.
3. Clear.
4. Create two files.
5. Show files.
6. Clear.
7. Create three files.
8. Show files.

```bash
cd E:
ls -la
clear
touch file1.txt file2.txt
ls -la
clear
touch file3.txt file4.txt file5.txt
ls -la
```

### List Files
```bash
ls
```
Lists files and folders in the current directory. `l` option can be used (`ls -l`) to show in table format or `a` option to show hidden files and folders (`ls -a`). It can be combined (`ls -la`) and a directory can be specified to see what's in it (`ls -la <path>`)

#### Activity - Use List Command
1. Display current directory.
2. Go to another drive.
3. Create a folder.
4. Create file1.txt.
5. Create file2.txt.
6. Create file3.txt.
7. Use list command.
8. Use list command with `l` option.
9. Use list command with `a` option.
10. Use list command with `l` and `a` option.
11. Go up one level.
12. Use list command with the relative address of the new folder.
13. Go to a different drive.
14. Use list command with an absolute address of the new folder.
```bash
pwd
cd E:
mkdir python-project
touch file1.txt
touch file2.txt
touch file3.txt
ls
ls -l
ls -a
ls -la
cd ..
ls -la python-project
cd C:
ls -la E:/python-project
```

### Clear Terminal
```bash
clear
```
Clears the terminal.

#### Activity - Clear the Terminal
1. Display current directory.
2. Go to another drive.
3. List the files and folders in the current directory.
4. Clear the terminal.

```bash
pwd
cd E:
ls -la
clear
```

### Open Folder in File Explorer
```bash
start .
```
Opens current folder in File Explorer. Using `explorer .` also works similarly. `open .` is the command in macOS. `open <filename>` can be used to open the file. The equivalent command for Windows or Linux is `start <filename>`.

#### Activity - Open Folder in File Explorer
1. Display current directory.
2. Go to another drive.
3. List files and folders in current directory.
4. Clear terminal.
5. Create a new folder.
6. Move to the new folder.
7. List files and folders in the new folder.
8. Clear terminal.
9. Create a file.
10. Open folder in file explorer.

```bash
pwd
cd E:
ls -la
clear
mkdir python-project
cd python-project
ls -la
clear
touch notes.txt
start .
```

### Display Current Directory
`pwd` - See what is the current directory.

#### Activity - Display Current Directory
1. Display current directory.
2. Go to another drive.
3. Display the current directory again.
4. Go to root folder.
5. Display the current directory one last time.

```bash
pwd
cd E:
pwd
cd
pwd
```

### Current Directory
`.` is the alias of the current directory.

#### Activity - Open the Current Directory in File Explorer
1. Display current directory.
2. Go to another drive.
3. List files and folders in the current directory.
4. Clear terminal.
5. Open current directory in file explorer.

```bash
pwd
cd E:
ls -la
clear
start .
```

### Parent Directory
`..` is the alias of the parent directory.

#### Activity - Go Back One Level
1. Display current directory.
2. Go to another drive.
3. List files and folders in current directory.
4. Clear terminal.
5. Create a new folder.
6. List files and folders again.
7. Go back one level.
8. List files and folders one last time.

```bash
pwd
cd E:
ls -la
clear
mkdir python-project
ls -la
cd ..
ls -la
```

### Edit File
```bash
nano <filename>
```
Use a text editor to edit a file like in `nano new-file.txt`. `ctrl + o` to write changes and `ctrl + x` to exit in nano.

#### Activity - Edit a File with Nano
Write `<!DOCTYPE html>` in the html file and then save it with `ctrl + o` then `ctrl + x` to exit nano. Open the file again and see its contents.

```bash
cd E:
mkdir git-folder
cd git-folder
touch index.html
nano index.html
nano index.html
```

### Autocomplete
Use tab key to autocomplete commands in the terminal. Press tab key twice to see choices. Can show available commands or possible directories in the incomplete command.

#### Activity - Use Autocomplete
Write `ex` in terminal and press tab key twice.

#### Activity - Use Autocomplete with Directories
Create a folder with similar names in the first part but different names for the second part then use autocomplete to see the choices when using the incomplete command `cd git-`.

```bash
cd E:
mkdir git-folder
mkdir git-tutorial
```

### Print
```bash
echo "<string>"
```
Print a string to terminal.

#### Activity - Display a String to Terminal
Display the string "Today is cloudy" to terminal.

```bash
echo "Today is cloudy"
```

### Help
```bash
man <command>
```
Display the details on a specific command like in `man clear`. Git Bash doesn't support `man`. Use `--help` like in `touch --help`. Press `ctrl + z` to close help from `man`.

#### Activity - Use Help
See the details of `exit` command.
```bash
exit --help
```

### Write
`>` is used to write to file like in `echo "Hello World" > another-file.txt`.
`>` will overwrite whatever is inside the file if the file already exists.

#### Activity - Create a File with a String then Overwrite
```bash
cd E:
mkdir git-folder
cd git-folder
echo "Today is raining" > file.txt
nano file.txt
echo "Hello World" > file.txt
nano file.txt
```

### Append
`>>` - Append to the file like in `echo "Another Line" >> another-file.txt`.

#### Activity - Create a File with a String in it then Append
```bash
cd E:
mkdir git-folder
cd git-folder
echo "Bread is breakfast" >> diary.txt
nano diary.txt
echo "Ordered a pizza this afternoon" >> diary.txt
nano diary.txt
```

### List File Contents
```bash
cat <name>
```
List contents of the file. `cat file.txt` will show contents of the file unless it is an empty file.

#### Activity - See the Contents of File
Use editor to write in the file and then use `cat` command to see the file's contents.

```bash
cd E:
mkdir git-folder
cd git-folder
touch index.html
nano index.html
cat index.html
```

### Remove File / Directory
```bash
rm <file / directory>
```
Remove file or directory by putting the name of file or directory like in `rm new-folder` (directory needs to be empty to be deleted). `rm -rf <name>` forcibly removes files inside a folder recursively (deletes the folder) like in `rm -rf new-folder`. If removing a file, the path to the file can be used like in `rm folder/file.txt`.

#### Activity - Delete Files and a Folder
```bash
cd E:
mkdir folder1
cd folder1
touch file1.txt
ls
rm file1.txt
ls
mkdir folder2
cd folder2
touch file2.txt
ls
cd ..
rm folder2/file2.txt
cd folder2
ls
cd ..
rm folder2
```

### Close Git Bash / Bash Terminal in VSCode
```bash
exit
```
Close the terminal.

#### Activity - Close the Terminal
```bash
pwd
ls -la
clear
exit
```

### Hidden Files
Hidden files start with a `.` in Unix-like systems. In Windows, files and folders are hidden depending on the file / folder attribute.

## Git Concepts

### Git Objects
Git stores blobs, trees, commits and annotated text in the Git repository.

### Three Main Areas in a Project
- Working Directory - Contains untracked, modified and unmodified files.
- Staging Area - Contains staged and unmodified files.
- Git Repository - Contains unmodified files.

#### Working Directory
Untracked files are in working directory.

#### Staging Area
Sits between working directory and Git repository. It is usually called index and it is actually responsible for preparing files to be inserted into the Git repository and also in the opposite way, It prepares file taken from Git repository to be put into working directory. Putting files into staging area is a mandatory step in all operations either when you want to place files from working directory into Git repository or when you want to read files from Git repository and checkout them into your working directory.

#### Git Repository
Unmodified files are in Git repository.

### File Status Types
Every file in Git may have one of four tracking statuses:
1. Untracked - File only exist in working directory.
2. Tracked - Files that are monitored by git.
   - Modified - Use git add to put this file to staging area (Deleted is another state and it is also added to staging area).
   - Staged - This file is still located in working directory but is only written in staging area for simplicity's sake. If `git commit` is not used, the file in Git repository is an old version of the staged file.
   - Unmodified - Files that are present in working directory, staging area and Git repository.
3. Ignored - Files that are excluded from staging and committing.
4. Committed - Committed files are saved in Git and a new commit will appear in commit history. The changes are only saved locally. If there is one or more commits, those changes can be pushed to the Remote Repository.

### Setup

#### Display Git Version Number
```bash
git --version
```
Get the version of Git. Also helps in checking if Git is installed (`git -v` and `git version` works similarly).

#### Display Configuration
```bash
git config --list
```
Display the current Git configuration.

#### Display Global / Local Username
```bash
git config user.name
```
Show the global username when not inside a Git repository. It will show the local username when inside a Git repository.

#### Display Global / Local User Email
```bash
git config user.email
```
Show the global user email when not inside a Git repository. It will show the local user email when inside a Git repository.

#### Change Global Username
```bash
git config --global user.name "<name>"
```
Changes the name that will be displayed in the commits.

#### Change Global Email
```bash
git config --global user.email "<email>"
```
Changes the email displayed in commits.

#### Change Local Username
```bash
git config user.name "<name>"
```
Override local username per project. Should be done inside a Git repository.

#### Change Local Email
```bash
git config user.email "<email>"
```
Override local email per project. Should be done inside a Git repository.

#### Change Default Branch Name
```bash
git config --global init.defaultBranch <branch>
```
Change branch into main to change the default name of branch in initialization to main (used when default name of branch isn't main). The branch name will change when using `git init` command. The changes in settings can be seen with `git config --list`.

#### Initialization
```bash
git init
```
Initialize current directory as Git repository. It will create a hidden `.git` folder that can only be managed by Git. This is about local repositories. Not related to remotes (remote repository).

##### Activity - Initialize a Git Repository
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

#### Local Repository
A copy of remote repository that a team member or collaborator can work on in their own computer.

### Inspect

#### Repository Status
```bash
git status
```
Display status of Git repository (but doesn't show files in staging). Can be used with verbose option (`git status -v`). Depending on the terminal, yellow cross signs means uncommitted changes and those changes to be committed are located in staging area. Yellow cross signs will disappear and it means there are no changes to be committed.

#### Display Commit History
```bash
git log
```
Display all commits in the current branch. Ctrl + z to exit. Show history of changes (commits). See all commits that were created in history. Press Q to exit. Use `git log --oneline` to see one line in the output. Use --stat to see additional information as in `git log --stat`. The -p option shows changes in every file or every commit as in `git log -p` but it is not convenient to see changes in terminal (use gui programs like vscode or sourcetree instead). Using `git log -<number>` will only show a specific number of commits as in `git log -4` and --oneline can be added to it as in `git log -4 --oneline`. `git log --graph` will show commits history with branch connections. We can see how many parents and can be combined with --oneline as in `git log --graph --oneline`.

#### Format Output of Git Log
`git log --pretty=format:"%H"` - Shows log of commits but formatted. %H is variable for complete hash of commits. Add cn to see committer names as in `git log --pretty=format:"%cn %H"`. More pretty formatting variables in https://devhints.io/git-log-format. Short hash is h as in `git log --pretty=format:"%cn %h"`.
Strings can also be added as in `git log --pretty=format:"Author of commit: %cn Commit SHA1 hash: %h"`. Date can be added with cd as in `git log --pretty=format:"Author of commit: %cn; Commit SHA1 hash: %h; Date: %cd"`

#### Show Merge Commits and Non Merge Commits
`git log --merges` - The option --oneline can be used as in `git log --merges --oneline`. Only show merge commits. There is a reason why there can be few merge commits in a repository and why in some cases people do not merge branches in traditional and they use rebasing with squashing instead. `git log --no-merges` can be used to see non merge commits (commits made by humans or merges using other techniques). Option --oneline can also be used as in `git log --no-merges --oneline`.

#### Filter
`git log --author="<name>"` - The filter is actually regular expression and you can enter a part of the author name and it will find results the same as before. Show commits made by an author. The `--oneline` can be added as in `git log --author"AchillesJ" --oneline`. Find specific string with `git log --grep="<query>"` as in `git log --grep="3.12.1"` to find commits with the string. The `--oneline` can also be added.

#### Compare
```bash
git diff
```
When changes are made and they are saved but not yet staged then committed, you can use this command to see the modifications made. With `git diff`, if a file is modififed and that file is saved, `git status` will show one file is modififed. Without staging and committing, use `git diff`. A will mean the previous file and B represents modified file. Click in VS Code to see those two side by side. You will also see hashes of the two when `git diff` is used. Modififed version got a hash even if it isn't staged yet. If a number like -3, 6 +3, 8 shows, it means old file with - is displayed with line 3 as the one we see and there are 6 lines total. The modified file is + and the displayed code start at line 3 and there are a total of 8 lines. Only a portion of the whole code is shown. We also see a text that is part of the code beside the numbers. We can copy those text and find it to see portion of the code that was changed. Scroll down in command line with down arrow key. You can stage and commit after using `git diff`.

#### Show Changes in Commit
```bash
git show <hash>
```
See the changes made in the specified commit.

#### Show Summary of All Commits
```bash
git shortlog
```
Display a summary of all commits.

`git shortlog` - Show summary of all commits. You can see which authors made more commits and you can sort the output in descending order starting from authors that made more commits. By default, this will be sorted by author name. You will see commits made by author. Use -n to sort by number of commits as in `git shortlog -n`. Suppress showing of commits with -s (show summary) to only show author and number of commits as in `git shortlog -n -s` while -e is to show email as in `git shortlog -n -s -e`. `git shortlog -nse` also works similarly.

#### Alias
```bash
git lg
```
Show history of commits with author and when were commits made but not much detail (no date).
If `git lg` is not available, create an alias for it with `git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%C(bold blue)<%an>%Creset' --abbrev-commit"`.

#### Show References
```bash
git show-ref
```
Check remote refs and local refs.

#### Compare References for a specific Branch
`git show-ref <branch>` - When branch is master, you will only see references for master branch in local master master and remote master branch. Branch can be other branch. The references can be different or exactly the same. When a commit is made but not yet pushed, references will be different. When pushed, the references will become the same and it means local and remote branch are in sync.

### Staging
#### Stage a File
```bash
git add <filename>
```
Add a file from working directory to staging area. Staging multiple files can be done by separating two files or more with a space as in `git add file1.txt file2.txt`.

#### Stage All Files
```bash
git add .
```
Add all files to staging area. When the project folder is new, there are only a few files so using this is ok but later on, you don't want to add all files and then realize only few files need to be added to staging.

#### Stage Previously Tracked Files
```bash
git add -u
```
Stages only the files that were previously tracked. Might be better than `git add .` since at first the project is small and we can add all files to staging area but as the project grows, there will be cases where we don't want to add all files to staging if we end up with a lot of new untracked files in our project folder.

#### Unstage a File
```bash
git rm --cached <filename>
```
Remove a file from the staging area if changes haven't been committed yet. Changes file to untracked or modified state from staged. Doesn't remove file from working directory.

#### Unstage All Files
```bash
git reset .
```
Unstages all files but working directory won't be changed.

### Blob
Git stores any files with any extensions: either video files, pictures, text files. They are stored as blobs. A blob represents a single file in a Git file system.

### Tree
With the help of tree object type, Git actually stores information about directories. In other file systems, directories may contain files or be empty or be mixed with files and directories. Tree in Git may be a set of blobs or set of blobs and other trees. Tree is representation of folder in Git. Tree represents a directory.

### Commits
With a commit object type, we are able to actually store different versions of our project. A commit is like saving the state of a project in a specific moment of time. But saving (or just creating a commit) is not enough to make sure the we won't have to worry about the project. Pushing the commit or commits to remote (remote repository) will later on allow us to get all versions of our project even if our local Git repository or project folder is gone from our computer. Pushing to remote also allows collaboration with other people.

#### Hash Function
There is an online tool for generating hash. Git utilizes SHA1 function and uses hexadecimal format.
Hash Functions:
- MD5 (128 bit)
- SHA1 (160 bit)
- SHA256 (256 bit)
- SHA384 (384 bit)
- SHA512 (512 bit)

#### Hash
String of numbers and letters. It is like an ID. Generated based on input. We store files in Git based on their hash. Hash function is a function that takes any variable length input and creates a fixed length hash. Hash can be created with a very small file or big sized file. Hash depends on the content. If you know the hash but don't know the input, you can't create the input based on hash. Hash functions are one-way functions. We are not able to find out input based on specific hash. Passwords are stored as hash. A server creates hash of the password and compares it to hash stored in database on log in. Same input will produce the same hash.

#### Create a Commit
```bash
git commit
```
Create a commit in the current branch. An editor will open to enter commit description. 

#### Commit and Write Description in Terminal
```bash
git commit -m "initial commit"
```
Use `git commit -m "<description>"` to enter description in terminal without opening an editor. 

#### Stage and Open Editor to Create Description then Commit
```bash
git commit -a
```
The `-a` option (`git commit -a` can also be used after resolving a merge conflict where you will see commit message and if you are happy with it type :wq then press enter and then merge will be successful) can be used to add changes to staging area (previously tracked files) and commit them then an editor will open to enter commit description but this only applies to previously tracked files.

#### Stage Previously Tracked Files and Commit
```bash
git commit -am "<description>"
```
Stage and commit files (only for previously tracked files) with `git commit -a -m "<description>"` or `git commit -am "<description>"`.

### Branch
A branch contains its own commit history that are different from other branches. Allows team members to work on different features simultaneously (by making a branch for each feature). Branches can be merged to other branches. A branch is like a bookmark which is easy to remember instead of memorizing the hash of a commit so checking out a branch is fast and easy than checking out a commit that will have different hash whenever the branch is updated with a new commit that is why branch is useful since it will automatically bookmark the newest commit added to the branch.

#### HEAD
The current commit or branch. There can only be one HEAD. HEAD is current commit or branch. By default HEAD points to current branch and it moves of course along with branch. You can also checkout specific commit by using its hash, where you will move into detached HEAD state. It is the name of the currently checked out commit. HEAD normally points to a branch name.

#### HEAD File
Contains pointer to currently checked out branch which can be master branch.

#### Show Local Branches
```bash
git branch
```
Shows a list of all branches in local repository. The branch with `*` is the current branch. This won't show branches created in remote repository. Use the `-r` option to show remote branches at remote Git repository only (`git branch -r`). The `-a` option (`git branch -a`) is used to show all branches in local and remote repository. If it is remote, there will be a remote name and then followed by name of the remote git server which can be origin and then followed by name of branch. Head pointer will point to remote's default branch which can be remote's master or main branch and that default branch is the one that is default branch created for local after cloning.The `-vv` option (`git branch -vv`) shows local branches and their remote branches (tracking branches). If there is origin/master, it means local branch is tracking branch and it tracks origin/master branch. We can see if a remote branch is gone with this command after using git `remote update origin --prune`.

#### Create a Branch
```bash
git branch <branch>
```
Create a new branch by copying all commits in the current branch. The name shouldn't conflict with currently existing branches. Use `git branch <branch> <source>` to create a branch with a specified source branch without checking it out. Use `git branch -f <hash>` to move a branch forcefully to a commit or use relative refs instead of hash. `git branch -f` is not allowed for current branch in a real Git environment.

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
You can use a commit's hash or a branch to change where HEAD points to which will become the currently checked out commit or branch. Checkout a remote branch in remote repository to create a local tracking branch with `git checkout <branch>` and then the new local branch will track remote branch. After checking out specific version of the project, you can easily move on and make any changes, add new files to your project, commit those changes and so on. It also replaces files in staging area. This command will completely override contents of your working directory. To return to Head State, use `git checkout main`. Discard changes done while in detached head state by using `git checkout -f main` where `-f` means force.

#### Create and Checkout a Branch
```bash
git checkout -b <branch>
```
Create a branch and check it out.

#### Detached HEAD State
Detached HEAD state happens when HEAD is pointing to a commit.

`git branch <branch> <hash>` - After going back to another branch from detached head state, create branch for experimental commits.
When in last experimental commit while in detached head state, `git checkout -b <branch>` can be used to save experimental commits. If you are just experimenting and will throw away changes, just go to another branch while in detached head state. By default, unreachable git objects are garbage collected after 30 days. New commits created while in detached head state will not be included in master branch and while creating new commits in detached head state, creating a branch is ok to make sure those changes are not lost. Sometimes when you want to retain experimental commits, you can create a branch while in detached head state. While in detached head state, you can create experimental commits and if you go to a branch and out of detached head state, those experimental commits will be garbage collected by git. When head points to a currently checked out branch, creating new commits will automatically make head point to the new commits. Checking a specific commit with its hash will make head go into detached head state. Checking out a specific commit. If you make a commit while located in detached HEAD state, those commits that were made in detached HEAD state will be lost and deleted automatically by Git and you will not be able to return to those commits. That is why in most cases, HEAD is referenced to specific branch, not commit.

#### Merging
Combine the changes from a feature branch into a receiving branch (which can be main branch).

##### Receiving Branch
If we want to merge a branch to main, main is the receiving branch.

##### Fast Forward Merge
When a branch is created from master branch and the new branch got a commit and there are no new commits in master branch, checking out master branch and merging the new branch to main with `git merge <new-branch>` will just move master branch pointer to point to the new commit where new branch points to. The new branch can be deleted with `git branch -d <new-branch>`. Git simply moves HEAD pointer. Git won't create a new commit. If there are no new commits in main branch and another branch based on main got new commits, we can merge that branch to main and Git will use fast forward merge. Main branch will simply move to the last commit of the other branch that was merged. You can delete the other branch if you're not going to make any other changes in it. If we want to merge a branch like `bugFix` to main, we need to checkout main first and then use `git merge bugFix`. main pointer will point to the commit to where bugFix points.

##### Three Way Merge
Git will create new merge commit that will contain all changes.

##### Merge a Branch
```bash
git merge <branch>
```
Merge a branch into the current branch (get changes from a branch and put them into the receiving branch). `git merge` is then performed locally in local repository. `git commit` is needed to complete merge if there is merge conflict and conflicts are resolved. In a 3-way merge, vim will open to edit the reason of why merging is needed. press i to use insert mode then edit the message. press escape to exit insert mode. type `:wq` then enter to exit. To merge a branch named br1 to main, we must checkout main branch first and then use `git merge br1`. br1 branch can then be deleted. We use merging if we want to incorporate changes made in one branch to another branch. Combines the work from two different branches. If main is the current branch and we want to merge bugFix branch to main branch, we use `git merge bugFix` then a new commit with two parents based on the branches merged will be created and main will point to the new commit. We can then checkout bugFix and merge main with `git merge main` so bugFix will just point to the new commit and update bugFix branch. When git performs 3-way merge, it will create automatic commits (automatically created by git) and these commits are not made by humans.

#### Move Branch
```bash
git branch --force <branch>
```
Move branch to current commit.

```bash
git branch --force <branch> [<new-tip-commit>]
```
`new-tip-commit` can be a branch name (ex. master, origin/master) and branch will be moved there.

### Relative Refs
- `git checkout <branch>^` - Caret Operator - If main is the current branch, find the parent of the specified commit so `git checkout main^` means we checkout the parent of main and `git checkout main^^` means the grandparent of main. Using `git checkout HEAD^` can be useful too to get the parent of HEAD.
- `git checkout HEAD~<number>` - Tilde Operator - Move up the commit history four times from where HEAD is. Use `git branch -f main HEAD~3` to move main branch three parents behind HEAD forcefully (in a real Git environment `git branch -f` is not allowed for your current branch).


### Remotes (Remote Repository)
Remote is the remote server where the remote repository is. Usually named origin. We need to be connected to the internet.

#### Add a Remote
```bash
git remote add <remote> <url>
```
Add a remote by putting its name and URL like in `git remote add origin https://github.com/millenniumdisk/learn-programming.git`(create a reposiroty first in a repository hosting service like GitHub). More than one remote can be added by changing the name of the other remote from origin to something else.

#### Origin
An alias for remote repository URL. When using `git pull`, you will pull from origin which is the default remote repository. Origin can be thought of as a default name of remote repository. 

#### Make Git Remember Upstream Branch
```bash
git push -u <remote> <branch>
```
Make Git remember an upstream branch (`git push -u origin temp`) in remote repository and remote is the remote server which turns the local branch into a tracking branch. This is a shorter version of `git push --set-upstream <remote> <branch>`.

`git push` - The -u in `git push -u origin <branch>` makes git to remember the upstream branch. In `git push -u <server> <branch>` or `git push -u origin <branch>`, branch can be master branch and remote branch will be created in remote server. Set upstream branch for local branch with `git push -u origin <branch>` where git will get branch from origin remote server and origin can be changed to other remote server. `git push -u origin <branch>` is used to track remote branch after set up of remote server. When local branch has a corresponding remote branch the local branch becomes a tracking branch, the command `git push` instead can be used when making a new commit and push changes to remote branch. To create a remote branch when a new local branch is created then local branch will track the new remote branch, use `git push --set-upstream origin <branch>` (branch is going to be the name of remote branch) where branch is the same name of local branch since it is what will be suggested in the terminal and origin is the name of server and origin is default name and instead of the longer command, `git push -u origin <branch>` can be used and -v option can also be added as `git push -v -u origin <branch>`. If we push a local branch with `git push -v` and there is no corresponding remote branch that is tracked by the local branch, there will be a prompt that says there's no upstream branch. After testing and you are happy with the changes, you can push the changes from your local git repository to the remote git repository. Put your changes to remote repository. Publish local branch with `git push --set-upstream origin <branch>` where upstream branch is a remote branch that your local branch tracks. When you set an upstream branch, you link your local branch to a branch on the remote repository. You push a local branch to the origin remote repository. The command `git push -u origin <branch>` can be used instead. The `-u` says the branch is an upstream branch and origin is the name of the remote repository. Both `--set-upstream` and `-u` establish a tracking relationship between your local branch and the remote branch so in the future, pushing from local branch to remote branch only needs `git push`. git push -u origin main` To put the changes in main branch to remote repository. Another version can be used with -v option as `git push -v` and there will be a prompt asking for GitHub account username and password then remote branch will point to the commit in local branch and git updates local tracking reference for refs/remotes/origin/branch where branch is the remote branch name and local branch and remote branch will point to the same commit. Changes in local repository will be incorporated into remote repository.

#### Stale Branch
When a tracking branch loses its corresponding upstream remote branch.

A tracking branch in local repository will become stale if the remote branch is deleted in remote repository. Use `git remote prune origin` to remove the stale branch configured for `git pull`. The local branch will still exist and is still tracking the removed remote branch. You can create the removed remote branch by using `git push` after making changes to the local branch. Local branch can also be deleted if you won't push changes and create removed remote branch.

#### Tracking Branch
A local branch becomes a tracking branch when it is paired with its corresponding remote branch.

Tracking branch can be removed by deleting local branch with `git branch -d <branch>`. If there is a branch in remote repository named b1 and there is no local branch that tracks b1 branch, it means there is no local tracking branch for b1 branch. If there is a local branch named b2 and there is no branch in remote repository that is connected to it, it means that b2 branch is not tracking branch.
You can create remote tracking branch for b2 by creating remote branch in remote repository. The same for b1 branch, just checkout remote branch and you will create local b1 branch in local repository and this will automatically be connected to remote branch and the branch will be tracking branch.
Tracking branch is local branch that is connected to a specific remote branch in remote repository. There can be a single tracking branch called master and local master branch tracks remote master branch.

#### Even With Master
It means the branch is up-to-date or in sync with master branch.

#### Merge Conflict
An error that appears when there are files that are in conflict with one another when trying to merge branches. The conflicts should be resolved first to proceed with merging.

#### Resolve Merge Conflict
- Checkout the main branch.
- Pull the changes from the remote main branch (your local main branch and remote main branch are identical).
- Checkout to your branch (when creating the pull request, you are trying to merge to main and `git merge main` will merge the main branch into your branch even if the initial goal was the opposite which was to merge your branch to main branch so we must resolve the issue by merging main to our branch to identify the problem).
- View the merge conflicts list in your code editor (arrows pointing to left are from our branch and arrows pointing to right are changes coming from the main branch).
- You can manually choose what you want to keep or remove by removing the lines and clearing code you don't want there.
- Click resolve button if you don't want to manually resolve (you can choose to only accept yours or accept their code or you want something in between but in most cases you want some of their code and some of your code so use third option merge).
- In the left side of the code editor, we see our changes, the right side is their changes and in the middle is the result (click double arrows you want to keep and x button to remove code you don't want to keep then apply).
- Stage all files.
- Commit with description.
- Push changes.
- Pull request won't have any merge conflicts error so tag reviewer in the message and tell them to check it.
- Some will request changes if needed by commenting on the pull request when going to the code base (files changed in GitHub).
- Merge pull request to main branch will happen next.
- A new commit will appear.

#### List Remote Repositories
`git remote` - Show the remote servers that were already set up. Show the remote servers for your local repositories. Using `git remote -v` will show two URLS for fetch and push commands. A local repository that is not connected to a remote repository will have an empty output when using `git remote`. It doesn't matter what the branch is for `git remote`. Use `git remote show origin` to show local stale branches and entire information about the connection between local repository and remote repository. See additional information and not just the URLS used for fetch and push (origin can be changed to other remote server name). Head branch is default remote branch in remote repository. You will see list of remote branches and if they are tracked (with tracking branches for push and pull). If we see up-to-date, it means branches are in sync.

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

`git fetch` - Can be used as `git fetch -v` (verbose option) to see detailed operation and helps in seeing how many branches are in remote. It will not create local tracking branch. Can be used in any branch. When a new remote branch is created in remote repository, the new change can't be seen with `git branch -r` or `git branch -a` so `git fetch` should be used first to get remote changes and put them in local repository and it is not destructive since it won't change working directory and staging area and it will not merge any remote changes to your local changes. Get changes from remote git repository and updates the local git repository. Local working directory and staging area are not touched. If a branch is created in remote git repository, that branch can be seen in local git repository after using `git fetch`.

#### Pull Changes From Remote Repository
```bash
git pull
```
Fetches changes from remote repository and merges those changes behind the scenes. The `-v` or verbose option can also be added to observe fetch and merge operations (`git pull -v`).

`git pull` - The option -v can be used as in `git pull -v` for detailed pull. We need a local tracking branch to use `git pull`. Operation is performed partially, only locally in your git repository and it is a two step process of fetching remote changes and then merging them into local changes. A destructive operation that also updates the working directory and staging area because the changes from remote git repository is merged to the local git repository. Is the command to use to make your local branch up-to-date when somebody made changes to remote branch either directly or by merging other changes into it. This command fetches changes from the remote repository and merges them into your local repository for that branch.

#### Remove Stale Branch
```bash
git fetch --prune
```
Cleans local repository by removing references of remote branches that were deleted. `git remote prune origin` will remove stale branch.

#### Clone a Remote Repository
```bash
git clone <url>
```
Create a local repository based on the remote repository by using its URL. The branch created in local repository will be automatically be a tracking branch that is connected to the remote branch. A default branch defined in the remote repository will be the branch created in local repository.

Only default remote branch is created as local branch (not all remote branches in remote repository is created in local branch with this). Git automatically creates binding between remote repository and local repository default remote repository is created for local repository and the name of the default remote repository is origin. Local repository can be connected to multiple remote repositories and every remote repositories will have different names and when you use push, pull or fetch, you choose which remote repository you want to interact with. To clone a repository, use `git clone <url>` to download a project with its Git repository where the url is from a git hosting service like GitHub. When you clone a repository, Git automatically names the remote repository as origin (origin is url of remote repository).

#### Update Tracking Statuses
`git remote update origin --prune` - Removes a remote branch from being tracked by a local branch if remote branch is deleted. Use the command so that git will know there is no remote branch. When a remote branch is created and then a branch for it is created locally with `git checkout <branch>` where branch is the new remote branch and remote branch will be deleted and then fetch and use `git branch -vv` to see local branch is still tracking the deleted remote branch so use `git remote update origin --prune` to update status of tracking branch and tracking status will change for local branch. The local branch can be deleted with `git branch -D <branch>` or force deletion because there will be an error with `git branch -d <branch>` because local branch is not merged.

#### Update All Branches Set to Track Remotes
`git remote update`
Only updates all branches set to track remotes. No changes will be merged. `git remote update origin` is another command.

#### Delete Remote Branch
`git push origin -d temp` - Delete remote branch. We can create a local branch and then create and track remote branch by using `git push -u origin temp` then use `git push origin -d temp` to delete remote branch. Check with `git branch -a`. Delete local branch with `git branch -D <branch`>

### Mktree
`git mktree` - Low level git command. Create new tree object.

### Hash-object
`git hash-object` - Low level git command. Create new object in Git structure. `echo "Hello, Git" | git hash-object --stdin -w` creates an object file.

### Cat-file
Low level git command. Reads Git objects.
- `git cat-file -p <hash>` - Contents of the object will be printed to terminal.
- `git cat-file -s <hash>` - Size of the object will be printed to terminal.
- `git cat-file -t <hash>` - Git type of the object will be printed to terminal.

### Config File
Config file is a configuration of your Git repository and default settings.

### Management of Blobs and Trees
For management of blobs and trees, we will use low level git commands like `git hash-object` and `git cat-file`.

### Pipe Symbol
`echo "Hello, Git" | git hash-object --stdin` - We take the output of another command as input of a different command with pipe symbol.

## Advanced
Advanced Git commands are not used very often but in some cases can be really useful. Some of these features are destructive (changes git history).
Topics:
- Revert commits.
- Reset commits.
- Amend commits.
- Cherry pick commits.
- Rebasing with squashing (useful when you want to collapse multiple commits just into one commit and perform rebasing).
- Advanced filtering options that could be used with `git log`.

### Pull Request
Changes you want to be applied to a branch (usually main) that will undergo review by other team members and can be accepted or not.

Each pull request is connected to a specific branch. Start review process. A dev creating a pull request wants to merge the feature into main branch and pull request can be called merge request. Pull request is named pull request because when a dev finish a feature, he will push it to remote repository he will ask other devs to pull remote changes in the specific branch, check it out and veryify how the feature works and give feedback. Pull requests help devs communicate and collaborate and move development process easier and faster.
When a dev has finished working on a specific branch and commits of changes were created and branch was published to remote, it is not good in most cases to merge those changes into main / release branch directly so a dev that has finished its work on a specific feature proposes changes that should be applied to main branch that may or may not be applied into master / release. After review of other devs, changes may be rejected and then pull request will be closed and corresponding branch will be deleted. Proposal of potential changes. Lets you share your changes with your team for review and feedback. Once approved and merged, your changes becomes a part of the main branch. Compare is the branch you want to merge from and Base is the branch you want to merge to in GitHub. If everything looks good and there are no merge conflicts, others can merge it. Your branch will be merged to main branch. Old branch will be one commit behind and zero commits ahead so it is ok to delete it. GitHub executes a Git operation in the background which is `git merge <branch>` and then the branch you want to merge. Using GitHub's PRs is preferable. Merge happens only in the remote repository so update local repository with `git pull` (this command is shorthand for `git pull origin main` but by default GitHub pulls from the remote origin from the same branch you're currently in).

### Annotated Tags
Annotated tag is one of the four Git objects and it is a persistent text pointer to a specific commit. There are two types of tag: lightweight tag and annotated tag. Annotated tag is better because it contains more information.

#### Semantic Versioning
Major version number is the first followed by minor and last is patch number like in ver. 3.7.2 and if big changes were applied to the software and it makes it not backwards compatible and the major number should be incremented and the rest will become 0 like in 4.0.0. Minor is small feature that adds some functionality but doesn't break anything in the previous version and other packages that are dependent on the software will continue to work the update like from 3.7.2 to 3.8.0 and the last number will become 0. Patch is a small bug fix or small feature adjustment like from 3.7.2 to 3.7.3. It is not recommended to automatically install any major updates since they may contain some incompatible changes that will break functionality of your software package. NPM contains packages and npm can automatically update if you are happy with minor updates like in node-sass. Pre-release versions are 5.2.4-alpha or 5.2.4-beta or 5.2.4-1.3 in staging environment where you test new features. 5.2.4-1.3 can be incremented to 5.2.4-1.4 and when pre-release features were properly tested, you can move to release version and release next version of software and release 5.2.4. It means 5.2.4 is greater than 5.2.4-1.4 and 5.2.3 may be the stable version. The rc in 2.0.0-rc.2 is release candidate and use rc when you are pretty close to release next software version and 2.0.0 is greater than 2.0.0-rc.2 and 2.0.0-rc.2 is greater than 2.0.0-rc.1.

#### Show Tag List
```bash
git tag
```
Show list of current lightweight and annotated tags. Lightweight and annotated tags can't be distinguished with this command.

#### Add a Lightweight Tag
```bash
git tag <name>
```
Always use an annotated tag instead of a lightweight tag since it is a more detailed tag.

Add a lightweight tag to the current commit in current branch (`git tag v1.0.0`). Stored in .git/refs/tags (stored where branches are which are also pointers) Just a text pointer to a specific commit.

#### Add an Annotated Tag
```bash
git tag -a <name> -m "<description>"
```
Create an annotated tag (better tag) with tag name and tag description to the current commit.

Message is required. Create an annotated tag and author and date will be added automatically. It is not possible to distinguish the difference between lightweight tag and annotated tag when using `git tag` but using `git tag -v <tag>` as in `git tag -v v1.0.0` will show details of the annotated tag. Signature can be added to annotated tag.

- Added with `git tag -a v1.0.0 -m "<message>"` like in `git tag -a v1.0.0 -m "New tag"`.
- Stored in .git/refs/tags.
- Also stored in .git/objects.
- Stores tag message.
- Stores tag author and date.
- Description is optional to add.
Git tags are not pushed to remote by default with `git push` because if any devs can push tags then there will be conflicts in tag names. Tags should have unique names. When creating a lightweight tag, a new file will be created and inside the file is pointer to specific commit. Annotated tag or text is used to store not only the tag but also the tag message and tag author will be from git configuration. Use only annotated tags because it got dates unlike lightweight tags. Annotated tag is git object. Create tags with different names. Tag names should be unique across the entire repository. When major features are merged into master branch, you can add a specific tag (like v1.2.0). Mostly used to add release versions of the project. If you make some commits in detached head state and then go back and check out master branch or other branch, those commits made in detached head state will be removed by git (garbage collected). You can check out specific tag and you will move to specific commit (goes into detached head state). You can create tags anywhere in the project at any time. Tags don't move while branches are developing and tags will still point to specific commits. Git tag is a static text pointer to a specific commit in commit history (branches are dynamic because they move when there is a new commit). Used for adding software version numbers. When a branch is merged, a minor version is incremented and if another branch is merged, patch number can be incremented depending on what feature is added and tag is added on the new merge commit created after merging.

#### Display Annotated Tag Details
```bash
git tag -v <name>
```
Show details of an annotated tag (`git tag -v v1.0.0`). This command won't work on lightweight tags.

#### Display Commit Details with Tag
```bash
git show <tag>
```
Get the commit with the specific tag (`git show v1.0.0`).

#### Push Local Tags to Remote
```bash
git push --tags
```
Push tags to remote. Use `-v` option for more details (`git push -v --tags`).

When pushing tags, commits are not pushed to remote (use `git push` to push commits to remote). Pushes local tags to remote git server. The command `git push -v --tags` can also be used for a detailed output with verbose option. `git push -v origin <tag>` as in `git push -v origin v1.0.1` only pushes tag to remote git server.

#### Push One Tag to Remote
```bash
git push <remote> <tag>
```
Push tag to remote (`git push origin v1.0.1`). The `-v` option can be used (`git push -v origin v1.0.1`).

#### Delete a Tag
```bash
git push --delete origin <tagname>
```
The `git push -d origin <tagname>` can also be used to delete a tag or push an empty ref to the remote tag name (`git push origin :tagname`). The command `git push origin :refs/tags/<tagname>` can be used to be sure that a branch won't be deleted because Git has a tag namespace and branch namespace. The command `git tag --delete <tagname>` or `git tag -d <tagname>` will delete the local tag.

#### Create Tags in GitHub
Go to releases and click draft a new release.

### Ignore Files in Git
- Explicitly tells Git which files and folders to ignore.
- Changes in ignored files and folders are ignored.
- Rules are defined in the separate file .gitignore.
- .gitignore file itself must be committed.

#### .gitignore File
The first file that should be created after initializing a Git repository is the .gitignore file. Rules can be created inside that will help Git to know which files to ignore.

#### Ignore Previously Committed File
Option 1
- Add ignore rule in .gitignore.
- Delete file in working directory.
- Commit changes.
Option 2
- Add ignore rule in .gitignore.
- Delete file only from repository keeping it in the working directory by using command `git rm --cached <filename>` as in `git rm --cached new-file.txt` and git will automatically stage this change.

#### Ready to Use Ignore Template for Different Programming Languages / Frameworks
Ignore the following:
- Build folders like bin/ (usually builds are created on production systems and anyone who got repository files can create bin).
- Dependency folders like node_modules/ or packages (because they are large and anyone can install those dependencies after pulling repository).
- Compiled and log files like *.pyc, *.log (compiled file for python and log files). 
- Hidden OS files like Thumbs.db or .DS_Store.
gitignore repository in github contains different templates. We create .gitignore file after initialization to avoid committing files we want to be ignored. Go to gitignore.io. To make a previously ignored file be tracked again, just change the filename in .gitignore to another filename or remove the filename of the file you want to be tracked and then you can commit the changes in the file. Ignore all temporary files with `*.tmp` and * means it matches 0 or more characters. Use `#` to add comments in .gitignore like `# ignore single file` and wildcard patterns can be used in .gitignore. Ignore a folder by adding a line like `bin/` to .gitignore and all files in the bin folder will be ignored after staging and committing .gitignore. You can add a line with the contents `new-file.txt` in .gitignore then stage and commit .gitignore and a file with the name `new-file.txt` will be ignored by git and it won't be pushed to remote. Create a .gitignore file in the git repository with `touch .gitignore` then stage it with `git add .gitignore` then commit it. Usually .gitignore is created after repository initialization. .gitignore file may be placed in any folder in your project but it is usually placed in the root of the repository. To exclude file/s and folder/s, create rules in a file called .gitignore. By default git ignore is not configured (there are no ignored files in any repository by default). If you add an ignored file in working directory, git won't tell you to stage it and commit it and git will not say repository it not in sync, git will only ignore the file. Files in git are either tracked or untracked. When creating a new file, git treats it as untracked and offers you to stage it and commit it to make it be in tracked status. If you don't want to stage and commit specific file or files, you can ignore them in git. Ignore is an additional file status. You don't need to commit system files, build files or temporary files.

### Reset
Reset is intended for private branches and not for public branches in remote like production, release, master, dev, etc.

You can commit changes again when mixed or soft reset are used. Hard reset is when changes are removed from git repository, staging area and working directory and commits are removed. Soft reset is when changes are removed in git repository but changes are still in staging area and working directory and commits are removed. Default reset is mixed reset where changes are in working directory but changes are removed in git repository and staging area and commits are removed. You can use relative refs instead of hash. Revert is one of two primary ways to reverse changes in Git (the other is Revert). Revert to a previous commit with the possibility of choosing whether you want to keep or discard the changes in the working directory. Git Reset is when you checkout a particular commit with `git checkout` and then you want to delete everything that comes after it. When using mixed reset, the file will turn a different color which means there are changes in the file and green lines will appear which means those are the additional or new changes or modifications and they are unstaged. These changes came from the commits that have been reset. You can keep those changes, modify the changes then stage and commit or remove those changes entirely. It can be used with relative refs like in `git reset HEAD~1` wherein main is the current branch and it will be moved to its parent. Reset like `git reset HEAD~1` works great for local branches on your own machine but its method of rewriting doesn't work for remote branches that others are using so to reverse changes and share those reversed changes with others, use Revert like `git revert HEAD`.
- `git reset --soft <hash>` - Soft Reset - Moves to specified commit in history but keeps changes staged in a working directory (staged changes are those added to Git tracking with `git add .` and before they are untracked and then they become tracked).
- `git reset <hash>` - Mixed Reset - It is the default. Put the hash of the commit to move to that specified commit in history, unstage the changes and keeps them in the working directory but they won't be staged. All changes made after the specified commit will be in your working directory but not staged. You can manually stage them with `git add .`
- `git reset --hard <hash>` - Hard Reset - It moves to the specified commit in history and discards all changes in the working directory and staging area. All those changes made after the selected commit will be discarded entirely and no trace will be left.

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

Use `git stash pop` to get the previous changes stored in stash and changes will be applied and stash file will be deleted in git repository. Just use `git stash` to save uncommitted changes in a branch even if only one is a staged file and the other file is just modified and the changes will be removed but they are stored for later on (git creates a temporary commit and stores it in git repository). Stashing allows you to save uncommitted work. If you are working on a specific feature branch like temp branch and you have created some files, modified some files and you have staged some changes but not yet committed them and if at this moment of time you want to check out other feature branch like temp2 branch but you want to keep changes made in temp branch, that is where stashing comes in. After coming back to temp branch, you can retrieve changes from stash continue work on them. After using the command, it will be saved and you can work right away on what you want to focus on that is different then do the usual add, commit and push as fix to a bug then get the code back with `git stash apply <name>`. Use `git stash list` to see the names like `git stash apply stash@{0}`. If the previous bug fix is in the same line, a merge conflict will appear and you need to manually choose which to keep and remove the lines around what we want to keep then you can continue working on your feature. It will save your uncommitted changes, both staged and unstaged without committing them (use on code you don't want to lose). This is used when you are in the middle of working on a feature and it is not complete yet and is also not ready to commit yet but you want to keep your active changes somewhere and work on it later so you can work on an urgent bug fixing or a different more important task.

#### Pop Stashed Changes
```bash
git stash pop
```
Get the previous changes stored in stash then apply those changes and then the stash file will be deleted in the Git repository.

### Revert
```bash
git revert <hash>
```
Revert the changes made by one specific commit when changes were already pushed to remote by creating a new commit that inverses the changes made by the specified commit. (`git revert HEAD`). Can be used on public branches in remote like master, release, dev, production, etc. When the commit specified is not the last commit, conflicts might appear that should be resolved to continue revert operation. Works on only one commit. History of commits won't be changed.

Use :wq to accept default commit message. `git revert --continue` is used after resolving conflicts with staging the changes and `git revert --abort` is used to cancel revert operation. When git revert is used on 4th commit before last commit with `git revert <hash>` where hash is 4th commit before last commit, there will be an error because of conflicts and git status will show that there are unmerged paths and conflicts should be resolved first and after that continue revert operation so go to vscode and find conflicts in the file. Git revert is really useful when you have already pushed changes to remote repository in specific public branch and some other people have already pulled those changes so if you want to revert changes, you don't have any other option except git revert and git revert is a safe operation and it doesn't modify history but it adds additional commit. With git revert, you only revert only a single commit but with git reset you are able to reset multiple commits. History won't be adjusted and after using git revert, it can be push the change to remote repository but git revert is a safe operation and if you want to apply changes to public branch, you can. Put commit hash in hash and head can be used instead as in `git revert HEAD` to revert last commit and create a new commit that inverses changes in last commit and git will offer you to edit commit message in terminal just write :wq then enter to accept default message because git opens message in vim editor. Git revert operation reverts specific commit, just a specific commit, and you need hash of that commit and git revert will take the specific commit and then inverse all changes that were made in that commit and create a brand new commit. Git revert is opposite of reset since it is not a destructive operation and it doesn't modify git history and that is why it can be safely used on any public branches like master branch, release branch or dev branch. You can use relative refs instead of hash. One of the primary ways to reverse changes in Git (the other is Reset). If you've deployed a feature that broke `production` branch and you want to undo its effects without losing the commit history. You want the logs to be there but you want to revert to an old commit. It is ideal when you have nothing to hide and you want to maintain a clear record of changes that you did and it is like the opposite of `git reset`. A mini merge conflict will appear and it is trying to figure out what we want to keep and what we want to remove. Remove all lines that you don't need. Save and add those changes to staging with `git add .` then use `git revert --continue` to succesfully finalize the revert. A message will say that we will revert the commit, we just need to provide a commit message. We can exit that window with `:qa!` then enter. A new commit will be added. Both reset and revert have use cases (whether you want to hide your tracks or you want to show everybody that you messed up and you fixed it later on.

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

We won't be able to see when branches were made and merged and which commits were made in a specific branch after using rebasing. Merging doesn't change commits but rebasing change commits and it create new commits. Rebasing also can make it seem like commits were made before the other commits because of a differnt timestamp. Rebase the current branch which can be feature branch onto the branch which can be master branch as in `git rebase master` in order to copy commits in current branch and put it in a linear fashion after the last commit in master branch (old commits in current branch will be deleted). After using rebase command, checkout the base branch which can be master and then merge the feature branch into main branch by using `git merge <branch>` where branch is the feature branch we want to merge into master and then you can delete the feature branch that was merged into master by using `git branch -d <branch>` as in `git branch -d feature1` then push changes to remote with `git push`. With `git rebase main`, if bugFix branch is the current branch, the work in bugFix will be copied and put as latest work in main branch. Take a set of commits, copy them and put them somewhere else. It can make a nice linear sequence of commits for a cleaner commit log if it is allowed. Use `git rebase bugFix` when main is current branch so main will just point to the copied commit from bugFix and that copied commit is where bugFix now points too also.

#### Rebasing Branches
- Rewrites history.
- History becomes linear.
- Doesn't keep entire history of all commits.

#### Steps in Rebasing (Rebasing is a two step process [part 1 and 2 is step 1 and part 3 and 4 is step 2])
Merge feature branch (feature1 branch) into base branch (master branch) using rebasing:
1. Checkout feature branch by using `git checkout <branch>` as in `git checkout feature1`.
2. Rebase feature branch on top of the base branch by using `git rebase <branch>` as in `git rebase master` (brand new commits will have the last commit of base or master branch as parent to form linearly and those brand new commits are just copies of old commits created by git).
3. Checkout base branch with `git checkout <branch>` as in `git checkout master`.
4. Merge feature branch into the base branch with `git merge <branch>` as in `git merge feature1` and fast forward merge will be used.
5. Old commits from feature branch (feature1) will be garbage collected because there are no pointers there and the feature branch pointer now points to the brand new commits.
Rebasing of branches - There will be no new merge commit with rebasing. With rebasing, history is linear and every commit got only one parent and information about feature branches actually lost unlike merging that keeps entire history of all commits. Rebasing is alternative way to merge two different branches or more together. There are advantages and disadvantages of this process. Advantage is rebasing keeps history linear. With merging, there are commits with multiple parents but with rebasing every commit has just a single parent if you of course only rebase branches and don't merge them and there are no commits that have multiple parents and that means that history becomes linear. Drawbacks of rebasing: rebasing rewrites history and that means that it doesn't keep the entire history of all commits and some commits actually are lost during rebasing and you won't be able to travel in history to find commits that were made in specific branches that were rebased and so on.
You need to merge release or master branch into your current feature local branch in order to keep it up-to-date with already published features. In such case, you could use rebasing but never use rebasing on public branches like master or release because rebasing is a destructive operation and it changes history but locally on your private branches, you could use it. Rebasing is a two step process. First step is rebasing of the feature branch on top of the master or release branch that is public branch and then merging of feature branch into master or release branch and then fast forward merge will be done and no new merge commits will be created. Rebasing creates branch new commits and commits that were created in a branch that was rebased will be automatically deleted by git. Use rebasing with care.

#### Rebasing with Squashing
In many public, especially large repositories with many collaborators, many pull requests, many feature branches, rebasing with squashing technique is applied when merging specific pull request or specific branch into main branch, release or master branch. After merging of specific feature branch into dev branch, instead of 3 commits, only 1 commit was added. Repository don't have many merge commits because those guys don't perform 3 way merging, they use rebasing with squashing. Every feature collapses into 1 single commit and is then added to main dev branch. Useful for keeping history line of public branches pretty clean. There are not many commits with many parents. There are not much merge commits. There are 3 choices that will appear in github. The usual create a merge commit, squash and merge and rebase and merge. Choose the 2nd one to make 3 commits into 1 commit. 2nd one is rebasing with squashing. The 1st one is just going to create a merge commit while the 3rd one is just going to do rebasing but no squashing.

#### Interactive Rebase
`git rebase -i HEAD~4` - Can be used to get and copy only one commit if that commit contains a bug fix while the rest of commits contains debug and console.log or print to track down the bug. If main is the current branch, create a new copy of whichever commits will be selected among commits up to 4 above the current commit. Commits can be selected or not selected to be included. Order of copied commits that were selected can be changed. It is using rebase with `-i` option. Git will open a UI to show you which commits are about to be copied below the target of rebase. It also shows the hash and commit message. In real Git, UI is opening a file in a text editor like vim. In real Git interactive rebase, you can do squashing (combining) commits, amending commit messages and even editing commits themselves.

#### Interactive Rebasing with Squashing
`git rebase -i <hash>`
Use the command while in the feature branch where the commits to be squashed are. The master branch points to the 4th commit so use the hash of 4th commitl. A prompt will appear that contains all commit message of the 3 commits. Change the word pick to squash or just type s. Press i to insert. Git wlll create new single commit that will be based on those 3 commits. Type :wq then enter. If you are happy with commit message, type :wq again then enter. Rebasing will happen. It is now 1 commit instead of 3 commits. 1 commit incorporated all changes from previous 3 commits. It is now safe to merge feature branch to main master branch. Checkout master with `git checkout master`. Merge feature to master branch as in `git merge -v feature2`. Fast forward merge will be performed because rebasing was just performed. Same operation was performed locally on computer just like in github. As argument in rebase command, hash of commit that was last commit before creation of specific feature branch is to be passed. Rebasing with squashing with terminal is a bit more complex than one button click in github. Interactive rebasing must be used. It is rebasing with -i option. If you want to squash 3 commits then get the hash of 4th commit that will not be squashed and use the hash in the command.

### Reflog
Reflog can be used in:
1. `git log` - Select an old commit that is not the last commit.
2. `git reset --hard <hash>` - Use the selected old commit.
3. `git log` - Check commits history.
4. `git reflog` - You will see the operation in the output of reflog.
5. `git reset --hard <hash>` - Use the commit previously show by reflog with HEAD@{1} counter to make repository go back to its previous state.
Show the entire history of all operations made in repository. Use `git reflog show <branch>` to see operations done in a branch. Only changes made in local repository can be seen in reflog. Instead of hash, you can use the references from the output of reflog (`git checkout HEAD@{6}`). perations in reflog are stored for only 90 days by default.

`git reflog` - Use `git lg` then select an old commit hash like from 5 weeks ago and then `git reset --hard <hash>` to make head point to commit made 5 weeks ago then check with `git lg` then you will see that operation in `git reflog` and if you are not happy with reset operation and you want to get back to the state before git reset, you can perform another git reset but by using the 2nd hash of `git reflog` output (the one with HEAD@{1}) so copy the hash and use `git reset --hard <hash>` and the hash is the 2nd commit hash and you will see changes back again. `git reflog` doesn't show operations made in remote repository or on other computers or collaborators. Operations in reflog are stored for 90 days by default so you can't go back to a previous state in repository that are older than 90 days. You can use HEAD@{0} instead of hash and you can change the number 0 to other numbers because they are references to the commit hash as in `git checkout HEAD@{6}`. By using the info from the `git reflog` output, you can go into detached head state by copying the commit hash and then using `git checkout <hash>`. You will see hash, references like head and dev branch and something like HEAD@{0}. This is counter for a specific reference. You see references of head by default with `git reflog`. You can use it for to see which operations were made in that branch with `git reflog show <branch>` as in `git reflog show temp`. You can use it with any branch. A useful command that will show the entire history of all operations made in repository. This will output only changes made in your computer (on your local repository). Using the result of this command, you can revert back to the state that was in repository before performing reset operation. Let's assume you have resetted to five commits back and then you want revert this operation and get five commits back again. It is possible with reflog command.

### Cherry Pick
`git cherry-pick <hash>` - Insert a commit. This is not destructive. It simply allows you to apply any other changes fast and easy. Hash can be hash of commit that is in another branch and it will be added to current branch and new commit will be added. --no-commit can be added as in `git cherry-pick --no-commit <hash>` in order to get changes and stage them but not commit them so that you can add your own commit message with `git commit -m <description>`. `git cherry-pick <hash> <hash> <...>` is used to get multiple commits. Cherry pick allows you to take any commit and insert it into currently checked out branch as a last commit and use cherry pick operation in several scenarios. For example, you are working on a separate feature branch and have made several commits there and want to take just one commit of that feature branch and insert it into for example master branch or release branch like a bugfix or something else and you can do that with cherry pick operation. Another scenario for example you hae moved to detached head state and moved 1 or 2 commits there but you don't want to create a new feature branch and afterwards merge it into release or master branch. You just want to take 1 or both commits from detached head state and afterwards insert them into master or release branch. You can do this also using cherry pick operation. Can be used to get and copy only one commit if that commit contains a bug fix and the other commits only contains debug and console.log or print to track down the bug. It is best when you know which commits you want and you know their hashes, if you don't know which commits you want, use interactive rebasing. It is the best way to review a series of commits you're about to rebase. If main is current branch, `git cherry-pick <hash> <hash>` can copy a commit from a branch and copy another commit from another branch to main branch. Copy a series of commits below your current location (HEAD) or current branch. Commits can be picked from another branch and those commits don't need to be connected one after another in the commit history.

### Amend
`git commit --amend -m "<description>"` - Modify last commit and create a brand new commit while old one is removed. Amend option for git commit command is useful when you have occasionally made some typo or mistake in the very last commit. With amend option you can adjust information in the last commit. Git will create a brand new commit and previous one will be garbage collected that is why amend is destructive operation. Destructive operations should be done with caution only on private branches, not in public branches like dev, release or master. Use amend option to adjust last commit. Author can be changed with `git commit --amend --author="Ray Ferringson <rayferringson@gmail.com>"`and then there will be a prompt to modify commit message in the new commit and message is taken from the previous commit. If you are happy with the message, enter :wq. Amend command can't be used in older commits, it can only be used on the last commit.

### Run Garbage Collection
`git gc`
Garbage collection runs automatically from time to time to clean the repository. It can be manually started.

## Misc

### Staging Environment
- Multiple people may have merging rights.
- Different feature branches are merged into release branch.
- Merging is performed frequently.
- Primarily used for testing.
- Usually for internal use.
Staging environment can be any name but release branch is common.
Before going to production, each feature goes first to staging. When any dev has finished work on a specific branch, he may request a review from other devs if they are happy with that, devs who have rights may merge into staging and after that dedicated people may test the feature. This happens in a closed staging environment and customers don't see those new features before they are applied to production. Used internally and is not facing any customers. Some companies open this staging environment for selected customers and they ask them to review some changes to get feedback and improve corresponding feature. Merging is need to start testing process on staging. The same devs that may have rights to merge into staging will not be able to merge corresponding changes to production. When any of the features is ready, corresponding dev opens pull request and target branch in this case will be release branch.

### Production Environment
- Can have any name but master branch is common.
- For stable production service.
- For customers.
- Merging happens every 2 weeks or 1 month.
- Usually only release branch is merged into master branch.
- Only few people have merge rights.
Specific tests are set up for every merge and before merge into release or master, you may run different tests and you can set them up in github. Production service must always be up and running so it is critical to merge only features that were properly tested. Only release branch can be merged into production but hotfixes may go directly into production (create a separate branch and merge directly to master branch but it is not recommended to merge anything without proper testing on staging). Features in production may only be implemented after careful proper testing (test before release is merged into production). That is why merging can be once a month or less. Small or mid-sized projects may be relased more often like each week or every several days but it is common practice to plan releases to production and move according to plan like merge once a month or every 2 weeks.

### Git Development Workflow
Public branches are like master, release or dev and are usually set as protected branches and only owners can merge pull requests or other branches into those branches. There are times where you are still developing your own feature while other features are being merged into public branch and you then want to be up to date with other changes or features. So you need to merge public branches into your current feature branch you are currently working on. We have commits that can't be pushed to remote becuase of having no permissions. So we need to reset those new commits to go back to the previous state to be the same as remote repository. Github desktop don't have the feature to reset to specific commit. Only revert is possible. So reset with `git lg` then get the commit to where remote is pointing to then use `git reset --hard <hash>`. We merge public branch to feature branch since public branch may have new changes applied to it. Merging public branch to feature branch will create new merge commit so to avoid that, rebasing can be used. We just want to update feature branch.

### CI/CD
In the modern world, each software is developed  usually according to CI/CD principles. CI means continuous integration and CD means continuous development. It means software is being developed continuously. There are two environments: staging environment and production environment. There is also staging version and production version of specific software. Set the two branches are protected branches to avoid automatic merging into those branches (good practice). Those branches shouldn't be deleted by anyone in the team.
