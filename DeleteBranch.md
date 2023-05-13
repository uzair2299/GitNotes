# Branches
## Listing
| Command  | Operation |
| ------------- | ------------- |
| `git branch` |  Lists all the local branches in the repository. The current branch is indicated with an asterisk. |
| `git branch -r` |  Lists all remote-tracking branches. In Git, the -r flag for the git branch command stands for "remote" |
| `git branch -a` |  Lists all local and remote branches. In Git, the -a flag for the git branch command stands for "all" |
| `git branch -v` |  Lists all local branches along with their last commit message. In Git, the -v flag for the git branch command stands for "verbose" |


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




## Delete Branch

| Command  | Operation |
| ------------- | ------------- |
| `git branch -d localBranchName` | This command deletes a local branch.The -d option will delete the branch only if it has already been pushed and merged with the remote branch. Use -D instead if you want to force the branch to be deleted, even if it hasn't been pushed or merged yet. |
| `git push origin --delete remoteBranchName` | This command deletes a remote branch |

