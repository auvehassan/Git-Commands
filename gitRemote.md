# Git-Remote
Managing remote repositories in Git involves a set of commands that allow you to add, view, and remove connections to other repositories.

- Manage the set of remotes that you are tracking with your local repository.
  ```
  git remote
  ```
- Lists the URLs of the remote connections you have to other repositories.
  ```
  git remote -v
  ```
- Adds a new remote Git repository.
  ```
  git remote add <name> <url>
  ```
- Removes a remote.
  ```
  git remote remove <name>
  ```
  or
  ```
  git remote rm <name>
  ```
- Renames a remote.
  ```
  git remote rename <old-name> <new-name>
  ```
- Changes the URL associated with the remote.
  ```
  git remote set-url <name> <new-url>
  ```
- Fetches branches and their respective commits from the remote repository.
  ```
  git fetch <remote>
  ```
- Fetches the specified remote’s copy of the current branch and immediately merges it into the local copy.
  ```
  git pull <remote> <branch>
  ```
- Pushes the branch to the remote, along with necessary commits and objects. Creates named branch in the remote repository if it doesn’t exist.
  ```
  git push <remote> <branch>
  ```
- Setting the Remote HEAD to a Specific Branch:
  ```
  git remote set-head <remote-name> <branch-name>
  ```
- Deleting the Remote HEAD:
  ```
  git remote set-head <remote-name> -d
  ```
