

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |


### Listing  Files & and Find the Diffrences b/w Files

| Command | Description |
| ------- | ----------- |
| `git show --pretty="" --name-only <sha1-commit-hash>` | Listing files using show|
| `git diff-tree --no-commit-id --name-only -r <sha1-commit-hash>` | Listing files using git diff-tree command|
| `git diff --name-only <start-commit>..<end-commit>` | To list all the changed files between two commits using diff|
| `git diff --name-status <start-commit>..<end-commit>` | To find the state of file to include the added, modified or deleted change next to each file |

### Undo Commit from Local and Remote Repository(Git Reset vs Revert vs Checkout)

| Command | SCOPE |Description
| ------- | ----------- |----------|
| `git reset` | Commit-level|Discard commits in a private branch or throw away uncommited changes|
| `git reset` |File-level| Unstage a file|
| `git checkout` |Commit-level|Switch between branches or inspect old snapshots|
| `git checkout` |File-level|	Discard changes in the working directory|
| `git revert` |Commit-level|	Undo commits in a public branch|
| `git revert` |File-level|		(N/A)|

### Git Reset Commands at commit level
#### Reset Soft: 
##### If we changed to previous commit head moved to prevoius commit but index will remains in lastet commit only.That's why chnages will be appear in staged/index araea

#### Reset Mixed: 
#####  If we changed to previous commit head moved to prevoius commit along with index.That's why changes will be appear in unstaged/working directory

#### Reset hard: 
#####  If we changed to previous commit head moved to prevoius commit but no matter of index.Changes will be deleted from working directory also.
<img src="git-reset-tree.jpg" alt="Girl in a jacket">



