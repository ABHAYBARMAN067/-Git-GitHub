# Git & GitHub Cheat Sheet (Basic → Advanced)

---

## 🔹 BASIC SETUP

```bash
git --version                    # Checks the installed version of Git
git config --global user.name "Your Name"  # Sets your global username for commits
git config --global user.email "you@email.com"  # Sets your global email for commits
git config --list                # Lists all current Git configuration settings
```

---

## 🔹 REPOSITORY

```bash
git init                         # Initializes a new Git repository in the current directory
git clone <repo-url>             # Downloads a repository from a remote URL and creates a local copy
```

---

## 🔹 STATUS & ADD

```bash
git status                       # Shows the current state of the working directory and staging area
git add file.txt                 # Stages a specific file for the next commit
git add .                        # Stages all changes in the current directory for the next commit
git rm file.txt                  # Removes a file from the working directory and stages the removal
```

---

## 🔹 COMMIT

```bash
git commit -m "message"          # Creates a commit with the staged changes and a message
git commit -am "add & commit"    # Adds all tracked files and commits them in one step
```

---

## 🔹 LOG / HISTORY

```bash
git log                          # Shows the commit history in detail
git log --oneline                # Shows a condensed commit history (one line per commit)
git log --graph                  # Displays commit history with a graphical branch structure
```

---

## 🔹 REMOTE (GitHub)

```bash
git remote add origin <url>      # Adds a remote repository (e.g., on GitHub) as "origin"
git remote -v                    # Lists all configured remote repositories with their URLs
```

---

## 🔹 PUSH / PULL

```bash
git push origin main             # Uploads local commits to the "main" branch on the remote "origin"
git pull origin main             # Downloads and merges changes from the remote "main" branch into the local branch
```

First Push:

```bash
git branch -M main               # Renames the current branch to "main"
git push -u origin main          # Pushes to "main" and sets it as the upstream branch for future pushes
```

---

## 🔹 BRANCHING

```bash
git branch                       # Lists all local branches
git branch feature               # Creates a new branch named "feature"
git checkout feature             # Switches to the "feature" branch
git checkout -b new-branch       # Creates and switches to a new branch named "new-branch"
git branch -d feature            # Deletes the "feature" branch (only if merged)
```

---

## 🔹 MERGE

```bash
git merge feature                # Merges the "feature" branch into the current branch
```

---

## 🔹 STASH

```bash
git stash                        # Temporarily saves uncommitted changes and reverts the working directory
git stash list                   # Lists all stashed changes
git stash apply                  # Applies the most recent stash without removing it
git stash pop                    # Applies and removes the most recent stash
git stash clear                  # Deletes all stashes
```

---

## 🔹 RESET

```bash
git reset --soft HEAD~1          # Undoes the last commit but keeps changes staged
git reset --mixed HEAD~1         # Undoes the last commit and unstages changes (default behavior)
git reset --hard HEAD~1          # Undoes the last commit and discards all changes
```

---

## 🔹 REVERT (Safe)

```bash
git revert <commit-id>           # Creates a new commit that undoes the changes from a specific commit
```

---

## 🔹 DIFF

```bash
git diff                         # Shows differences between working directory and staging area
git diff HEAD                    # Shows differences between working directory and the last commit
git show <commit-id>             # Displays details of a specific commit, including changes
```

---

## 🔹 TAGS

```bash
git tag                          # Lists all tags
git tag v1.0                     # Creates a lightweight tag named "v1.0" at the current commit
git push origin v1.0             # Pushes the "v1.0" tag to the remote repository
git tag -d v1.0                  # Deletes the local "v1.0" tag
```

---

## 🔹 REBASE (Advanced)

```bash
git rebase main                  # Reapplies commits from the current branch onto "main" (linear history)
git rebase -i HEAD~3             # Interactively rebases the last 3 commits (allows editing)
```

---

## 🔹 CHERRY PICK

```bash
git cherry-pick <commit-id>      # Applies changes from a specific commit to the current branch
```

---

## 🔹 CLEAN

```bash
git clean -f                     # Removes untracked files from the working directory
git clean -fd                    # Removes untracked files and directories
```

---

## 🔹 RESTORE

```bash
git restore file.txt             # Discards changes to "file.txt" in the working directory
git restore --staged file.txt    # Unstages "file.txt" without changing the working directory
```

---

## 🔹 ADDITIONAL USEFUL COMMANDS

```bash
git fetch origin                 # Download changes from remote without merging
git pull --rebase origin main    # Pull and rebase instead of merge
git reflog                       # Show history of HEAD movements
git blame file.txt               # Show who last modified each line
git bisect start                 # Start binary search for bugs
git submodule add <url>          # Add a submodule
```

---

##  MOST IMPORTANT COMMANDS

```bash
git clone
git pull
git push
git add .
git commit -m
git branch
git merge
git stash
git reset
git revert
```

---

## TIP

Git = Local Version Control  
GitHub = Online Repository

---

Perfect for **beginners, interviews & real projects**