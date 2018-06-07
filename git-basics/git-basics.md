# Git
Git is a version control system which allows us to
manage our source code history with a strong focus on collaborative and distributed development.

## Installation
To work with git we have to download and install it. Git can be downloaded from https://git-scm.com/.
To determine whether git was successfully installed type
```console
C:\git-basics> git --version
git version 2.13.0.windows.1
```
into your terminal. In case of a successful installation git will return its version.

## Initializing Git
In order track our source code history we have to tell git that it should track the folder containing our project. Let's begin by creating a new project folder named ```project```:
```console
C:\git-basics> mkdir project
```
We can tell git to track this folder by changing into the directory and using the ```git init``` command.
```console
C:\git-basics> cd project
C:\git-basics\project> git init
Initialized empty Git repository in C:/git-basics/project/.git/
```

## Committing Files
Let's beginn by creating a new file ```hello-git.txt``` in our project folder and adding the following lines to it:
```
Hello World!
```
Using the ```git status``` command will reveal that we created a
new file ```hello-git.txt``` that is untracked. This means that this file is currently not under version control.
```console
C:\git-basics\project> git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        hello-git.txt

nothing added to commit but untracked files present (use "git add" to track)
```
Committing new or modified files into a git repository is a two-step process:
1. Using the ```git add```command to tell git which of the new or modified files we want to commit. Files that are marked for a commit are also referred to as *staged files*
1. Using the ```git commit``` command to actual commit the files

Now we can tell git to stage our new file by using the ```git add``` command.
```console
C:\git-basics\project> git add hello-git.txt
```
An alternative to specifying the exact file is to stage all new and modified files by using the period.
```console
C:\git-basics\project> git add .
```
Using the ```git status``` command again will reveal that git is tracking our new file and that this file is now staged for the next commit.
```console
C:\git-basics\project> git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   hello-git.txt
```
Finally we can use the ```git commit``` command to commit our currently staged files.
```console
C:\git-basics\project>git commit -m "Initial commit."
[master (root-commit) a5e5a0a] Initial commit.
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt
```
After the file has been sucessfully committed the ```git status``` command once again reveals that we have no more changes to be committed.
```console
C:\git-basics\project>git status
On branch master
nothing to commit, working tree clean
```