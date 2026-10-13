---
layout: post
title: Introduction to Bash
---

# Introduction to Bash

## Introduction
Bourne Again Shell (Bash) was released in June 8, 1989 and is written in C.

### Autocomplete
Create two folders. Type `git-` then press tab twice to see choices. Type `git-f` then press tab to use autocomplete.
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

## Find Desktop Folder
1. Check current directory.

```bash
pwd
```

## Show Contents of Current Directory and Clear Terminal

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

## Go to Root Directory then to Desktop Folder
1. Go to desktop folder.
2. Go to root directory.
3. Go to desktop folder.

```bash
cd Desktop
cd
cd Desktop
```

## Create a New Directory as Testing Area
1. Create a direcotory.
2. Go to the directory.

```bash
mkdir bash-testing-area
cd bash-testing-area
```

## Check Current Directory
1. Check current directory.
2. Clear terminal

```bash
pwd
clear
```

## Create a File and a Directory
1. Create a file.
2. Create a directory.

```bash
touch coding-notes.txt
mkdir images
```

## Remove a File and an Empty Directory
1. Remove a file.
2. Remove an empty directory.

```bash
rm coding-notes.txt
rm images
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

## Print a String

```bash
echo "create a program that uses pointers in c language"
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

## Move a File
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

## Find a File
1. Create folder.
2. Create files.
3. Go back one level.
4. Find a file.
5. Find all text files.

```bash
mkdir data_folder
touch a.txt b.txt c.txt notes.md
cd ..
find data_folder -name b.txt
find data_folder -name *.txt
```

## Show Help

```bash
man clear
```

If `man` won't work, use `--help`.

```bash
touch --help
```

## Exit Terminal

```bash
exit
```