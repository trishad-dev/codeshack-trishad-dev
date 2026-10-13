
# Git Notes

## 1. Introduction to Git

Git is a distributed version control system used to track changes in files and manage project history. It allows developers to work on different features independently, review changes, and collaborate on software projects.

### Key Concepts

- **Repository:** A directory whose changes and history are tracked by Git.
- **Working directory:** The files currently being edited.
- **Staging area:** The area where changes are selected for the next commit.
- **Commit:** A recorded snapshot of staged changes.
- **Branch:** An independent line of development.
- **Remote repository:** A repository hosted on a platform such as GitHub.

## 2. Essential Git Commands

### 2.1 `git init`

Initialises a new Git repository in the current directory.

**Example:**
```bash
git init
```

**Explanation:** Creates the local Git repository metadata needed to track changes.

### 2.2 `git clone`

Creates a local copy of an existing remote repository.

**Example:**
```bash
git clone https://github.com/username/repository.git
```

**Explanation:** Downloads the repository and its available history into a new local directory.

### 2.3 `git status`

Displays the current branch and the state of files in the working directory and staging area.

**Example:**
```bash
git status
```

**Explanation:** Helps identify modified, staged, and untracked files before committing.

### 2.4 `git add`

Stages changes for the next commit.

**Example:**
```bash
git add README.md
```

To stage all changes in the current directory:
```bash
git add .
```

**Explanation:** Selects which changes will be included in the next commit. It does not create a commit.

### 2.5 `git commit`

Records staged changes in the repository history.

**Example:**
```bash
git commit -m "Add project documentation"
```

**Explanation:** Saves a snapshot of the staged changes with a descriptive message.

### 2.6 `git log`

Displays the commit history.

**Example:**
```bash
git log
```

For a compact history:
```bash
git log --oneline
```

**Explanation:** Shows previous commits, including their identifiers and messages.

### 2.7 `git diff`

Displays changes that have not yet been staged.

**Example:**
```bash
git diff
```

To view staged changes:
```bash
git diff --staged
```

**Explanation:** Helps review modifications before committing them.

### 2.8 `git branch`

Lists local branches.

**Example:**
```bash
git branch
```

To create a branch without switching to it:
```bash
git branch feature/documentation
```

**Explanation:** Branches allow different tasks to be developed separately.

### 2.9 `git switch`

Switches to another branch.

**Example:**
```bash
git switch master
```

To create and switch to a new branch:
```bash
git switch -c feature/documentation
```

**Explanation:** Allows development to take place on a selected branch. The `-c` option creates the branch before switching to it.

### 2.10 `git checkout`

Switches branches or restores files, depending on the options used.

**Example:**
```bash
git checkout master
```

To create and switch to a branch:
```bash
git checkout -b feature/documentation
```

**Explanation:** This is an older, widely used command. For switching branches alone, `git switch` is generally clearer.

### 2.11 `git merge`

Combines changes from one branch into the currently checked-out branch.

**Example:**
```bash
git switch master
git merge feature/documentation
```

**Explanation:** The example merges the changes from `feature/documentation` into `master`. The target branch must be checked out first.

### 2.12 `git fetch`

Downloads updates and references from a remote repository without merging those changes into the current branch.

**Example:**
```bash
git fetch origin
```

**Explanation:** Allows developers to inspect remote updates before integrating them.

### 2.13 `git pull`

Fetches remote changes and integrates them into the current branch.

**Example:**
```bash
git pull origin master
```

**Explanation:** Updates the current branch using changes from the specified remote branch. Integration may require resolving conflicts.

### 2.14 `git push`

Uploads local commits to a remote repository.

**Example:**
```bash
git push -u origin master
```

**Explanation:** Sends local commits to the remote branch. The `-u` option sets the upstream relationship, making subsequent pushes simpler.

For a feature branch:
```bash
git push -u origin feature/documentation
```

### 2.15 `git remote`

Displays or manages remote repository connections.

**Example:**
```bash
git remote -v
```

**Explanation:** Lists configured remote names and their fetch and push URLs. A remote named `origin` commonly refers to the GitHub repository.

### 2.16 `git rm`

Removes a tracked file from the repository and stages its removal.

**Example:**
```bash
git rm old-notes.md
```

**Explanation:** Stages the deletion of a tracked file for the next commit.

### 2.17 `git config`

Sets or displays Git configuration values.

**Example:**
```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

To view the configured name:
```bash
git config --global user.name
```

**Explanation:** The name and email are recorded in new commits. Use an appropriate email associated with your GitHub account if you want your commits linked to it.

## 3. Reviewing Changes Before Committing

Reviewing changes helps identify unintended modifications before they become part of the repository history.

### View Unstaged Changes

```bash
git diff
```

Displays modifications that have not been staged.

### View Staged Changes

```bash
git diff --staged
```

Displays changes already staged for the next commit.

### Check Repository Status

```bash
git status
```

Shows the current state of the working directory and staging area.

## 4. Basic Git Workflow

A typical workflow for updating a project is:

**Step 1: Check the repository status**
```bash
git status
```

**Step 2: Create a feature branch**
```bash
git switch -c feature/documentation
```

**Step 3: Make the required changes**

Edit the relevant files in the working directory.

**Step 4: Review the changes**
```bash
git diff
```

**Step 5: Stage the required files**
```bash
git add README.md
```

**Step 6: Commit the changes**
```bash
git commit -m "Improve project documentation"
```

**Step 7: Push the feature branch**
```bash
git push -u origin feature/documentation
```

**Step 8: Review the commit history**
```bash
git log --oneline
```

In a collaborative project, the feature branch can then be reviewed and merged according to the team's workflow.

## 5. Difference Between `git fetch` and `git pull`

| `git fetch` | `git pull` |
|---|---|
| Downloads updates from a remote repository. | Downloads updates and integrates them into the current branch. |
| Does not merge the downloaded changes into the current branch. | Integrates the updates, potentially requiring conflict resolution. |
| Useful for inspecting remote changes first. | Useful when ready to update the current branch. |

## 6. Conclusion

Git provides essential tools for tracking changes, maintaining project history, creating branches, and synchronising work with remote repositories. Understanding these commands helps developers manage projects systematically and collaborate effectively.
