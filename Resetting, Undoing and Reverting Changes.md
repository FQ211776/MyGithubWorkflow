# Git examples: Resetting, Undoing and Reverting Changes


## ** Reset to remote ** :
Warning You will lose unsaved/uncommited work in the working directory!

Make the local working directory exaclty like the code in the remote branch (e.g. origin/master):
```powershell
git fetch origin
git reset --hard origin/master
```
---
## **Revert working directory to last commit** :
You will lose any unsaved changes!

In other words, make your working directory look exactly the same as it was after the previous commit.
```powershell
git reset --hard HEAD~1
```
---
## **Revert working directory to specific commit** :

You will lose any unsaved changes!

That will make your working directory mirror what your Repository was like after commit `<commit_hash>`

```powershell
git reset --hard <commit_hash>
```
---
## **Restore file from commit** :
Revert a file to the way it was on a given commit.

Useful for when you've modified or deleted a file by mistake.

Use `git checkout <commit_hash> -- path/to/file`

Example: Restore file.txt the way it was in this commit:
```powershell
git checkout f6f207 -- file4.txt
```
---

## **Restore file from previous commit** :

When you mistakenly delete/modify a file and commit it

Use this to revert a file to how it was in the previous commit.

Use `git checkout HEAD~1 -- path/to/file`

Example: Revert file.txt the way it was before the previous commit:

```powershell
 git checkout HEAD~1 -- file.txt
```
---


