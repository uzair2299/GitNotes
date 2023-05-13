# Branches
## Listing
| Command  | Operation |
| ------------- | ------------- |
| `git branch` |  Lists all the local branches in the repository. The current branch is indicated with an asterisk. |
| `git branch -r` |  Lists all remote-tracking branches. In Git, the -r flag for the git branch command stands for "remote" |
| `git branch -a` |  Lists all local and remote branches. In Git, the -a flag for the git branch command stands for "all" |
| `git branch -v` |  Lists all local branches along with their last commit message. In Git, the -v flag for the git branch command stands for "verbose" |
| `git branch --merged` |  Lists all branches that have been merged into the current branch. |
| `git branch --no-merged` |  Lists all branches that have not been merged into the current branch. |


## Create New Branch
| Command  | Operation |
| ------------- | ------------- |
| `git branch <branchname>` |  Creates a new branch with the specified name based on the current branch. |


## Switching Branch
| Command  | Operation |
| ------------- | ------------- |
| `git checkout <branchname>` |  Switches to the existing specified branch and updates the working directory to reflect the files in that branch.|


## Create & Switch Branch
| Command  | Operation |
| ------------- | ------------- |
| `git checkout -b <branchname>` |  Creates a new branch with the specified name and switches to it in one command.|

## Push Branch To The Remote
| Command  | Operation |
| ------------- | ------------- |
| `git push <remote> <local-branch-name>:<remote-branch-name>` | `<remote>` is the name of the remote repository you want to push.This is typically `origin`. </br> `<local-branch-name>` is the name of the local branch you want to push. </br> `<remote-branch-name>` is the name of the branch you want to create or update on the remote repository. If you omit this, Git will use the same name as the local branch.|


## Merging


| Command  | Operation |
| ------------- | ------------- |
| `git merge <branch-to-merge>` |This will merge the changes from `<branch-to-merge>` into your current branch. If there are any conflicts between the changes on the two branches, Git will pause the merge process and ask you to resolve the conflicts before proceeding.|

## Delete Branch

| Command  | Operation |
| ------------- | ------------- |
| `git branch -d localBranchName` | This command deletes a local branch.The -d option will delete the branch only if it has already been pushed and merged with the remote branch. Use -D instead if you want to force the branch to be deleted, even if it hasn't been pushed or merged yet. |
| `git push origin --delete remoteBranchName` | This command deletes a remote branch |


 



##  Conflict Markers

```
<<<<<<< HEAD 
Code from current branch
=======
Code from other branch
>>>>>>> other-branch
```
The `<<<<<<< HEAD` marker indicates the start of the conflict resolution block. The code between this marker and the `=======` marker is from your current branch, and the code between the `=======` marker and the `>>>>>>>` marker is from the other branch.

To resolve the conflict, you need to manually edit the code to decide which changes to keep and which to discard. Once you have resolved the conflict, you can remove the conflict markers and commit the changes.
  

