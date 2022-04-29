# Git remote examples: Interacting with Github and other External Repos

**What is a git remote:**
A remote is a nickname for an external repository that you want to interact with.

`origin` is the name git gives to the original repository when you make a copy of (clone) it:


## **List remotes** :
`git remote`
```powershell
$ git clone git@github.com:username/my-repo.git
$ cd my-repo
my-repo$ git remote
origin
```
---
## **Show information about remote** :
`git remote show <remote_name>`
```powershell
$ git clone git@github.com:username/my-repo.git
$ cd my-repo
my-repo$ git remote show origin
* remote origin
  Fetch URL: git@github.com:username/my-repo.git
  Push  URL: git@github.com:username/my-repo.git
  HEAD branch: master
  Remote branches:
    branch_1                    tracked
    branch_2                    tracked
    master                      tracked
  Local branch configured for 'git pull':
    master merges with remote master
  Local ref configured for 'git push':
    master pushes to master (up to date)
```
---
## **Add new remote** :
TEMPLATE: `$ git remote add <remote_name> <repo_url>`

To add a new remote called origin:
```powershell
$ git remote add origin git@github.com:username/my-repo.git
$ git remote
origin
```
---
## **Delete remote** :
TEMPLATE: `$ git remote rm <remote_name>`

To delete remote called origin:
```powershell
git remote rm origin
```
---
## **Change origin of repository** :
Say you have a git repository that points to a remote repo (`origin`) and you want to change it.
```powershell
$ git remote rm origin
$ git remote add origin git@github.com:username/project.git
$ git config master.remote origin
$ git config master.merge refs/heads/master
```
---
## **Show all remotes** :

```powershell
 git remote -v
```
---
## **Fetch remote branch** :
If you have a copy of a repository that doesn't include all branches, you can fetch a branch individually:

TEMPLATE: `git fetch origin my-branch:my-branch` then `git checkout my-branch`
```powershell
$ git fetch origin branch-1:branch-1
remote: Enumerating objects: 90284, done.
remote: Counting objects: 100% (90284/90284), done.
remote: Compressing objects: 100% (26670/26670), done.
remote: Total 88353 (delta 56434), reused 84439 (delta 53035), pack-reused 0
Receiving objects: 100% (88353/88353), 16.71 MiB | 1.31 MiB/s, done.
Resolving deltas: 100% (56434/56434), completed with 1181 local objects.
From github.com:username/my-repo
 * branch            branch-1 -> FETCH_HEAD
$ git branch
* master
  branch-1
```
---
## **Delete branch locally and on remote** :
*you must use -D instead of -d of you want to force-delete an unmerged branch*

Use `git branch -d <branch_name>` to delete it locally, `git push <remote_name> --delete <branch_name>` to delete it remotely:

1) Delete the branch locally
```powershell
$ git branch -d old-branch
Deleted branch old-branch (was eeb9376)
```
2) Delete the branch on remote
```powershell
$ git push origin --delete old-branch
To git@github.com:username/my-repo.git
 - [deleted]         old-branch
```
---


## **Clone branch** :
To git clone a branch only `(my-branch)`:
```powershell
git clone -b my-branch git@github.com:my-user/repo.git repo-my-branch
```

