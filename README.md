# Git Commands

_A list of commonly used Git commands_


### Git Identity Setup

| Command | Description |
| ------- | ----------- |
| `git config --global user.name "[your name]"` | Configure the author name |
| `git config --global user.email [username]@[example].com` | Configure the author email address to be used with your commits |
| `git config --list` | List config settings |

### Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone https://github.com/[username]/[repository-name].git` | Create a local copy of a remote repository using HTTPS |
| `git clone git@github.com:[username]/[repository-name].git` | Create a local copy of a remote repository using SSH |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branchName]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git stash` | Stash uncommited changes in a dirty working directory |
| `git stash list` | Lists all the stored stash previously |
| `git stash apply stash@{[stash number]}` | Apply the stash changes in your current working directory |
| `git stash clear` | Remove all stashed entries |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |

### Managing Remotes

| Command | Description |
| ------- | ----------- |
| `git fetch [remote]` | Fetches updates of all the branches from a remote repository |
| `git fetch [remote][branch name]` | Only fetches updates of the specified branch |
| `git fetch --all` | Fetches updates of all the registered remotes and their branches |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository (`git pull` does a `git fetch` followed by a `git merge`) |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push origin [branch name] -f` | Force push a branch to your remote repository (DANGEROUS, not recommended) |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git remote add origin git@github.com:[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin git@github.com:[username]/[repository-name].git` | Set a repository's origin branch to SSH |
| `git remote -v` | List all the current remotes |
| `git remote rm [remote-name]` | Remove a remote URL from your repository |
| `git remote rename [current-name] [new-name]` | Rename an existing remote |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git diff` | Preview uncommited changes before merging |
| `git diff [sourcebranch]..[targetbranch]` | Preview diff from source branch to target branch |
| `git log` | View commit history |
| `git log --pretty=oneline` | View commit history with just one line summary of each commit |
| `git log -p [filename]` | View the commited changes in commit history of file |
| `gitk --follow [filename]` | View the changes history in Git repository browser |

### Manage commits & Commit history

| Command | Description |
| ------- | ----------- |
| `git reset --soft HEAD~1` | Undo last one commit. It resets HEAD to previous commit. |
| `git reset --mixed HEAD~1` | In addition to `soft` option, It will reset the index to match it. |
| `git reset --hard HEAD~1` | In addition to `mixed` option, <br />It resets the working copy to match it as well (DANGEROUS, not recommended) |
| `git rebase --i HEAD~[number-of-commits]` | To squash commits, <br />replace `pick` with `s` for the commits you want to squash |
| `git rebase --i HEAD~[number-of-commits]` | To rename commits, <br />replace `pick` with `r` for the commits you want to rename |
| `git rebase --abort` | It resets the rebase and gets you back to where you started |
| `git cherry-pick master` | Apply the changes added by the commit at the tip of the <br />master branch and create a new commit with this change. |

### Versioning & Release

| Command | Description |
| ------- | ----------- |
| `git tag` | List the available tags |
| `git tag -l *[sub-string]*` | Refine the list of tags, pass `-l` option with a wild card expression |
| `git tag [tag name]` | Create a new tag |
| `git tag -d [tag name]` | Delete a tag |
| `git push [remote] [tag name]` | Push tag to remote |
| `git push [remote] --tags` | Push all the tags to remote (not recommended) |

