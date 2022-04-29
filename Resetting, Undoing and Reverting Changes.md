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

## **Undo commit** :
No files in the working directory will be changed.

The repository will be pointing to the previous commit.
```powershell
git reset --soft HEAD~1
```
---
## **Unstage changes** :
I.e. un-add all added files:
```powershell
git reset --soft HEAD
```
---
## **Add changes to commit** :
ust `add` new files and then run `git commit --amend`

To add file `file1.txt` to the previous commit:
```powershell
git add file1.txt
git commit --amend
```
This will open up the previous commit message in case you want to edit it or keep the same message.
---
## **Undo git add** :
This is the same as unstaging changes in a file.

To undo adding a file to a commit (but keep it tracked) use
```powershell
git reset HEAD path/to/file.txt
```
---
## **Change commit message** :
git commit --amend will open a text editor for you to change the last commit message
```powershell
git commit --amend
```

---
## **Revert file to previous commit** :
This is what you should do to reset one single file to the way it was in the previous commit:e
```powershell
git reset HEAD~1 -- path/to/file
```
Then you can re-add/re-commit it again into the repo's history.


https://queirozf.com/entries/git-examples-resetting-undoing-and-reverting-changes
