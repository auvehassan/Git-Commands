Here’s a comprehensive list of all **Git branch-related commands** with explanations:

### **Basic Branch Commands**
1. **List all branches**  
   ```bash
   git branch
   ```
   - Shows a list of local branches, highlighting the current branch.

2. **List all branches (local & remote)**  
   ```bash
   git branch -a
   ```
   - Displays all local and remote branches.

3. **List only remote branches**  
   ```bash
   git branch -r
   ```
   - Shows only remote branches.

4. **Create a new branch**  
   ```bash
   git branch <branch-name>
   ```
   - Creates a new branch but does not switch to it.

5. **Switch to an existing branch**  
   ```bash
   git checkout <branch-name>
   ```
   - Moves to the specified branch.

6. **Create and switch to a new branch** (modern approach)  
   ```bash
   git checkout -b <branch-name>
   ```
   OR  
   ```bash
   git switch -c <branch-name>
   ```
   - Creates a new branch and switches to it.

### **Branch Management**
7. **Rename the current branch**  
   ```bash
   git branch -m <new-branch-name>
   ```
   - Renames the current branch.

8. **Rename another branch**  
   ```bash
   git branch -m <old-name> <new-name>
   ```
   - Renames a specified branch.

9. **Delete a local branch**  
   ```bash
   git branch -d <branch-name>
   ```
   - Deletes a branch (only if merged).

10. **Force delete a local branch**  
    ```bash
    git branch -D <branch-name>
    ```
    - Deletes a branch, even if it has unmerged changes.

11. **Delete a remote branch**  
    ```bash
    git push origin --delete <branch-name>
    ```
    OR  
    ```bash
    git push origin :<branch-name>
    ```
    - Removes the specified branch from the remote repository.

12. **See the last commit on each branch**  
    ```bash
    git branch -v
    ```
    - Displays the last commit for each branch.

13. **See branches already merged into the current branch**  
    ```bash
    git branch --merged
    ```

14. **See branches not yet merged into the current branch**  
    ```bash
    git branch --no-merged
    ```

### **Tracking & Remote Branches**
15. **Set up tracking for a branch**  
    ```bash
    git branch --set-upstream-to=origin/<remote-branch> <local-branch>
    ```
    - Links the local branch to the remote branch.

16. **Check the upstream branch**  
    ```bash
    git branch -vv
    ```
    - Shows which remote branch each local branch is tracking.

### **Merging & Rebasing**
17. **Merge another branch into the current branch**  
    ```bash
    git merge <branch-name>
    ```
    - Merges changes from the specified branch.

18. **Rebase the current branch onto another**  
    ```bash
    git rebase <branch-name>
    ```
    - Moves the base of the current branch onto the specified branch.

### **Advanced Branch Operations**
19. **Show a branch’s starting point**  
    ```bash
    git merge-base <branch1> <branch2>
    ```
    - Shows the common ancestor commit.

20. **Compare branches**  
    ```bash
    git diff <branch1>..<branch2>
    ```
    - Shows differences between two branches.

21. **Find out which branches contain a commit**  
    ```bash
    git branch --contains <commit-hash>
    ```
    - Lists branches that contain a specific commit.

22. **Create a new branch based on a specific commit**  
    ```bash
    git branch <new-branch-name> <commit-hash>
    ```
    - Creates a branch from a specific commit.

23. **Prune deleted remote branches locally**  
    ```bash
    git remote prune origin
    ```
    - Removes remote branches that no longer exist.

24. **Fetch remote branches without checking them out**  
    ```bash
    git fetch --all
    ```

25. **Pull remote branches**  
    ```bash
    git pull origin <branch-name>
    ```
    - Fetches and merges updates from a remote branch.

### **Branch Cleanup**
26. **Delete all merged branches except `main` or `master`**  
    ```bash
    git branch --merged | grep -v "main" | xargs git branch -d
    ```
    - Deletes all merged branches except `main`.

This covers almost all Git branch commands! Let me know if you need more details. 🚀
