---
layout: post
title: Bash Basics Part 1
---

# Bash Basics Part 1
## Bash Commands
1. Show Current Directory - `pwd`
2. Show Files / Directories - `ls`
3. Show Files / Directories as List - `ls -l`
4. Show Hidden Files / Directories - `ls -a`
5. Show All Files / Directories as List - `ls -l -a`
6. Show All Files / Directories as List V2 - `ls -la`
7. Show All Files / Directories in Path as List - `ls -la <path>`
8. Go to a Specific Directory - `cd <path>` (path can be an absolute or relative address)
9. Go to Root Directory - `cd`
10. Go Back One Level - `cd ..`
11. Create a File - `touch <filename>`
12. Create Multiple Files - `touch <filename1> <filename2>`
13. Create a Directory - `mkdir <directory>`
14. Create Multiple Directories - `mkdir <directory1> <directory2>`
15. Remove a File / Empty Directory - `rm <filename / directory>` (deleting a file inside a directory is possible: `rm <directory>/<filename>`)
16. Remove Multiple Files - `rm <filename1> <filename2>`
17. Remove Multiple Empty Directories - `rm <directory1> <directory2>`
18. Remove Multiple Non-empty Directories `rm -rf <directory1> <directory2>`
19. Show File Contents - `cat <filename>`
20. Edit a File - `nano <filename>` (exiting right away works and then when asked to save, press `y`)
    1.  Save File in Nano Editor - `ctrl + o`
    2.  Exit Nano Editor - `ctrl + x`
21. Print a String - `echo "<string>"`
22. Create or Overwrite File - `echo "<string>" > <filename>`
23. Create or Append to a File - `echo "<string>" >> <filename>`
24. Copy a File - `cp <source> <destination>`
25. Move / Rename a File / Directory
    1.  Move File / Directory - `mv <source> <destination>`
    2.  Rename File / Directory - `mv <old_name> <new_name>`
    3.  Move Multiple Files with Wildcard - `mv *.<file_extension> <destination>`
26. Find a File - `find <path> <options> <expression>` (there are a lot more ways to use `find`)
    1.  Find a Specific File - `find <path> -name <filename>`
    2.  Find all Files with Wildcard - `find <path> -name *.<file_extension_name>`
    3. Find Regular Files - `find <directory/directory> -type f`
27. Clear Terminal - `clear`
28. Show Help - `man <command>` / `<command> --help` (`ctrl + z` to close)
29. Exit Terminal - `exit`

## Terminal Concepts
- `.` is the symbol used for current directory.
- `..` is the symbol used for parent directory.
- `Relative address` is the location of the file or folder which is short and must be used relative to the current directory.
- `Absolute address` is the location of the file or folder which is complete and can be used regardless of the current directory.
- `Hidden` files or folders start with `.` in their name.
- Using `start .` / `open .` (macOS) / `explorer .` will open the current folder in the file explorer.
- `start <filename>` / `open <filename>` (macOS) will open the file.
- Use tab key to autocomplete commands in the terminal. Press tab key twice to see choices. Can show available commands or possible directories in the incomplete command.
- Previously used commands can be navigated with up or down arrow keys.
- `Bourne Again Shell` (Bash) was released in June 8, 1989 and was written in C.
