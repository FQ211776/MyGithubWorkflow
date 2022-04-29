# Untrack files in Git

**Description :**  As far as I know, there are at least 2 ways to untrack a file using git:

## **Remove file from the repository but keep it in your working directory** :

```powershell
git rm --cached your_filename
```

## **Make git not notice changes to a file** :
This will keep the file in the repository, but it won't commit changes to it. It will stay unchanged in the repository:

```powershell
git update-index --assume-unchanged your_filename
```
to undo the previous command(tell git that you do want to keep track of changes for the file), there's the opposite command, `--no-assume-unchanged`
```powershell
$ git update-index --no-assume-unchanged your_filename
```
