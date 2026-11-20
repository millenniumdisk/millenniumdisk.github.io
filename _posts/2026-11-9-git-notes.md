---
layout: post
title: Git Notes
---

# Git Notes

## Introduction
Git is a distributed version control system (VCS). Distributed means that team members in a project got their own repository copy in their local computers.

Git works offline and repository is stored in the local computer.

## Remote Repository Hosting Services
A remote repository hosting service can be used when many team members are working on a project (or even if it is just a personal project you are working on alone) in order do the following:
- Update the project.
- Get the latest version of the project.
- Collaborate with other team members regardless of time, location or computer being used.
- Use the remote repository as backup in the event that the local repository is lost due to the local computer malfunctioning.

Git should be installed then the computer should be connected to the internet and an account in GitHub or GitLab is needed.

## Terminal Commands
Bash will be used. Bash (Bourne Again Shell) was released in June 8, 1989 and was written in C.

In Windows 11, `Desktop` folder can be found in `C:\Users\<name>` (ex. `C:\Users\millenniumdisk`) and `/` can be used in Git Bash instead of `\`.

- `.` is the symbol used for current directory.
- `..` is the symbol used for parent directory.
- Relative address is the location of the file or folder which is short and must be used relative to the current directory.
- Absolute address is the location of the file or folder which is complete and can be used regardless of current location.
- Hidden files or folders start with a dot (`.`) in their name.
- Using `start .` / `open .` (macOS) / `explorer .` will open the current folder in the file explorer.
- `start <filename>` / `open <filename>` (macOS) will open the file.
- Use `tab` key to autocomplete commands in the terminal. Press tab key twice to see choices. Can show available commands or possible directories in the incomplete command.
- Previously used commands can be navigated with up or down arrow keys.

### `pwd` Command
`pwd` will give us information on what is the current directory. `pwd` means print working directory.
```bash
pwd
```

### `ls` Command
`ls` and its options can be used to get information about different files and folders in a directory in different ways.

Options:
- `l` - Show output in a list (ex. `ls -l`).
- `a` - Include hidden files and folders in the output (ex. `ls -a`).

Options can be used in succession (ex. `ls -l -a`) or in combined form (ex. `ls -la`).
We can specify a path to see the files and folders in that address (`ls -la <path>`).

Show the files and folders in the current directory.
```bash
ls
```

### `cd` Command
`cd` can be used to move to a different directory.

Go to the root directory.
```bash
cd
```

Go to a specific directory (path can be an absolute or relative address).
```bash
cd <path>
```

Go back one level.
```bash
cd ..
```

### `touch` Command
Create a file.
```bash
touch <filename>
```

Create multiple files by separating the next filename with a space.
```bash
touch <filename1> <filename2>
```

### `mkdir` Command
Create a directory.
```bash
mkdir <directory>
```

Create multiple directories.
```bash
mkdir <directory1> <directory2>
```

### `rm` Command
Remove a file or empty directory.
```bash
rm <filename / directory>
```

Deleting a file inside a directory is possible (ex. `rm <directory>/<filename>`).

Remove multiple files.
```bash
rm <filename1> <filename2>
```

Remove multiple empty directories.
```bash
rm <directory1> <directory2>
```

Remove a non-empty directory.
```bash
rm -rf <directory1>
```

Remove multiple non-empty directories.
```bash
rm -rf <directory1> <directory2>
```

### `cat` Command
Show file contents.
```bash
cat <filename>
```

### `nano` Command
Edit a file. Use `ctrl + o` to save file and then `ctrl + x` to exit.
```bash
nano <filename>
```

Another way to save the file is by exiting right away and then when asked to save, press `y`.

### `echo` Command
Print a string.
```bash
echo "<string>"
```

Create a file. If the file already exists, overwrite it.
```bash
echo "<string>" > <filename>
```

Create a file. If the file already exists, append to it.
```bash
echo "<string>" >> <filename>
```

### `cp` Command
Copy a file where first argument is the source and second argument is the destination. If destination doesn't exist, create it (ex. `cp apple.txt orange.txt`).
```bash
cp <source> <destination>
```

Rename a file. If destination exists, overwrite it (ex. `cp apple.txt orange.txt`).
```bash
cp <source> <destination>
```

### `mv` Command
Move file or directory. Source and destination can be a filename, directory or path of where the file or directory is.

Rename a file (`mv quiz.txt exam.txt`).
```bash
mv <old_name> <new_name>
```

Rename a directory (ex. `mv videos movies`).
```bash
mv <old_name> <new_name>
```

Move a file (ex. `mv grocery.txt docs`).
```bash
mv <source> <destination>
```

Move a directory. Move `dir1` directory to `dir2` directory (ex. `mv f1 f2`).
```bash
mv <dir1> <dir2>
```

Move multiple files (`mv tuna.txt sardines.txt box`).
```bash
mv <file1> <file2> <directory>
```

Move multiple files with wildcard.
```bash
mv *.<file_extension> <destination>
```

Move and then rename file (ex. `mv cookie.txt container/chocolate.txt`).
```bash
mv <source> <destination>
```

### `find` Command
Find a file. There are a lot more ways to use `find`.
```bash
find <path> <options> <expression>
```

Find a specific file.
```bash
find <path> -name <filename>
```

Find all files with wildcard.
```bash
find <path> -name *.<file_extension_name>
```

Find regular files. `f` means file.
```bash
find <relative directory path> -type f
```

### `clear` Command
Clear terminal.
```bash
clear
```

### `man` Command
Show help (`ctrl + z` to close). Use `<command> --help` if `man` is not working. 
```bash
man <command>
```

### `exit` Command
Exit terminal.
```bash
exit
```

## `git init` Command
Initialize a project directory as a Git repository. Creates an empty `.git` folder inside the project directory. Affects current directory.

When we say Git repository, it can mean the whole project folder or the hidden `.git` folder inside the project directory.

## `.git` Folder
There will be some folders that are empty inside the `.git` folder. `.git` folder will also have `config`, `description` and `HEAD` files. Don't modify the files in `.git` folder manually.

## `config` File
We can see contents of config file while inside `.git` folder. We will see default settings for Git configuration.
```bash
cat config
```

## `description` File
We will see description of repository.
```bash
cat description
```

## `HEAD` File
We will only see `ref: refs/heads/master` in the `HEAD` file.
```bash
cat HEAD
```

## Git Objects
There are four Git object types that Git stores in `objects` folder inside `.git`: `blob`, `tree`, `commit` and `annotated tag`.

## `objects` Folder
Git stores files independently in its `objects` folder inside `.git` folder. It is independent from your files in the file system. It is a separate database.

## Blob
Git stores any files (video, pictures or text files) with any file extension in blobs. A blob represents a single file. Used to store raw files. Blobs don't have filenames.

## Tree
Git stores information about folders with tree object type. A tree may be empty or contain files or other folders or a mix so a tree can have blobs or trees. A tree represents a folder. Filenames for blobs are in trees.

## Commit
We can store different project versions with the commit object type.

## Annotated Tag
A persistent text pointer to a specific commit.

## Management Of Blobs And Trees
We will use low level commands to manage blobs and trees.

Low level commands:
- `git hash-object`
- `git cat-file`
- `git mktree`

With `git hash-object`, we can create a new Git object.

With `git cat-file`, we can read Git objects.

With `git mktree`, we can create a new Git tree object.

## `git hash-object` Low Level Command
While inside the initialized Git repository or project folder, we will use a command.

Create a Git object inside the Git file structure. A new file will be in the `objects` folder.
```bash
`echo "Hello, Git" | git hash-object --stdin -w`
```

`--stdin` option means that `git hash-object` command will take its input from standard input and `|` means the output of the first command will be the standard input of the next command. A hash of the string will be shown in the output. `-w` will create the object.

## Hexadecimal
Hexadecimal or base 16 got 16 characters (0 to F). Base 10 format only got 10 characters (0 to 9). Binary or base 2 only got 2 characters (0 and 1).

## Generate SHA1 In Terminal
Use `man shasum` to know more about the command. `shasum` will generate hash from a string or file. The `-n` in `echo -n "Hello, Git"` won't generate newline at the end. `echo -n "Hello, Git" | shasum` will generate 40 hex characters. We need single quotes to use `!` in `echo -n 'Hello, Git!' | shasum`.

## `git cat-file` Low Level Command
`git cat-file` have many options and needs a hash.
Options:
- `p` - See the contents of the object.
- `s` - See the size of the object.
- `t` - See the type of the object.

See content of object by putting the hash or first four or more characters of the hash of the object (ex. `git cat-file -p b7aec520de`).
```bash
git cat-file -p <hash>
```

When looking for object type, we can get `blob` as output (ex. `git cat-file -t b7aec520de`)..
```bash
git cat-file -t <hash>
```

We might get `11` bytes from the object (ex. `git cat-file -s b7aec520de`)..
```bash
git cat-file -s <hash>
```

## `git hash-object` Low Level Command With A File
Create a `.txt` file first then check its contents with `cat file1.txt`. Go to the project folder with `.git` and then use `git hash-object ../file1.txt -w`.
Create a Git object inside `objects` folder inside Git repository based on a file.
```bash
git hash-object <filepath> -w
```

## Git Object Structure
A Git object got four fields: a `content`, `type`, `length` and `delimiter`. An example for each is `Hello, Git`, `blob`, `11` and `\0`. Git stores files in compressed binary format so `cat` command won't work. Hash is generated with `content` + `type` + `length`. `\0` is null character.

## Echo Option
Use `-e` option to interpret escaped characters (ex. `echo -e "blob 11\0Hello, Git"`) when `\0` can be seen in output when using `echo "blob 11\0Hello, Git"`.

## Tree Object Structure
Structure of tree is similar to blob but it got a type `tree` and it got information about `permissions`, `object type`, `hash` and `name` for each blob or tree inside it. Git will reuse the same objects and not create new objects since filenames are inside the `tree` object type.

## Permissions
Only directory and regular non-executable file permissions are common. We need permissions because root folder or project folder is a separate file system from Git repository (we can also use low level commands to create files in our project folder based on `objects` folder).

Permissions:
- `040000` - Directory permission.
- `100644` - Regular non-executable file permission.
- `100664` - Regular non-executable group-writeable file permission.
- `100755` - Regular executable file permission.
- `120000` - Symbolic link permission.
- `160000` - Gitlink permission.

## Create A Tree Object
While in the project folder with `.git` folder. `git mktree --help` will show description of command. Create `.txt` file first with the contents `100644 blob b7ae...   file1.txt` for the first line where `b7ae...` should be a complete hash and next is a tab character then filename. Second line is `100644 blob 4400...  file2.txt`.

Create tree based on a file. We will get hahs of object.
```bash
cat ../blueprint.txt | git mktree
```

## Three Areas Where Files Can Live In Git
Files in Git can live in `working directory` (project folder), `staging area` and `Git repository`.
- `Staging Area` - Prepares files from working directory to be inserted into Git repository. Staging area also prepares files taken from Git repository to be placed into the working directory. Putting files into staging area is required for all Git operations and it is between working directory and Git repository.

## `git ls-files` Low Level Command
Show all files that are in the staging area. If there is no output, it means that the staging area is empty.

Read contents of staging area. We will see filenames of files in the staging area.
```bash
git ls-files
```

Option `-s` will to make output be in table format. Permissions, hash, a digit and filename will be listed for each file. The digit can be `0` which means the files in the staging area are the same files in Git repository. It means those files were not modified.
```bash
git ls-files -s
```

## Root Tree
When nothing points to a Git tree object, it is the root tree in the Git repository or project folder.

## `git read-tree` Low Level Command
Get files from Git repository and put them in the staging area (ex. `git read-tree 3b95`). Arugment is a Git tree object.

Files from Git repository will appear in staging area.
```hash
git read-tree <hash>
```

## `git checkout-index` Low Level Command
Move files from staging area into working directory.

`-a` option, we can read all files in staging area and put them into working directory.
```bash
git checkout-index -a
```

We can use `ls` and `cat` commands to check files in working directory.

## Files In Three Areas
Same files can be in Git repository, staging area and working directory. It just means that no modification was made in the files.

## `git status` Command
Check status of Git repository. It will show current branch. We can also see changes (or added files) to be committed if we have some.

## Commit Git Object
Commit got the same structure as blob object. A commit got a `type`, `length` and `content`. Each commit got information about `author name`, `author email`, `description`, `parent` (pointer to parent commit) [optional], `hash` and `pointer to a specific tree`. Commits are used to store project versions. We can move to any project version by checking out a specific commit.

## `git config` Command
Set name and email that will be attached in commits. Can be set globally or per project. Usually set globally. The only thing that can be changed is the settings for your local computer.

Use `--global` option to set name and email globally. Don't use `--global` to set name and email per project but command must be used inside a Git repository.

Set a global name (ex. `git config --global user.name "Millennium Disk"`).
```bash
git config --global user.name "<name>"
```

Set a global email (ex. `git config --global user.email millenniumdisktte@gmail.com`).
```bash
git config --global user.email <email>
```

Read configuration of Git. `user.name` and `user.email` can be seen.
```bash
git config --list
```

## `git commit` Command With Description
There should be changes and those changes should be placed in the staging area then creating a commit is possible.

We can add description with `-m` option. We will see in what branch the commit is created. `root-commit` means it is the first commit and it doesn't have any parents. We will see its hash and description. Commit will have information about the author (who made changes), committer (who used commit command), time, time zone and description.

Create a commit in Git repository. Git will create objects if those objects are not yet in the `objects` folder.
```bash
git commit -m "<description>"
```

## `git log` Command
Show commit history.

## File Status
Files that are newly added in working directory are `untracked` files.

Tracked files are `modified`, `staged` and `unmodified`.

Untracked can change to tracked with staging.

Staged files will become unmodified with commit (we can say unmodified state is when a file is in Git repository, staging area and working directory).

Unmodified will change to modified when file is edited.

Modified files will become staged with staging.

A committed file can become untracked with untracking.

When an unmodified file became modified and it turned into staged state, it can be unstaged and will become unmodified.

An untracked that is staged can become untracked after unstaging.

## `git add` Command
Add files from working directory into staging area. New untracked files will become tracked.

Modified, newly added and deleted files will be affected by `git add`.

Stage a file from working directory (ex. `git add file1.txt`).
```bash
git add <filename>
```

Stage all files from working directory.
```bash
git add .
```

## Unstage A File
When a file is staged but not yet committed, it can be unstaged. File will be removed from staging area but it will not be removed in working directory.

Remove file from staging area (ex. `git rm --cached file1.txt`).
```bash
git rm --cached <filename>
```

## `git checkout` Command
Takes files from Git repository, puts them into staging area under the hood and then replaces the files in working directory. We can check out a commit or branch. With this command, we can go to old project versions. 

This command only moves the HEAD pointer.

We need to put the branch name to go to a branch.

Go to a branch (`ex. git checkout br1`). Only moves HEAD pointer to branch.
```bash
git checkout <branch>
```

We need to put the hash of the commit to go to a commit.

Go to a commit (`git checkout ba5e7c02ed`). Only moves HEAD pointer to commit.
```bash
git checkout <hash>
```

## Branch
A branch is just a pointer to a specific commit (a branch is like a bookmark on a commit that also automatically moves to the latest commit in it).

The default branch is `master` branch or `main` branch.

Sometimes the name of `master` is `release`.

A Git repository can have many branches.

Pointers for branches are in `.git/refs/heads` folder.

Branch names can't have spaces.

Going inside `.git` folder with `cd .git/refs/heads`, we can see one file named `master`. Using `cat master` will show the hash of a commit. It means master branch points to a commit.

## HEAD
Working directory can only be in one version of project at a time.

- HEAD is a reference to the currently checked out branch or commit (it points to current project version) so it automatically moves.
- HEAD is locally significant.
- File location is at `.git/HEAD`.
- Default pointer is `ref: refs/heads/master`.
- There is only one HEAD.

In `.git`, we can check contents of HEAD file with `cat HEAD`. We will see `ref: refs/heads/master` and when we use `cat ref: refs/heads/master`, we get hash of commit that the current branch points to.

## Deleted File State
Another file state is deleted. It is like modified state.

## `git commit` Command
`git commit` will open default editor to enter description and then a commit will be created.
```bash
git commit
```

Vim might be the default editor.
To enter insert mode press `i` key then type description.
To exit insert mode press `esc` key then type `:wq` to save file and exit (`w` is write and `q` is quit).

Using `cat .git/HEAD` will give `ref: refs/heads/master` which is the same as before.
Using `cat .git/refs/heads/master` will give a new hash because of new commit.

If we delete all files in working directory, stage and commit them, files won't be deleted in Git repository. Staging area will be empty but Git repository will keep all history.

## Detached HEAD State
Normally, HEAD points to a branch. Detached HEAD state is when HEAD points to a commit.

Checking out old commits won't show new commits in commits history.

Checking out commits instead of branch is not the preferrable way to change project version.

It is not reccommended to create new commits while in detached HEAD state. After creating a commit while in detached HEAD state and then checking out a branch, the commits created while in detached HEAD state will be lost and deleted automatically by Git and you won't be able to return to those commits.

## Why Do We Need Branches
Branches can be created when collaborating with other team members is needed. If you are working in `br1`, someone can work on a different `br2` branch at the same time.

It is possible that you are working in `br1` branch and another team member is also working on the same `br1` branch.

If master or main branch is the main project, a branch `br1` can be created so that changes in `br1` won't affect master or main branch.

We create branches so that different features can be developed at the same time.

When a feature is ready, tt will be tested and verified and then the branch with the feature can be merged to master or main or release branch.

Having multiple branches is like each having their own separate history line.

Use consistent branch names so making all branch names be descriptive is ok (ex. `refactor-main-menu`).

With branches, moving with `git checkout` is easy because we only need to remember the branch name.

## Branch Management
List all local branches. Currently checked out branch will be marked.
```bash
git branch
```

Create a new branch based on the current branch (ex. `git branch br1`). Doesn't automatically checks out the new branch. Branch should have at least one commit.
```bash
git branch <name>
```

Delete a merged branch (ex. `git branch -d br1`). 
```bash
git branch -d <name>
```

Rename a specific branch and apply immediately (ex. `git branch -m br1 DEV-1532`).
```bash
git branch -m <old_name> <new_name>
```

Force delete a non-merged branch (ex. `git branch -D br1`).
```bash
git branch -D <name>
```

If branch name doesn't exist, create a branch based on the current branch and automatically check out the new branch.
```bash
git checkout -b <name>
```

Using `ls .git/refs/heads` will show branches.
Using `cat .git/HEAD` will show `ref: refs/heads/master` which is the same as before.
After changing branches with `git checkout`, `cat .git/HEAD` will show `ref: refs/heads/temp` because a branch like `temp` is the current branch.

## Public Repository
A public repository is a Git repository that can be viewed in a repository hosting service like GitHub or GitLab and we can always get the latest updated repository since it is public.

Author and committer can be different in a public repository.

We can clone a public Git repository to our local computer and then create local commits or local branches.

If we don't have write access to the public Git repository, we can't push to it.

## `git clone` Command
We can clone our own private repository or a public repository owned by others.

We want to clone a public repository so in GitHub's website go to Developers -> Explore -> Trending repos -> Collections -> Learn to Code -> `leachim6 / hello-world` to find a Git repository with different programming languages inside it.

Click the green `Code` button. Copy the URL (`Download Zip` won't include `.git` folder so we don't want it).

The URL can be:
`https://github.com/leachim6/hello-world.git`

