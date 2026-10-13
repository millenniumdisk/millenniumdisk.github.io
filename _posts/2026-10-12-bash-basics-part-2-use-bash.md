---
layout: post
title: bash basics part 2
---

# Bash Basics Part 2

## Inspect
We check what our current directory is and show files and folders.

```bash
pwd
ls
ls -l
ls -a
ls -l -a
ls -la
clear
```

## Navigation
Navigate to a folder.

```bash
cd Desktop
cd 
cd Desktop
cd ..
cd Desktop
```

## Create Part 1
Create directories.

```bash
mkdir bash-experiments
cd bash-experiments
cd ..
cd ..
cd Desktop/bash-experiments
cd 
cd C:/Desktop
cd bash-experiments
mkdir fruits vegetables
mkdir recipes logos projects fonts music
cd recipes
touch pasta.txt
cd ..
cd logos
touch readme.md
cd ..
cd projects
touch calculator.py
cd ..
```

## Create Part 2
Create files.

```bash
touch apple.txt
touch cabbage.txt lettuce.txt
```

## Delete Part 1
Delete directories.

```bash
rm fruits
rm fonts music
rm -rf recipes
rm -rf logos projects
```

## Delete Part 2
Delete files.
```bash
rm apple.txt
rm cabbage.txt lettuce.txt
```

## Edit
Edit files.

```bash
echo "pineapple on pizza or not?"
echo "create a simple todo program in python" > homework.txt
cat homework.txt
echo "today is rainy" >> diary.txt
cat diary.txt
touch grocery_shopping.txt
nano grocery_shopping.txt
```

## Organize
Organize files.

```bash
mkdir old_folder new_folder alpha beta
cd old_folder
touch index.html style.css
cp index.html ../new_folder
cd ..
cp old_folder/style.css new_folder
cd alpha
touch fibo.py pointers.cpp
mv fibo.py ../beta
cd ..
mv alpha/pointers.cpp beta
```

## Find
Find files.

```bash
mkdir backup_folder
cd backup_folder
touch a.txt b.txt c.txt contacts.md
cd ..
find backup_folder -name b.txt
find backup_folder -name *.txt
```

## Help
Show help.
```bash
man touch
```

or

```bash
touch --help
```

Exit terminal.
```bash
exit
```