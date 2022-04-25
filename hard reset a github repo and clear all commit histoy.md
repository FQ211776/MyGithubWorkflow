# Make the current commit the only (initial) commit in a Git repository

**Description :**   Deleting the .git folder may cause problems in your git repository. If you want to delete all your commit history but keep the code in its current state, it is very safe to do it as in the following:

**Example** :

```powershell
# Check current branches to replace
git branch

# a new branch without history keeping current states of old files in main<master> branch
# This will create a new branch with one commit that adds everything in HEAD. It doesn't alter anything else, so it's completely safe
git branch new_branch_name $(echo "commit message" | git commit-tree HEAD^{tree})

# Checkout
git checkout new_branch_name

# Delete old branches
git branch -D master

# Rename the current branch to master or the name you prefer
git branch -m dominus

# Finally, force update your repository
git push -f origin dominus
```


**this will not keep your old commit history around**


**[based on a mix of answers in stackoverflow](https://stackoverflow.com/questions/9683279/make-the-current-commit-the-only-initial-commit-in-a-git-repository)**