Go to `Desktop`.

Clone a remote repository and create new folder. A new folder will be created. Local repository will be connected to remote repository.
```bash
git clone <url>
```

## Merge Commit
If a commit is a `merge commit`, it means someone else has created a `pull request` and the author in the commit merged the pull request into a branch like master branch.

## Empty Objects Folder
In a public repository, the `objects` folder may only have `info` and `pack` folders. It is empty because the repository is optimized to save space. All Git objects are in the pack file (archived file) inside `pack` folder. The file with `.idx` inside `pack` folder is a file that contains index of Git objects. We can unpack the `.pack` file.

## `git upack-objects` Low Level Command
Unpack objects to `objects` folder. The `file` argument is the pack file. Output contents of pack file to the second command.
```bash
cat <file> | git unpack-objects
```

1. Move `.pack` file to `.git` folder (`.pack` file will disappear in `pack` folder).
2. Go to `.git` folder with `cd .git`.
3. Use `cat pack-a1a6323.pack | git unpack-objects`
4. Delete `.pack` file with `rm pack-a1a6323.pack` because we don't need it anymore (Use `rm -f pack-a1a6323.pack` to forcefully delete it if it won't work the first time).

## GitHub Desktop
`Fetch origin` button in GitHub Desktop will download all updates or latest changes in remote repository.

