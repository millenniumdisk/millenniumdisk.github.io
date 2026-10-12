---
layout: post
title: Introduction to Bash
---

# Introduction to Bash

Bourne Again Shell (Bash) was released in June 8, 1989 and is written in C.

## Find Desktop Folder
1. Check current directory.

```bash
pwd
```

## Show the Contents of Current Directory and Clear Terminal
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

## Create and Delete a Non-empty Directory
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





## Autocomplete
Create two folders.
1. Create folder.
2. Create folder.

```bash
mkdir git-folder
mkdir git-tutorial
```

Type `git-` then press tab twice to see choices. Type `git-f` then press tab to use autocomplete.
