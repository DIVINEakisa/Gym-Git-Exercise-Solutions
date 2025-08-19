# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash/terminal
PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> cd..
PS C:\Users\USER\OneDrive\Documents> mkdir myProject


    Directory: C:\Users\USER\OneDrive\Documents


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/18/2025   6:32 PM                myProject


PS C:\Users\USER\OneDrive\Documents> cd .\myProject\
PS C:\Users\USER\OneDrive\Documents\myProject> git init
Initialized empty Git repository in C:/Users/USER/OneDrive/Documents/myProject/.git/
PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

PS C:\Users\USER\OneDrive\Documents\myProject> git branch
* master
PS C:\Users\USER\OneDrive\Documents\myProject> git branch -m  master main
PS C:\Users\USER\OneDrive\Documents\myProject> git branch
* main

PS C:\Users\USER\OneDrive\Documents\myProject> git commit -a -m "First Changes"
[master (root-commit) 7666d6e] First Changes
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\USER\OneDrive\Documents\myProject> git remote add origin https://github.com/DIVINEakisa/Bundle1--Exercises1.git
PS C:\Users\USER\OneDrive\Documents\myProject> git remote -v
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (fetch)
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (push)
PS C:\Users\USER\OneDrive\Documents\myProject> git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 396 bytes | 198.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/DIVINEakisa/Bundle1--Exercises1/pull/new/master
remote:
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
 * [new branch]      main -> main


PS C:\Users\USER\OneDrive\Documents\myProject> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\USER\OneDrive\Documents\myProject> git commit -a -m "Adding style"
[dev a62e5c1] Adding style
 1 file changed, 11 insertions(+), 2 deletions(-)
PS C:\Users\USER\OneDrive\Documents\myProject> git checkout -b test
Switched to a new branch 'test'
PS C:\Users\USER\OneDrive\Documents\myProject> git checkout dev
Switched to branch 'dev'
PS C:\Users\USER\OneDrive\Documents\myProject> git branch -d test
Deleted branch test (was a62e5c1).
```

#### Exercises 2

```bash
PS C:\Users\USER\OneDrive\Documents\Gym-Git-Exercise-Solutions> cd ..
PS C:\Users\USER\OneDrive\Documents> cd myProject
PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash
Saved working directory and index state WIP on master: a62e5c1 Adding style
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: WIP on master: a62e5c1 Adding style

PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash push -m "About File"
Saved working directory and index state On master: About File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: About File
stash@{1}: WIP on master: a62e5c1 Adding style
PS C:\Users\USER\OneDrive\Documents\myProject> git add .
PS C:\Users\USER\OneDrive\Documents\myProject> git stash push -m "Add New File"
Saved working directory and index state On master: Add New File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: Add New File
stash@{1}: On master: About File
stash@{2}: WIP on master: a62e5c1 Adding style

PS C:\Users\USER\OneDrive\Documents\myProject> git stash pop --index "stash@{1}"
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

Dropped stash@{1} (63a78fcc046f8324841d5aff5eb909a22aae68d3)
PS C:\Users\USER\OneDrive\Documents\myProject> git add home.html
PS C:\Users\USER\OneDrive\Documents\myProject> git commit -m "Index File"
[master 53a4fef] Index File
 1 file changed, 19 insertions(+)
 create mode 100644 home.html

PS C:\Users\USER\OneDrive\Documents\myProject> git push origin master
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 16 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 824 bytes | 824.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/DIVINEakisa/Bundle1--Exercises1.git
   7666d6e..53a4fef  master -> master
PS C:\Users\USER\OneDrive\Documents\myProject> git stash list
stash@{0}: On master: Add New File
PS C:\Users\USER\OneDrive\Documents\myProject> git stash pop "stash@{0}"
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

Dropped stash@{0} (7a5607f28d37ce1145bd39803c75fe2189e67eec)
PS C:\Users\USER\OneDrive\Documents\myProject> git reset --hard
HEAD is now at 53a4fef Index File
PS C:\Users\USER\OneDrive\Documents\myProject> git rm team.html

PS C:\Users\USER\OneDrive\Documents\myProject> git commit -m "Team File Removed"
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)

```
