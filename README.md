# Git-Commands
A popular version control system used for  Tracking code changes,  Tracking who made changes, and Coding collaboration.


### Configuration
Git is a powerful version control system that allows you to configure various settings using the `git config` command. Here are some common `git config` commands:

1. **Set User Information**:
   - `git config --global user.name "Your Name"`: Sets your name for commits.
   - `git config --global user.email "your@email.com"`: Sets your email for commits.
   - `git config --global user.signingkey "Your GPG Key ID"`: Sets your GPG key for signing commits.
```
git config --global user.name "Your Name"
```
```
git config --global user.email "your@email.com"
```

2. **Set Editor**:
   - `git config --global core.editor "editor"`: Sets the default text editor for commit messages.

3. **Set Default Branch Name**:
   - `git config --global init.defaultBranch "main"`: Sets the default branch name for new repositories.

4. **View Configuration**:
   - `git config --list`: Lists all Git configuration settings.
   - `git config user.name`: Displays the user name configuration.
   - `git config user.email`: Displays the user email configuration.

5. **Aliases**:
   - `git config --global alias.st status`: Creates a Git alias. In this example, `st` is an alias for `status`.

6. **Set Merge Tool and Diff Tool**:
   - `git config --global merge.tool "mergetool"`: Sets the default merge tool.
   - `git config --global diff.tool "difftool"`: Sets the default diff tool.

7. **Set Remote Repository URL**:
   - `git remote set-url origin https://github.com/username/repo.git`: Changes the URL of the remote repository named "origin."

8. **Set Credential Helper**:
   - `git config --global credential.helper store`: Configures Git to store credentials in a file.

9. **Set Line Endings**:
   - `git config --global core.autocrlf true`: Automatically converts line endings to CRLF on Windows.

10. **Set Proxy**:
    - `git config --global http.proxy http://proxy.example.com:8080`: Sets an HTTP proxy.
    - `git config --global https.proxy https://proxy.example.com:8080`: Sets an HTTPS proxy.

11. **Set Color Settings**:
    - `git config --global color.ui auto`: Enables colored output in the command line.

12. **Set File and Directory Exclusions**:
    - `git config --global core.excludesfile ~/.gitignore_global`: Sets a global `.gitignore` file.

13. **Set Auto Correct**:
    - `git config --global help.autocorrect 1`: Enables autocorrection for typos in Git commands.

These are just a few examples of what you can configure using `git config`. You can adjust many aspects of Git's behavior to suit your workflow and preferences. Use the `--global` flag to apply settings globally, or omit it to set configuration for a specific repository.


### Stage and Snapshot
In Git, the process of staging and snapshotting your changes involves using various commands to manage your working directory, stage the changes you want to commit, and then create a snapshot (commit) of those changes. Here are some commonly used commands related to staging and snapshotting changes in Git:

1. **git status**: This command shows you the status of your working directory and which files have been modified, added, or deleted. It doesn't perform staging or commit actions but helps you understand the current state of your repository.

2. **git add**:
   - `git add <file>`: Stages a specific file for the next commit.
   - `git add .` or `git add -A`: Stages all changes in the working directory for the next commit.

3. **git reset**:
   - `git reset <file>`: Unstages a specific file, removing it from the staging area.
   - `git reset`: Unstages all changes, effectively clearing the staging area.

4. **git diff**:
   - `git diff`: Shows the difference between the working directory and the current commit (HEAD).
   - `git diff --staged`: Shows the difference between the staged changes and the last commit.

5. **git commit**:
   - `git commit`: Creates a new commit with the changes currently staged in the staging area. You'll be prompted to enter a commit message.

6. **git commit -a**: Commits all changes in the working directory without explicitly staging them first. This is a shorthand for staging all changes and committing in one step.

7. **git commit -m "Commit message"**: Commits changes with a specified commit message in a single step.

8. **git log**: Displays a log of commits in the repository, showing commit hashes, authors, dates, and commit messages.

9. **git show <commit-hash>**: Shows the details of a specific commit, including the changes introduced by that commit.

10. **git stash**:
    - `git stash`: Temporarily saves your changes and reverts your working directory to the last commit. This is useful when you need to switch to a different branch or address an urgent issue.
    - `git stash apply`: Applies the most recent stash back to your working directory.
    - `git stash pop`: Applies the most recent stash and removes it from the stash list.

11. **git branch**: Lists existing branches in the repository.

12. **git checkout**:
    - `git checkout <branch-name>`: Switches to a different branch.
    - `git checkout -b <new-branch-name>`: Creates a new branch and switches to it.

