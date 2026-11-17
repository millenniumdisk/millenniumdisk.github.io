# Git Experiments

## Starting Point
The user name should match the one listed in the computer being used. `millenniumdisk` is just an example user name.

To avoid confusion, we will use a familiar location in Windows OS to try Git.

Find the `Desktop` folder in file explorer.
Remember the path in the file explorer.
Open terminal (`Git Bash`).
Go to `Desktop` folder by entering `cd C:/Users/millenniumdisk/Desktop`.
Create a folder with the name `testing_area` with `mkdir testing_area`.
Go to the folder with `cd testing_area`.

When terminal is started, we need `cd C:/Users/millenniumdisk/Desktop/testing_area` to go to the starting folder.

Delete the files and folders inside the `testing_area` folder when trying different commands.

## Show Current Directory
Use `pwd` command a lot.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
pwd
```
## Show Files And Directories
Use `ls` command a lot.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch style.css
ls
ls -l
ls -a
ls -l -a
ls -la
mkdir hospital
cd patient.txt
cd ..
ls -la hospital
```
## Change Directory
### Go To Root Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
cd
pwd
```
### Go To A Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir backups
cd backups
```
### Go Back One Level
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir products
cd products
cd ..
```
### Go Back One Level And Go To A Different Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir f1 f2
cd f1
cd ../f2
pwd
```
### Use An Absolute Address
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
```
### Use A Relative Address
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir logos
cd logos
```
### Go To A Nested Folder
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir pictures
cd pictures
mkdir nature
cd ..
cd pictures/nature
```
## Create Files
### Create A File
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch index.html
```
### Create Multiple Files
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch doc1.txt doc2.txt
```
## Create Directories
### Create A Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir python_folder
```
### Create Multiple Directories
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir projects assignments
```
## Delete Files Or Directories
### Delete A File
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch program1.py
rm program1.py
```
### Delete A Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir images
rm images
```
### Delete Multiple Directories
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir chemistry biology
rm chemistry biology
```
### Delete A Non-empty Directory
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir arduino
cd arduino
touch instructions.txt
cd ..
rm -rf arduino
```
### Delete Multiple Non-empty Directories
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir math english
cd math
touch algebra.txt
cd ..
cd english
touch presentation.txt
cd ..
rm -rf math english
```
## Show File Contents
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "Apple" > fruit.txt
cat fruit.txt
echo "Orange" > fruit.txt
cat fruit.txt
```
## Create Or Edit A File With An Editor
### Create A File With An Editor
Creates a file if it doesn't exist.

Create a file and edit it.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
nano recursion.c
```
### Edit A File With An Editor
Edits a file if it already exists.

Open file and edit it.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "Cook an italian carbonara" > reminder.txt
nano reminder.txt
```
## Use String To Print, Overwrite Or Append
### Print A String
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "It is raining today"
```
### Create Or Overwrite A File
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "It is time to read a book about programming" > todos.txt
```
### Create Or Append To A File
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "Lettuce" >> vegetable.txt
cat vegetable.txt
echo "Cabbage" >> vegetable.txt
cat vegetable.txt
```
## Copy A File
Creates a new file. If file exists, its contents will be overwritten.

Create `orange.txt` with contents from `apple.txt`.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "this is apple street" > apple.txt
cp apple.txt orange.txt
cat orange.txt
```
## Move Or Rename Files And Folders
### Rename A File
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
echo "What is 46 * 98?" > quiz.txt
cat quiz.txt
mv quiz.txt exam.txt
ls -la
cat exam.txt
```
### Rename A Directory
If directory in the second argument doesn't exist, a rename will happen.

Rename folder.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir videos
mv videos movies
ls -la
```
### Move A File
Move a file to a folder.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch grocery.txt
mkdir docs
mv grocery.txt docs
cd docs
ls -la
```
### Move A Directory
If second directory exists, first directory will be moved.

Move `f1` folder to `f2` folder.

If there is another `f1` folder inside `f2` and we use `mv f1 f2`, move won't happen if `f1` inside `f2` is not empty.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir f1 f2
mv f1 f2
ls -la
```
### Move Multiple Files
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch tuna.txt sardines.txt
mkdir box
mv tuna.txt sardines.txt box
cd box
ls -la
```
### Move And Rename File
Move and then rename file after moving.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
touch cookie.txt
mkdir container
mv cookie.txt container/chocolate.txt
```
## Find Files
### Find A File
Find a specific file with a filename.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir animals
touch monkey.txt lion.txt tiger.txt
cd ..
find animals -name lion.txt
```
### Find All Files
`*` in `find hiking -name *.txt` is a wildcard.

Find all files that have the `.txt` file extension.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir hiking
touch essentials.txt schedule.txt random_number_generator.py
cd ..
find hiking -name *.txt
```
### Find Regular Files
`f` in `find codes -type f` means file.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
mkdir codes
touch index.html project.txt
cd ..
find codes -type f
```
## Clear Terminal
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
pwd
clear
```
## Help
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
man ls
```
Use `--help` to get help if `man` is not working.
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
cd --help
```
## Exit terminal
```bash
cd C:/Users/millenniumdisk/Desktop/testing_area
exit
```