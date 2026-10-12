---
layout: post
title: Bash Commands
---

# Bash Commands
1. `pwd` - Show current directory.
2. `ls` - Show files and folders (options: `-l` to list and `-a` to show hidden files and folders).
3. `clear` - Clear terminal.
4. `cd` - Go to root directory (use `cd <path>` to go to a specific directory).
5. `touch <filename>` - Create a file.
6. `mkdir <folder_name>` - Create a directory.
7. `rm <filename / folder_name>` - Remove a file / remove an empty directory.
8. `rm -rf <folder_name>` - Remove a non-empty directory.
9. `cd <relative_address>` - Go to a nested folder with relative address (ex. `cd learning_resources/python_folder`).
10. `cd <absolute_address>` - Go to a directory with an absolute address (ex. `cd C:/Desktop`).
11. `cd ..` - Go back one level.
12. `echo "<string>"` - Print a string.
13. `nano <filename>` - Edit a file.
14. `echo "<string>" > <filename>` -  Write to a file. Use `>` to make the output of echo be used to write to a file. When the file already exists, it will be overwritten.
15. `echo "<string>" >> <filename>` - Append string to a file.
16. `cat <filename>` - Show file contents.
17. `cp <source> <destination>` - Copy file.
18. `mv <source> <destination>` - Move file.
19. Find Files
20. `touch <first_filename> <second_filename>` - Create multiple files.
21. `man <command>` - Show help. Use `<command> --help` as alternative (ex. `man clear` or `touch --help`).
22. `exit` - Exit terminal.

- Current Directory - `.` is the symbol used for current directory.
- Parent Directory - `..` is the symbol used for parent directory.
- Relative Address - Shorter address that can be used relative to the current directory.
- Absolute Address - Complete address that can be used regardless of the current directory.
- Hidden Files or Folders - Hidden files or folders start with `.` in their name.
- Previous Commands with Up or Down Arrow Key - Commands previously used can be easily accessed with up or down arrow keys.
- Autocomplete - Pressing the `tab` key will autocomplete an unfinished command. Pressing `tab` twice will show choices.
- Open Folder in File Explorer - Using `start .` or `open .` (for macOS) will open the current folder in the file explorer. `start <filename>` or `open <filename>` (for macOS) will open the file.