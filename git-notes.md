# Git Notes



## Introduction



Git is a distributed version control system used to track changes in files and coordinate development. It helps developers maintain project history, manage branches, and collaborate efficiently.



## Essential Git Commands



### 1. `git init`



Initialises a new Git repository in the current directory.



*\*Example:\*\*

```bash

git init

```



### 2. `git clone`



Creates a local copy of an existing remote repository.



*\*Example:\*\*

```bash

git clone https://github.com/username/repository.git

```



### 3. `git status`



Displays the current branch and the state of tracked and untracked files.



*\*Example:\*\*

```bash

git status

```



### 4. `git add`



Stages file changes for the next commit.



*\*Example:\*\*

```bash

git add README.md

```



To stage all changes in the current directory:

```bash

git add .

```



### 5. `git commit`



Records staged changes as a commit in the repository history.



*\*Example:\*\*

```bash

git commit -m "Add project documentation"

```



### 6. `git log`



Displays the repository's commit history.



*\*Example:\*\*

```bash

git log --oneline

```



### 7. `git diff`



Shows changes that have not yet been staged.



*\*Example:\*\*

```bash

git diff

```



To view staged changes:

```bash

git diff --staged

```



### 8. `git push`



Uploads local commits to a remote repository.



*\*Example:\*\*

```bash

git push origin main

```



The branch name must match the branch being pushed.



### 9. `git pull`



Fetches changes from a remote repository and integrates them into the current branch.



*\*Example:\*\*

```bash

git pull origin main

```



### 10. `git fetch`



Downloads updates from a remote repository without integrating them into the current branch.



*\*Example:\*\*

```bash

git fetch origin

```



### 11. `git branch`



Lists local branches.



*\*Example:\*\*

```bash

git branch

```



To create a branch:

```bash

git branch feature/documentation

```



### 12. `git switch`



Switches to another branch.



*\*Example:\*\*

```bash

git switch feature/documentation

```



To create and switch to a new branch:

```bash

git switch -c feature/documentation

```



## Conclusion



These commands provide a foundation for managing files, maintaining project history, working with branches, and synchronising changes with remote repositories.

