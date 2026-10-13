---
layout: post
title: bash basics part 1
---

# Bash Basics Part 1
## Bash Commands
1. Show Current Directory - `pwd`
2. Show Files / Directories - `ls`
3. Show Files / Directories as List - `ls -l`
4. Show Hidden Files / Directories - `ls -a`
5. Show All Files / Directories as List - `ls -l -a`
6. Show All Files / Directories as List V2 - `ls -la`
7. Go to a Specific Directory - `cd <path>` (path can be an absolute or relative address)
8. Go to Root Directory - `cd`
9. Go Back One Level - `cd ..`
10. Create a File - `touch <filename>`
11. Create Multiple Files - `touch <filename1> <filename2>`
12. Create a Directory - `mkdir <directory>`
13. Create Multiple Directories - `mkdir <directory1> <directory2>`
14. Remove a File / Empty Directory - `rm <filename / directory>`
15. Remove Multiple Files - `rm <filename1> <filename2>`
16. Remove Multiple Empty Directories - `rm <directory1> <directory2>`
17. Remove Multiple Non-empty Directories `rm -rf <directory1> <directory2>`
18. Show File Contents - `cat <filename>`
19. Edit a File - `nano <filename>`
20. Print a String - `echo "<string>"`
21. Create or Overwrite File - `echo "<string>" > <filename>`
22. Create or Append to a File - `echo "<string>" >> <filename>`
23. Copy a File - `cp <source> <destination>`
24. Move a File - `mv <source> <destination>`
25. Find a File - `find <path> <options> <expression>` (there are a lot more ways to use `find`)
    1.  Find a Specific File - `find <path> -name <filename>`
    2.  Find all Files with Wildcard - `find <path> -name *.<file_extension_name>`
26. Clear Terminal - `clear`
27. Show Help - `man <command>` / `<command> --help`
28. Exit Terminal - `exit`

## Terminal Concepts
- `.` is the symbol used for current directory.
- `..` is the symbol used for parent directory.
- `Relative address` is the location of the file or folder which is short and must be used relative to the current directory.
- `Absolute address` is the location of the file or folder which is complete and can be used regardless of the current directory.
- `Hidden` files or folders start with `.` in their name.
- Using `start .` / `open .` (macOS) will open the current folder in the file explorer.
- `start <filename>` / `open <filename>` (macOS) will open the file.
- Pressing the `tab` key will autocomplete an unfinished command.
- Pressing `tab` twice will show possible command choices.
- Previously used commands can be navigated with up or down arrow keys.
- `Bourne Again Shell` (Bash) was released in June 8, 1989 and was written in C.
