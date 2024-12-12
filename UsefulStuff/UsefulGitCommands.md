1. **Initialize a new Git repository**:
    ```sh
    git init
    ```

2. **Clone an existing repository**:
    ```sh
    git clone <repository_url>
    ```

3. **Check the status of your repository**:
    ```sh
    git status
    ```

4. **Add files to the staging area**:
    ```sh
    git add <file_name>
    ```

5. **Commit changes**:
    ```sh
    git commit -m "Your commit message"
    ```

6. **Push changes to a remote repository**:
    ```sh
    git push origin <branch_name>
    ```

7. **Pull changes from a remote repository**:
    ```sh
    git pull origin <branch_name>
    ```

8. **Check the commit history**:
    ```sh
    git log
    ```


1. **Create a new branch**:
    ```sh
    git branch <branch_name>
    ```
    - This command creates a new branch with the specified name but does not switch to it.

2. **Switch to a branch**:
    ```sh
    git checkout <branch_name>
    ```
    - This command switches the current working directory to the specified branch.

3. **Create and switch to a new branch**:
    ```sh
    git checkout -b <branch_name>
    ```
    - This command creates a new branch and immediately switches to it.

4. **List all branches**:
    ```sh
    git branch
    ```
    - This command lists all the branches in the repository. The current branch is highlighted with an asterisk (*).

5. **Delete a branch**:
    ```sh
    git branch -d <branch_name>
    ```
    - This command deletes the specified branch. It will not delete the branch if it has unmerged changes.

6. **Merge a branch into the current branch**:
    ```sh
    git merge <branch_name>
    ```
    - This command merges the specified branch into the current branch.

7. **Push a branch to a remote repository**:
    ```sh
    git push origin <branch_name>
    ```
    - This command pushes the specified branch to the remote repository named "origin".

8. **Pull a branch from a remote repository**:
    ```sh
    git pull origin <branch_name>
    ```
    - This command fetches and merges changes from the specified branch in the remote repository named "origin" into the current branch.



1. **Rebase the current branch onto another branch**:
    ```sh
    git rebase <branch_name>
    ```
    - This command re-applies commits from the current branch on top of the specified branch. It is useful for maintaining a linear project history.

2. **Continue a rebase after resolving conflicts**:
    ```sh
    git rebase --continue
    ```
    - After resolving conflicts during a rebase, this command continues the rebase process.

3. **Abort a rebase**:
    ```sh
    git rebase --abort
    ```
    - This command stops the rebase process and returns the branch to its state before the rebase started.

4. **Stash changes**:
    ```sh
    git stash
    ```
    - This command temporarily saves (stashes) changes in the working directory that are not yet committed, allowing you to work on something else.

5. **Apply stashed changes**:
    ```sh
    git stash apply
    ```
    - This command applies the stashed changes back to the working directory.

6. **List stashes**:
    ```sh
    git stash list
    ```
    - This command lists all stashed changes.

7. **Show changes in a stash**:
    ```sh
    git stash show -p <stash@{n}>
    ```
    - This command shows the changes in a specific stash.

8. **Delete a stash**:
    ```sh
    git stash drop <stash@{n}>
    ```
    - This command deletes a specific stash.

9. **Cherry-pick a commit**:
    ```sh
    git cherry-pick <commit_hash>
    ```
    - This command applies the changes from a specific commit to the current branch.

10. **Reset the current branch to a specific commit**:
    ```sh
    git reset --hard <commit_hash>
    ```
    - This command resets the current branch to the specified commit, discarding all changes after that commit.

11. **Revert a commit**:
    ```sh
    git revert <commit_hash>
    ```
    - This command creates a new commit that undoes the changes made by the specified commit.