## Visual Studio Code
In most bottom left corner of Visual Studio Code, current branch name can be seen.

Revert changes by clicking `Discard Changes` on a file when in `Source Control: Git` in Visual Studio Code. File will return to original state.
There are file labels when using Visual Studio Code:
`M` - File is modified.
`D` - File is deleted.

## Source Control
When in Visual Studio Code, `Source Control: Git` will show old version and new version when the changed file is clicked before committing.

## Last Commit Of Remote Repository
We can see the last commit of a remote repository when there is a `origin/master` (`origin` means it is in remote repository and `master` is the remote branch name) and `origin/HEAD`.

## `git diff` Command
Use `git diff`. If there are no output, it means there are no changes.

If there are changes and changes are not yet staged and not yet committed, the command will show old and modified versions of every file that was changed.

Show sections of file `a` (old version) and file `b` (modified version).
```bash
git diff
```
The command will show `@@ -<n1>, <n2> +<n3>, <n4> @@` where `-` means old file and `+` means new file (ex. `@@ -3,6 +3,8 @@`).

Old File:
`n1` - Line number start.
`n2` - Total number of lines.
New File:
`n3` - Line number start.
`n4` - Total number of lines.

Comparison can be done with Visual Studio Code since using this command can be inconvenient.

## `git commit` Command With `-a` Option
Automatically stage `modified` and `deleted` files to staging area and commit them (ex. git `commit -a -m "Changed program1.py"` or `commit -am "Initial commit"`). Doesn't work on files that aren't `modified` or `deleted`.
```bash
git commit -a -m "<description>"
```

