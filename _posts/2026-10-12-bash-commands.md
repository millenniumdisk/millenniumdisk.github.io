---
layout: post
title: Bash Commands
---
# Bash Commands

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
1. Show Current Directory - `pwd`
2. Show Files and Folders - `ls` (options: `-l` to list and `-a` to show hidden files and folders)
3. Clear Terminal - `clear`
4. Go to Root Directory - `cd`
5. Go to a Specific Directory - `cd <path>`
6. Create a File - `touch <filename>`
7. Create a Directory - `mkdir <folder_name>`
8. Remove a File / Empty Directory - `rm <filename / folder_name>`
9. Remove a Non-empty Directory - `rm -rf <folder_name>`
10. Remove Multiple Files / Folder
    1.  `rm <file1> <file2>`
    2.  `rm <directory1> <directory2>` (use rm -rf if both got files inside them)
11. Go to a Nested Folder with a Relative Address - `cd <relative_address>` (ex. `cd learning_resources/python_folder`)
12. Go to a Directory with an Absolute Address - `cd <absolute_address>` (ex. `cd C:/Desktop`)
13. Go Back One Level - `cd ..`
14. Print a String - `echo "<string>"`
15. Edit a File - `nano <filename>`
16. Write to a File - `echo "<string>" > <filename>` (when the file already exists, it will be overwritten)
17. Append to a File. `echo "<string>" >> <filename>`
18. Show File Contents - `cat <filename>`
19. Copy a File - `cp <source> <destination>`
20. Move a File - `mv <source> <destination>`
21. Find a File - `find <path> <options> <expression>` (there are more than two ways to use find command so definitely look it up online)
    1.  Find a Specific File - `find <path> -name <filename>` (ex. `find backup_folder -name picture1.jpg`)
    2.  Find all Files with Wildcard - `find <path> -name *.<file_extension>` (ex. Get all files that end with `.jpg` file extension with `find backup_folder -name *.jpg`)
22. Create Multiple Files - `touch <first_filename> <second_filename>`
23. Show Help - `man <command>` / `<command> --help` (ex. `man clear` / `touch --help`)
24. Exit Terminal - `exit`