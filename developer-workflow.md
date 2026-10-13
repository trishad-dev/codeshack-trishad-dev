\# Developer Workflow



\## Overview



A development workflow is a sequence of steps used to make changes, test them, and maintain a clear project history using version control.



\## 1. Check the Repository Status



Before making changes, inspect the current state of the repository.



```bash

git status

```



\## 2. Create a Feature Branch



Branches allow changes to be developed separately from the main development branch.



```bash

git switch -c feature/documentation

```



\## 3. Make and Review Changes



Edit the required files and review unstaged changes.



```bash

git diff

```



\## 4. Stage Changes



Select the files to include in the next commit.



```bash

git add developer-workflow.md

```



\## 5. Commit Changes



Save the staged changes with a descriptive message.



```bash

git commit -m "Add developer workflow documentation"

```



\## 6. Synchronise with the Remote Repository



Fetch remote updates:



```bash

git fetch origin

```



Pull and integrate remote changes into the current branch:



```bash

git pull

```



Push local commits to the remote repository:



```bash

git push

```



\## 7. Review Commit History



Inspect previous commits to understand the project's development history.



```bash

git log --oneline

```



\## Conclusion



A consistent workflow helps maintain organised changes, readable commit history, and safer collaboration through branches and remote repositories.

