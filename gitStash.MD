# Git-Stash
Stash the changes in a dirty working directory away.
- Temporarily saves your changes and reverts your working directory to the last commit. This is useful when you need to switch to a different branch or address an urgent issue.
  ```
  git stash
  ```
- Like push, but it cannot take pathspec 
  ```
  git stash save 'name'
  ```
- List the stash entries
  ```
  git stash list
  ```
- Show the changes recorded in the stash entry
  ```
  git stash show
  ```
- Applies the most recent stash back to your working directory. Like pop, but do not remove the state from the stash list.
  ```
  git stash apply
  ```
- Applies the most recent stash and removes it from the stash list.
  ```
  git stash pop
  ```
- Add a single stashed state to the stash list.
  ```
  git stash push
  ```
- Creates and checks out a new branch named <branchname>
  ```
  git stash branch <branchName> 
  ```
- Remove all the stash entries
  ```
  git stash clear
  ```
- Remove a single stash entry from the list of stash entries.
  ```
  git stash drop
  ```

