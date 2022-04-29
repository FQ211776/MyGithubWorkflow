#

**Description :**

## **Clone a local repository** :
Say you have a repository under `/home/path/to/repo.git` and you want to clone it into the `project/` directory (it is created if it doesn't exist)
```powershell
git clone --local file:///home/path/to/repo.git project
```

Note that, if your project is in a directory (with a `.git` directory within), you can also use the directory name as the pointer to the repository:

```powershell
git clone --local file:///path/to/repo/directory project
```
---
## **Add a local repository as remote** :
You can also use the handle above to have your git-versioned directory track a local repository:
```powershell
cd my-project
my-project$ git remote add origin file:///home/path/to/repo.git
```
