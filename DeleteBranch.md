# Branches
## Listing
| Command  | Operation |
| ------------- | ------------- |
| `git branch` |  Lists all the local branches in the repository. The current branch is indicated with an asterisk. |

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