## Branch Merging
We can merge any branch into any other branch.

In most cases, other branches will be merged into master or main branch.

There are two ways merging is done: fast forward merge and three way merge.

To incorporate the changes made in a branch, we use merging so that the other branch will get the changes.

Merge branch into current branch (ex. `git merge br1`).
```bash
git merge <branch>
```

## Receiving Branch
It is the branch that will receive changes from another branch because of branch merging.

## Feature Branch
It is the branch that was created to develop a feature while at the same time not affecting the master or main branch when making changes.

Feature branch can be merged into a receiving branch which can be master or main branch.

## Fast Forward Merge
Git only moves the branch pointer of the receiving branch to point to the feature branch's latest commit. No new comits will be created.

Fast forward merge happens when the receiving branch have no further commits at the time when the other branch that will be incorporated to it was made.

## Try Fast Forward Merge
If we want to merge a feature branch (`br1`) into a receiving branch (master or main branch):
1. Create new feature branch from the master or main branch.
2. Check out new feature branch.
3. Make changes in the new branch and commit them (test changes first before merging).
4. Check out the receiving branch.
5. Merge feature branch into the current branch or receiving branch (if feature branch is `br1` then use `git merge br1`).
6. You can delete the feature branch if you are not going to make any changes to it by using `git branch -d <branch>` (`br1` is feature branch so use `git branch -d br1`).

We will see that the receiving branch will point to a commit with a new hash instead of the old hash after merging.

Git will automatically determine what merging technique to use (fast forward merge or three way merge).

## Ancestor Commit
Ancestor commit is a commit that is both in the feature branch and receiving branch.

## Three Way Merge
When there are new commits in the receiving branch (which can be master or main branch) and we want to merge a feature branch, three way merge will be used to avoid losing commits if fast forward merge is used.

In three way merge a new merge commit will be created. It will contain all changes. The new merge commit will be based on three commits and those commits are: the first nearest ancestor commit in receiving branch and feature branch, the latest commit in receiving branch and the latest commit of feature branch.

## Try Three Way Merge
1. Create new feature branch from the master or main branch.
2. Check out new feature branch.
3. Make changes in the new feature branch and commit them (test changes first before merging).
4. Check out master or main branch (receiving branch)
5. Make changes in the master or main branch and commit them.
6. Merge feature branch into the current branch or receiving branch (if feature branch is `br1` then use `git merge br1`).
7. You can delete the feature branch if you are not going to make any changes to it by using `git branch -d <branch>` (`br1` is feature branch so use `git branch -d br1`).

## Merge Conflict
## `git branch` Command

```bash

```

```bash

```