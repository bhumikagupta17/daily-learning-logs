# Git Version Control System Notes

## 1. Configuration & Setup
Set up your identity for all commits.
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```
## 2. Basic Commands

| Command | Description |
|----------|-------------|
| `git init` | Initialize a new repository |
| `git status` | Check the status of your working directory |
| `git add .` | Adds all changes to the Staging Area |
| `git diff` | Shows differences for files that are changed but not staged |
| `git commit -m "message"` | Records changes to the repository with a message |
| `git rm "filepath"` | Removes a file from Git tracking |
| `git log` | View commit history |
| `git log --oneline` | View a simplified, one-line commit history |
| `git show [SHA]` | Show details of a specific commit using its ID (SHA) |


 **Note:** If you created a repo on GitHub and want to link it to your local VS Code project, use: ```git remote add origin <url>```

## 3. SSH (Secure Socket Shell)

SSH is used to secure the connection between your computer and GitHub.
- Key Generation: You must generate a key pair.
- Private Key: Stays on your computer (Secret).
- Public Key: Uploaded to GitHub (Security).

## 4. Reset & Revert

- **Reset:** Moves the HEAD to a specific commit.
```git reset --hard [commit_hash]```
Effect: All commits after this point are deleted/gone.
- **Revert:** Creates a new commit that inverses the changes of a previous commit (safest for public branches).

## 5. Branching Strategy

Branches allow you to work on features in isolation.
```
git branch                     # Checks which branch you are currently in
git branch <branch-name>       # Creates a new branch (Locally only)
git checkout <branch-name>     # Switch to an existing branch
git checkout -b "branch-name"  # Create AND switch to a new branch immediately
```

### Merging & Pushing
- If you push a new branch that doesn't exist on the remote yet:
```git push --set-upstream origin <branch-name>```

### To merge a branch (e.g., merging second-branch into main):
Switch to main: ```git checkout main```
Merge: ```git merge origin/second-branch```

### Branch Naming Conventions
It is good practice to name branches based on their purpose:
- feat/add-chat → Feature (New functionality)
- wip → Work In Progress (Stuff you know won't be finished soon)
- bug → Bug Fix or Experiment
- junk → Throwaway branch

**Tip:** Use "Git Visualizing" websites to understand the tree structure better!

## 6. Advanced Concepts
**Rebase** SEQUENTIALLY places commits on top of the base branch.
```
git rebase [branch-name]
```
**Note:** Unlike merge, this rewrites history to make it linear.
**Warning:** Using this incorrectly can "pollute" or complicate history if shared with others.

### Git Stashing
Used when you have local unstaged changes but need to git pull from remote or switch branches without committing yet.
- **Save changes temporarily:**
```
git stash
```
(Moves changes to a temporary storage area)
- **Restore changes:**
```
git stash apply
```
(Brings the changes back to your working directory)
