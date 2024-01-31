# Git-Remote
'git fetch' updates your local repository with changes from the remote, but it doesn't modify your working directory or current branch. 
After fetching, you may want to use git merge or git rebase to apply these changes to your local branches.

- Fetch from the default remote (usually 'origin'): fetches branches and tags from the default remote, but it doesn't merge any changes into your current working branch.
  ```
  git fetch
  ```
- Fetch all branches from all remotes:
  ```
  git fetch --all
  ```
- Fetch all branches from a specific remote:
  ```
  git fetch <remote>
  ```
- Fetch and prune: removes any remote-tracking references that no longer exist on the remote
  ```
  git fetch --prune
  ```
  or
  ```
  git fetch -p
  ```
- Fetch a specific branch:
  ```
  git fetch <remote> <branch>
  ```
- Fetch and force update: forces an update of the local remote-tracking branches even if they conflict with the remote branches
  ```
  git fetch --force
  ```
- Fetch with more verbose output:
  ```
  git fetch --verbose
  ```
  or
  ```
  git fetch -v
  ```
- Fetch tags:
  ```
  git fetch --tags
  ```
- Dry run: doesn’t perform the fetch but shows you what it would do if run.
  ```
  git fetch --dry-run
  ```
