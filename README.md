# Git-Commands
A popular version control system used for  Tracking code changes,  Tracking who made changes, and Coding collaboration.


### Configuration
Git is a powerful version control system that allows you to configure various settings using the `git config` command. Here are some common `git config` commands:

1. **Set User Information**:
   - Sets your name for commits
     ```
     git config --global user.name "Your Name"
     ```
   - Sets your email for commits.
     ```
     git config --global user.email "your@email.com"
     ```
   - Sets your GPG key for signing commits.
     ```
     git config --global user.signingkey "Your GPG Key ID"
     ```

2. **Set Editor**:
   - Sets the default text editor for commit messages.
     ```
     git config --global core.editor "editor"
     ```

3. **Set Default Branch Name**:
   - Sets the default branch name for new repositories.
     ```
     git config --global init.defaultBranch "main"
     ```

4. **View Configuration**:
   - Lists all Git configuration settings.
     ```
     git config --list
     ```
   - Displays the user name configuration.
     ```
     git config user.name
     ```
   - Displays the user email configuration.
     ```
     git config user.email
     ```

5. **Aliases**:
   - Creates a Git alias. In this example, `st` is an alias for `status`.
     ```
     git config --global alias.st status
     ```

6. **Set Merge Tool and Diff Tool**:
   - Sets the default merge tool.
     ```
     git config --global merge.tool "mergetool"
     ```
   - Sets the default diff tool.
     ```
     git config --global diff.tool "difftool"
     ```

7. **Set Remote Repository URL**:
   - Changes the URL of the remote repository named "origin."
     ```
     git remote set-url origin https://github.com/username/repo.git
     ```

8. **Set Credential Helper**:
   - Configures Git to store credentials in a file.
     ```
     git config --global credential.helper store
     ```

9. **Set Line Endings**:
   - Automatically converts line endings to CRLF on Windows.
      ```
     git config --global core.autocrlf true
     ```

10. **Set Proxy**:
    - Sets an HTTP proxy.
      ```
      git config --global http.proxy http://proxy.example.com:8080
      ```
    - Sets an HTTPS proxy.
      ```
      git config --global https.proxy https://proxy.example.com:8080
      ```

11. **Set Color Settings**:
    - Enables colored output in the command line.
      ```
      git config --global color.ui auto
      ```

12. **Set File and Directory Exclusions**:
    - Sets a global `.gitignore` file.
      ```
      git config --global core.excludesfile ~/.gitignore_global
      ```

13. **Set Auto Correct**:
    - Enables autocorrection for typos in Git commands.
      ```
      git config --global help.autocorrect 1
      ```

These are just a few examples of what you can configure using `git config`. You can adjust many aspects of Git's behavior to suit your workflow and preferences. Use the `--global` flag to apply settings globally, or omit it to set configuration for a specific repository.

### Status
The `git status` command in Git is used to display the current state of your working directory and staging area. It provides information about which files have been modified, which are staged for the next commit, and which are untracked. Here are some common `git status` commands and how to use them:

1. **Basic `git status`:**
   - To check the status of your working directory, simply run the following command:
     ```bash
     git status
     ```

   This will provide an overview of the files that have been modified, staged, or are untracked.

2. **Short Format `git status`:**
   - If you want a more concise version of the status information, you can use:
     ```bash
     git status -s
     ```

   This displays a shorter, more compact output, with two columns representing the status of each file.

3. **Ignoring Untracked Files:**
   - You can use `git status` with the `-u` or `--untracked` option to show untracked files:
     ```bash
     git status -u
     ```
     or
     ```bash
     git status --untracked
     ```

   This will list both tracked and untracked files, giving you a complete picture of the status of your working directory.

4. **Ignoring Untracked Files in Submodules:**
   - If your Git repository contains submodules, you can use the `-u` option to also show untracked files in submodules:
     ```bash
     git status -uall
     ```

   This will display the status of untracked files in submodules, as well as the main repository.

5. **Ignored Files:**
   - To include ignored files in the status output, use the `--ignored` option:
     ```bash
     git status --ignored
     ```

   This will display ignored files in addition to regular status information.

6. **Short and Porcelain Formats:**
   - You can use `git status` with `--short` and `--porcelain` options to obtain machine-readable formats for scripting and automation:
     ```bash
     git status --short
     ```
     or
     ```bash
     git status --porcelain
     ```

   These formats are designed for easier parsing by scripts and programs.

The `git status` command is a handy tool for understanding the state of your Git repository. It allows you to see which changes are ready for the next commit, which changes need to be staged, and which files are untracked. This information is vital for managing your work and ensuring that you commit the appropriate changes.

### Stage and Snapshot
In Git, the process of staging and snapshotting your changes involves using various commands to manage your working directory, stage the changes you want to commit, and then create a snapshot (commit) of those changes. Here are some commonly used commands related to staging and snapshotting changes in Git:

1. **git status**: This command shows you the status of your working directory and which files have been modified, added, or deleted. It doesn't perform staging or commit actions but helps you understand the current state of your repository.

2. **git add**:
   - Stages a specific file for the next commit.
     ```
     git add <file>
     ```
     or multiple files
     ```
     git add file1.txt file2.txt
     ```
     
   - Stages all changes in the working directory for the next commit.
     ```
     git add .
     ```
     or
     ```
     git add -A

3. **Stage All Modified and Deleted Files**:
   - If you only want to stage modified and deleted files, you can use the `-u` or `--update` option:
     ```
     git add -u
     ```
     
4. **Interactive Staging**:
   - For more fine-grained control over which changes to stage, you can use the interactive mode. This allows you to review each change and selectively stage them. Run the following command and follow the prompts:
     ```
     git add -i
     ```
     
5. **Staging Specific Lines or Hunks**:
   - You can stage specific lines or "hunks" within a file. This starts an interactive process where you can review and select changes to stage.
     ```
     git add -p
     ```

6. **Unstage Files**:
   - If you accidentally stage a file you didn't intend to, you can unstage it using:
     ```
     git reset HEAD file.txt
     ```
     
7. **git reset**:
   - Unstages a specific file, removing it from the staging area.
     ```
     git reset <file>
     ```
     
   - Unstages all changes, effectively clearing the staging area.
     ```
     git reset
     ```

8. **git diff**:
   - Shows the difference between the working directory and the current commit (HEAD).
     ```
     git diff
     ```
     
   - Shows the difference between the staged changes and the last commit.
     ```
     git diff --staged
     ```

9. **git commit**:
   - Creates a new commit with the changes currently staged in the staging area. You'll be prompted to enter a commit message.
     ```
     git commit
     ```
   - Commits all changes in the working directory without explicitly staging them first. This is a shorthand for staging all changes and committing in one step.
     ```
     git commit -a
     ```

   - Commits changes with a specified commit message in a single step.
     ```
     git commit -m "Commit message"
     ```
     
10. **git log**:
   - Displays a log of commits in the repository, showing commit hashes, authors, dates, and commit messages.
     ```
     git log

11. **git show <commit-hash>**: Shows the details of a specific commit, including the changes introduced by that commit.

12. **git stash**:
    - `git stash`: Temporarily saves your changes and reverts your working directory to the last commit. This is useful when you need to switch to a different branch or address an urgent issue.
    - `git stash apply`: Applies the most recent stash back to your working directory.
    - `git stash pop`: Applies the most recent stash and removes it from the stash list.

13. **git branch**: Lists existing branches in the repository.

14. **git checkout**:
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



