# GitNotes
# Stash
## Stash Changes

| Command  | Operation |
| ------------- | ------------- |
| `git stash save "optional message for yourself"` | This saves your changes and reverts the working directory to what it looked like for the latest commit. Stashed changes are available from any branch in that repository.  Note that changes you want to stash need to be on tracked files. If you created a new file and try to stash your changes, you may get the error No local changes to save.|
| `git stash push -m "say-my-name"` | - |
| `git stash list`  |  Shows a list of all stashes made in a Git repository, which can include changes that have been temporarily saved but not committed.  |

## Retrieve Stashed Changes

To retrieve changes out of the stash and apply them to the current branch you’re on, you have two options: <br/>
Difference Between Pop and Apply Git Stashes <br/>
The difference between `git stash apply` and `git stash pop` is `apply` option only applies the stash while the `pop` option applies the stash but also removes the stash from the stack.

| Command  | Operation |
| ------------- | ------------- |
| `git stash apply STASH-NAME`  | Applies the changes and leaves a copy in the stash  |
| `git stash pop "stash@{index}"`  | Applies the changes and removes the files from the stash  |

## Delete Stashed Changes
| Command  | Operation |
| ------------- | ------------- |
| `git stash drop`  | Removes the most recently stashed changes from the repository.  |
| `git stash drop "stash@{index}"`  | Removes a specific stash version.  |
| `git stash clear`  | Removes all stashes from the repository  |



