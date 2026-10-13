---
layout: post
title: Bash Commands
---
# Bash Part 1: Commands List

## Introduction
Some things to know first:
1. Current Directory - `.` is the symbol used for current directory.
2. Parent Directory - `..` is the symbol used for parent directory.
3. Relative Address - The location of the file or folder which is short and must be used relative to the current directory.
4. Absolute Address - The location of the file or folder which is complete that can be used regardless of the current directory.
5. Hidden Files or Folders - Hidden files or folders start with `.` in their name.
6. Up / Down Keys - Commands previously used can be easily accessed with up or down arrow keys.
7. Autocomplete - Pressing the `tab` key will autocomplete an unfinished command. Pressing `tab` twice will show possible choices.
8. Open Folder in File Explorer - Using `start .` or `open .` (for macOS) will open the current folder in the file explorer. `start <filename>` or `open <filename>` (for macOS) will open the file.

## Bash Commands List

### Basics
1. Print a String - `echo "<string>"`
2. Clear Terminal - `clear`
3. Exit Terminal - `exit`

### Navigation
1. Go to Root Directory - `cd`
2. Go to a Specific Directory - `cd <path>`
3. Go Back One Level - `cd ..`
4. Go to a Nested Folder with a Relative Address - `cd <relative_address>` (ex. `cd learning_resources/python_folder`)
5. Go to a Directory with an Absolute Address - `cd <absolute_address>` (ex. `cd C:/Desktop`)

### Inspect
1. Show Current Directory - `pwd`
2. Show Files and Folders - `ls` (options: `-l` to list and `-a` to show hidden files and folders)
3.  Show File Contents - `cat <filename>`
4.  Find a File - `find <path> <options> <expression>` (there are more than two ways to use find command so definitely look it up online)
    1.  Find a Specific File - `find <path> -name <filename>` (ex. `find backup_folder -name picture1.jpg`)
    2.  Find all Files with Wildcard - `find <path> -name *.<file_extension>` (ex. Get all files that end with `.jpg` file extension with `find backup_folder -name *.jpg`)
5.  Show Help - `man <command>` / `<command> --help` (ex. `man clear` / `touch --help`)

### File Creation
1. Create a File - `touch <filename>`
2. Create a Directory - `mkdir <folder_name>`
3. Create Multiple Files - `touch <first_filename> <second_filename>`

### File Editing
1. Edit a File - `nano <filename>`
2. Create or Write to a File - `echo "<string>" > <filename>` (when the file already exists, it will be overwritten)
3. Create or Append to a File. `echo "<string>" >> <filename>`

### File Deletion
1. Remove a File / Empty Directory - `rm <filename / folder_name>`
2. . Remove a Non-empty Directory - `rm -rf <folder_name>`
3.  Remove Multiple Files / Folder
    1.  `rm <file1> <file2>`
    2.  `rm <directory1> <directory2>` (use rm -rf if both got files inside them)

### File Organization
1. Copy a File - `cp <source> <destination>`
2. Move a File - `mv <source> <destination>`
