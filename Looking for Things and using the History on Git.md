# Looking for Things and using the History on Git: Examples and Reference

## **List commits that changed a file** :
The last argument is the path to a file or a glob pattern (file paths with wildcards).

Example: list all commits that changed files whose name includes `"some-file"`, in any directory.
```powershell
git log --all --full-history -- *some-file*
```
---
## **List commits with commit message matching text** :
Example: list all commits whose commit message contains text `"some text"`
```powershell
 git log --grep="some text"
```
