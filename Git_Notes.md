# Start a Project
## Initialize New Git Repository
| Command  | Operation |
| ------------- | ------------- |
| `git init` | This is a command in Git that is used to initialize a new Git repository. It creates a new directory with a .git subdirectory that contains all the necessary files for a Git repository. |

## Cloning a Git Repository:
| Command  | Operation |
| ------------- | ------------- |
| `git clone <repository URL>` |  creates a local copy of a remote Git repository on your machine. This copy includes all of the repository's files, branches, and commit history. Where `<repository URL>` is the URL of the remote Git repository that you want to clone. |



# Tags
Git tags are a way to mark specific points in Git history as significant. They are used to label or tag specific commits with a meaningful name, often to indicate version releases or important milestones in a project. Tags are typically used to create a stable reference to a specific commit, making it easier to reference and access later.
## Create Tag
| Command  | Operation |
| ------------- | ------------- |
| `git tag <tag_name>` |  Create a lightweight tag.|
| `git tag -a <tag_name> -m "Tag message"` |  Create an annotated tag. </br> `-a`: This option stands for "annotated." When used with the git tag command, it creates an annotated tag, which includes additional metadata such as the tagger's name, email, date, and a message. </br> `-m`: This option allows you to provide a message that describes the tag. It is used to specify a message associated with the creation of the tag|

## Latter Tagging
| Command  | Operation |
| ------------- | ------------- |
| `git tag <tag_name> <commit_identifier>` |To add a tag to an older commit in Git, you need to specify the commit's identifier, such as its commit hash or a reference to the commit. Find the identifier of the commit you want to tag by using `git log`. For example, if you want to add a tag called "v1.0" to an older commit with the commit hash "abc123", you would run the following command: `git tag v1.0 abc123`|

 ## List Tag
| Command  | Operation |
| ------------- | ------------- |
| `git tag` |  The `git tag` command without any additional options will list the tags that exist locally in your Git repository. It will display the names of all the tags that have been created in your local repository.|
| `git ls-remote --tags <remote_name>` |  This command will show the tags available in the specified remote repository.|
|`git ls-remote --tags <remote_name> <branch_name>`|List remote tags for a specific branch. `git ls-remote --tags origin main` This will show the tags that are associated with the "main" branch in the "origin" remote repository.|


## Show Tag information
| Command  | Operation |
| ------------- | ------------- |
| `git show <tag_name >` | Show detailed information about a specific tag |

## Pushing Tag To The Remote
| Command  | Operation |
| ------------- | ------------- |
| `git push origin <tag_name>` | Push tag to a remote repository |
| `git push origin --tags` | Push all tag to a remote repository |

## Delete Tag
| Command  | Operation |
| ------------- | ------------- |
| `git tag -d <tag_name>` | Delete a tag locally. |
| `git push origin -delete <tag_name>` | Delete a remote tag. |

## Checkout Tag
| Command  | Operation |
| ------------- | ------------- |
| `git checkout <tag_name>` | Checkout a specfic tag. |
| `git push origin -delete <tag_name>` | Delete a remote tag. |

If you have checked out a specific tag in Git and want to switch back to the current code (typically the latest commit on the branch), you can do so by checking out the branch you were on before inspecting the tag.

First, you need to identify the branch you were on before checking out the tag. You can use the `git branch` command to list all the branches in your repository and identify the branch you want to switch back to.
The current branch you were on will be indicated with an asterisk (*) next to its name. Once you have identified the branch, you can use the `git checkout` command to switch back to it:

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

## Clone Specific Remote Branch

| Command  | Operation |
| ------------- | ------------- |
| `git clone -b <branchname> <remote-repo-url>` |Used to clone a specific branch from a remote repository using Git. </br> `<branchname>` : Replace this with the name of the branch you want to clone.  </br> `<remote-repo-url>` : Replace this with the URL of the remote repository you want to clone. </br> Here `-b` is just an alias for `--branch`|

 
# Git Fatch
The `git fetch` command is used to retrieve changes from a remote repository. It updates your local repository's references to the remote branches, allowing you to see and interact with the latest changes. By default, it only updates the remote-tracking branches and does not merge the changes into your local branches.

| Command  | Operation |
| ------------- | ------------- |
| `git fatch` |Used to retrieve the latest changes from a remote repository without merging them into your local branches. </br> **1 New branches:** If new branches have been created in the remote repository, `git fetch` will download information about those branches and create or update the corresponding remote-tracking branches in your local repository. </br> **2 Updated branch commits:** If commits have been added to existing branches in the remote repository, `git fetch` will download those commits and update the remote-tracking branches in your local repository to reflect the latest state of those branches. </br> **3 Deleted branches:** If branches have been deleted in the remote repository, `git fetch` will update your local repository by removing the corresponding remote-tracking branches. </br> **4 Tags:** By default, `git fetch` retrieves tags associated with the remote repository. Tags represent specific points in history, often used to mark important milestones or releases.|
|`git fetch <remote> <branch>`|Fetch a specific branch from a remote repository. Replace `<remote>` with the name of the remote repository (e.g., origin) and `<branch>` with the name of the branch you want to fetch.|




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

# Commonly Used Term
**Remote Repository** efers to a copy of a repository hosted on a different server or location than your local repository. A remote repository allows collaboration and sharing of code with other developers.
  

