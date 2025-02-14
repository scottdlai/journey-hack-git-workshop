# What is this?

Sample respository for Git Work in Journey Hack 2025.

# Commands

### Setting up

```sh
# Only need to do one time when first setup
git config --global user.name "<kimi-no-na-wa>"
git config --global user.email "<your-email>"

# Nice to have
# Rebase instead of merge when pulling
git config --global pull.rebase true
# Autostash untracked changes when rebasing
git config --global rebase.autostash true
# New respository branch name is main
git config --global init.defaultbranch main
# Usage: git uncommit <commit-hash>
git config --global alias.uncommit "!f() { git reset --soft ${1:-HEAD~}; }; f"
# Usage: git unstage <path>
git config --global alias.unstage "reset HEAD"
git config --global alias.lol "log --graph --pretty=format:'%C(yellow bold)%h%C(reset)%C(auto)%d%C(reset) - %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'"
```

### Cloning a Repository

```sh
git clone <url>

# Cloning a repo into path
git clone <url> <path>
```

### Setting up existing project into a Repository locally

```sh
# Create a new repository on github

# In the root of your project
git init

git add .
git commit --message "setup: initial commit"
git remote add origin "<url>"
git push -u origin main
```

### Status

```sh
# To see current status of local workspace
git status
```

### Staging / Unstaging

```sh
git add <path-to-file>

# To add all of the edited files
git add .

# To unstage a file in the index
git reset HEAD <path>
```

### Commit

```sh
# See commit history
git log

# After staging the files you want to include in a commit
git commit --message "<commit-message>"

# To edit last commit message
git commit --amend --message "<new-commit-message>"

# To include new staged files in last commit
git commit --amend --no-edit
```

### Push

```sh
git push

# First time pushing to a branch
git push -u origin <branch-name>
```

### Pull

```sh
git pull

# To rebase
git pull --rebase
```

### Branching

```sh
# Create and switch to a new branch
git switch -c <branch-name>

# Switch to an existing branch
git switch <branch-name>

# Merge another branch to current branch
git merge <other-branch-name>

# Rebase another branch to current branch
git rebase <other-branch-name>
```
