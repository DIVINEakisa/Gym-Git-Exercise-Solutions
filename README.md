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
PS C:\Users\USER\OneDrive\Documents\myProject> git branch -m master main
PS C:\Users\USER\OneDrive\Documents\myProject> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

PS C:\Users\USER\OneDrive\Documents\myProject> git branch -m main master
PS C:\Users\USER\OneDrive\Documents\myProject> git status
On branch master

No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

PS C:\Users\USER\OneDrive\Documents\myProject> git commit -a -m "First Changes"
[master (root-commit) 7666d6e] First Changes
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS C:\Users\USER\OneDrive\Documents\myProject> git remote add origin https://github.com/DIVINEakisa/Bundle1--Exercises1.git
PS C:\Users\USER\OneDrive\Documents\myProject> git remote -v
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (fetch)
origin  https://github.com/DIVINEakisa/Bundle1--Exercises1.git (push)
PS C:\Users\USER\OneDrive\Documents\myProject> git push origin master
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
 * [new branch]      master -> master
PS C:\Users\USER\OneDrive\Documents\myProject> git branch checkout -b dev
error: unknown switch `b'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-f] [--recurse-submodules] <branch-name> [<start-point>]
   or: git branch [<options>] [-l] [<pattern>...]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --[no-]verbose    show hash and subject, give twice for upstream branch
    -q, --[no-]quiet      suppress informational messages
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --[no-]set-upstream-to <upstream>
                          change the upstream info
    --[no-]unset-upstream unset the upstream info
    --[no-]color[=<when>] use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --[no-]abbrev[=<n>]   use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --[no-]delete     delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --[no-]move       move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    --[no-]omit-empty     do not output a newline after empty formatted refs
    -c, --[no-]copy       copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --[no-]list       list branch names
    --[no-]show-current   show current branch name
    --[no-]create-reflog  create the branch's reflog
    --[no-]edit-description
                          edit the description for the branch
    -f, --[no-]force      force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --[no-]column[=<style>]
                          list branches in columns
    --[no-]sort <key>     field name to sort on
    --[no-]points-at <object>
                          print only branches of the object
    -i, --[no-]ignore-case
                          sorting and filtering are case insensitive
    --[no-]recurse-submodules
                          recurse through submodules
    --[no-]format <format>
                          format to use for the output

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
