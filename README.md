# Git-Commands
A popular version control system used for  Tracking code changes ,  Tracking who made changes , Coding collaboration.


### Configuration
Git is a powerful version control system that allows you to configure various settings using the `git config` command. Here are some common `git config` commands:

1. **Set User Information**:
   - `git config --global user.name "Your Name"`: Sets your name for commits.
   - `git config --global user.email "your@email.com"`: Sets your email for commits.
   - `git config --global user.signingkey "Your GPG Key ID"`: Sets your GPG key for signing commits.

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



### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