These commands help you stage, view changes, and create snapshots of your code in a Git repository, making it easy to track and manage your project's history and development.


### Branch and Merge
Branching and merging are essential concepts in Git, allowing you to work on multiple lines of development simultaneously and then combine those changes. Here's how you can create branches and merge them in Git:

### Branching:

1. **Create a New Branch:**
   - To create a new branch, use the `git branch` command followed by the name of the new branch:
     ```
     git branch new-branch
     ```

2. **Switch to the New Branch:**
   - To switch to the newly created branch, use the `git checkout` command:
     ```
     git checkout new-branch
     ```
   - A more concise way to create and switch to a new branch is to use `git checkout -b`:
     ```
     git checkout -b new-branch
     ```

3. **View Available Branches:**
   - To see a list of all branches in your repository and identify the currently checked out branch, use:
     ```
     git branch
     ```

### Making Changes:

4. **Make Changes in the New Branch:**
   - After switching to the new branch, you can make changes to your code, add, commit, and continue development independently.

### Merging:

5. **Switch Back to the Main Branch:**
   - To switch back to the main branch (or any other branch you want to merge into), use `git checkout`:
     ```
     git checkout main
     ```

6. **Merge the Branch:**
   - To merge the changes from the new branch into the main branch, use the `git merge` command:
     ```
     git merge new-branch
     ```
   - If there are no conflicts between the branches, Git will perform a "fast-forward" merge.

7. **Resolve Conflicts (if necessary):**
   - If there are conflicting changes in the branches being merged, Git will prompt you to resolve these conflicts manually. You need to edit the conflicting files, and then add and commit the resolved changes.

8. **Push the Changes:**
   - After merging and resolving conflicts (if any), push the changes to the remote repository to make them available to others:
     ```
     git push origin main
     ```

9. **Delete the Merged Branch:**
   - Once you've merged the changes, you can delete the branch you no longer need:
     ```
     git branch -d new-branch
     ```
   - Use `-d` for a safe delete that ensures the branch is fully merged, or `-D` to forcefully delete a branch that contains unmerged changes.

These steps outline the process of branching and merging in Git. Branching allows you to work on different features or fixes in isolation while merging combines those changes into the main codebase. Be cautious while merging, especially when resolving conflicts, to maintain code integrity.



### Inspect and Compare
In the context of version control systems like Git, "inspect" and "compare" refer to actions and commands related to examining and analyzing changes in your code or repository. Here's how you can inspect and compare changes in Git:

**Inspect:**

1. **View the Status of Your Repository:**
   - Use the `git status` command to inspect the status of your Git repository. It shows which files have been modified, added, or deleted.

2. **Inspect Specific Changes:**
   - Use the `git diff` command to inspect the exact differences between the working directory and the last commit (HEAD):
     ```
     git diff
     ```
   - To inspect the differences between the working directory and a specific commit, use:
     ```
     git diff <commit-hash>
     ```

3. **Inspect the Commit History:**
   - Use the `git log` command to inspect the commit history of your repository. This shows details of each commit, including commit messages, authors, dates, and commit hashes.

4. **View Specific Commit Details:**
   - Use `git show <commit-hash>` to inspect the details of a specific commit, including the changes introduced by that commit.

**Compare:**

1. **Compare Branches:**
   - To compare the differences between two branches, you can use the `git diff` command with branch names or commit hashes:
     ```
     git diff branch1..branch2
     ```

2. **Compare Commits:**
   - To compare specific commits, use `git diff` with the commit hashes:
     ```
     git diff commit1..commit2
     ```

3. **Compare with Remote Repository:**
   - To compare your local repository with a remote repository, you can use the `git fetch` command to fetch the changes from the remote repository, and then use `git diff` to compare branches or commits.

4. **Visual Diff Tools:**
   - Git also provides visual diff tools, such as `git difftool`, which allows you to use external tools for comparing changes visually.

5. **Pull Request Comparison (GitHub/GitLab/Bitbucket):**
   - If you're using a platform like GitHub, GitLab, or Bitbucket, you can compare branches or pull requests through their web interfaces, which often provide a side-by-side view of changes.

In summary, "inspecting" refers to viewing the current state, changes, and history of your repository, while "comparing" involves examining differences between branches, commits, or versions of your code. Git offers a variety of commands and tools to help you with these tasks, depending on your specific needs and preferences.

### Getting & Creating Projects
Stage the changes you want to commit, and then create a snapshot (commit) of those changes.

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
