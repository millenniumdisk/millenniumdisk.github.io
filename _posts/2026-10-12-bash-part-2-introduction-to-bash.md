---
layout: post
title: Introduction to Bash
---

# Bash Part 2: Introduction to Bash

## Introduction
Bourne Again Shell (Bash) was released in June 8, 1989 and is written in C.

### Initial Prep
Before we start, let's check our current directory first then go to a folder. We will then create our testing area.
1. Check current directory.
2. Check files and folders in current directory.
3. Go to Desktop folder.
4. Create folder for experiments.

```bash
pwd
ls
cd Desktop
mkdir bash-exp
```

### First Steps
#### Autocomplete
Create two folders. Type `cd` first then space then type `git-` then press tab twice to see choices. Delete the command then type `cd git-f` then press tab to use autocomplete.
1. Create folder.
2. Create folder.

```bash
mkdir git-folder
mkdir git-tutorial
```

### Open Folder in File Explorer
For Windows:

```bash
start .
```

For macOS:

```bash
open .
```

### Open File
For Windows:

```bash
touch pointers.cpp
start pointers.cpp
```

For macOS:

```bash
touch recursion.cpp
open recursion.cpp
```

### Basics

#### Print a String

```bash
echo "create a program that uses pointers in c language"
```

#### Clear Terminal

```bash
clear
```

#### Exit Terminal

```bash
exit
```

### Navigation

#### Go to Root Directory
1. Go to root directory.

```bash
cd
```

#### Go to a Specific Directory
1. Go to folder.

```bash
cd Desktop
```

#### Go Back One Level
1. Go back one level.
2. Check curent directory.

```bash
cd ..
pwd
```

#### Go to a Nested Folder with Relative Address
1. Go to folder.

```bash
cd Desktop/bash-exp
```

#### Go to a Directory with Absolute Address
1. Go to root directory.
2. Go to folder.

```bash
cd
cd C:/Desktop
```

### Inspect

#### Show Current Directory
1. Show current directory.

```bash
pwd
```

#### Show Files and Folders
1. Show files and folders in different ways.
2. Clear terminal.

```bash
ls
ls -l
ls -a
ls -l -a
ls -la
clear
```

#### Show File Contents
1. Create file.
2. Show file contents.

```bash
touch index.html
cat index.html
```

#### Find a File

##### Find a Specific File
1. Create folder.
2. Create files.
3. Go back one level.
4. Find specific file in folder.

```bash
mkdir data_folder
touch a.txt b.txt c.txt notes.md
cd ..
find data_folder -name b.txt
```

##### Find all Files with Wildcard
1. Find all text files in folder.

```bash
find data_folder -name *.txt
```

#### Show Help

##### First Way
1. Show help of `clear` command.

```bash
man clear
```

##### Second Way
If `man` won't work, use `--help`.
1. Show help of `touch` command.

```bash
touch --help
```

### File / Folder Creation

#### Create a File
1. Create a file.

```bash
touch coding-notes.txt
```

#### Create a Directory
1. Create a directory.

```bash
mkdir images
```

#### Create Multiple Files
1. Create two files.

```bash
touch apple.txt orange.txt
```

#### Create Multiple Directories
1. Create two folders.

```bash
mkdir fruits vegetable
```

### File Editing
#### Edit a File

```bash
touch grocery-to-buy.txt
nano grocery-to-buy.txt
```

#### Create or Write to a File

```bash
echo "create a todo program" > challenge.txt
```

#### Create or Append to a File

```bash
echo "create a simple board game program or a hangman" >> project.txt
```

### File / Folder Deletion

#### Remove a File
1. Remove a file.

```bash
rm coding-notes.txt
```

#### Remove an Empty Directory
1. Remove an empty directory.

```bash
rm images
```

#### Remove a Non-empty Directory
1. Remove a non-empty directory.

```bash
rm -rf logos
```

#### Remove Multiple Files
1. Remove multiple files.

```bash
rm major-tests.txt quizzes.txt
```

#### Remove Multiple Empty Folders
1. Remove multiple empty folders.

```bash
rm exams attendance
```

#### Remove Multiple Non-empty Folders
1. Remove multiple non-empty folders.

```bash
rm -rf python-programs text-files
```

### File Organization

#### Copy a File

## Copy a File
1. Create two folders.
2. Go to folder.
3. Create a file.
4. Copy file to another folder.

```bash
mkdir alpha_folder beta_folder
cd alpha_folder
touch calculator.js
cp calculator.js beta_folder
```

#### Move a File
1. Create two folders.
2. Go to folder.
3. Create a file.
4. Move file to another folder.

```bash
mkdir old_folder new_folder
cd old_folder
touch style.css
mv style.css new_folder
```






## Delete a Non-empty Directory
1. Create a directory.
2. Go to the directory.
3. Create a file.
4. Go back one level.
5. Remove a non-empty directory.

```bash
mkdir website
cd website
touch index.html
cd ..
rm -rf website
```

## Remove Multiple Files / Folder
1. Create two files.
2. Create two folders.
3. Remove two files.
4. Remove two folders.

```bash
touch dummy1.txt dummy2.txt
mkdir documents scans
rm dummy1.txt dummy2.txt
rm documents scans
```

If both got files inside them, use `rm -rf`.

```bash
rm -rf documents scans
```

## Go to a Nested Folder with Relative Address
1. Create folder.
2. Go to folder.
3. Create folder.
4. Go back one level.
5. Go to a folder inside another folder.

```bash
mkdir learning_resources
cd learning_resources
mkdir python_folder
cd ..
cd learning_resources/python_folder
```

## Go to a Directory with an Absolute Address
1. Go to root directory.
2. Go to desktop folder by using an absolute address.

```bash
cd
cd C:/Desktop
```

## Go Back One Level
1. Go back one level from current directory.

```bash
cd ..
```


## Edit a File
1. Create file.
2. Open editor.

```bash
touch random_num_gen.py
nano random_num_gen.py
```

## Write to a File
1. Create or overwrite a file if it already exists with a string as its content.

```bash
echo "create a random number generator program" > plan.txt
```

## Append to a File
1. Create file and add a string to the end of the file content.

```bash
echo "we have a cold weather today" >> random.txt
```

## Show File Contents
1. Create file.
2. Show file contents.

```bash
touch fib.py
cat fib.py
```
