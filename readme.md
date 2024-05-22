# gitgit Advance exercise

## part1:

### Splitting a Commit:
```
 91  git reset HEAD~
   92  git reset HEAD~
   93  git add test3.md
   94  git commit -m "Create Third File "
   95  git add test4.md
   96  git commit -m "create fouth file "
   97  git status
   98  git add readme.md
   99  history
   ```

   ### Advanced Squashing:
   ```
   100  git rebase -i --root
  101  git rebase -i HEAD~2
  102  git status
  103  git add .
  104  git status
  105  git add readme.md
  106  git commit -m "change on readme "
  107  git rebase -i HEAD~2
  108  git rebase -i --root
  109  history
  ```

  ### Dropping a Commit:
  ```
  110  git add Unwanted.txt
  111  git commit -m "chores:unwanted commit "
  112  git -i HEAD~2
  113  git rebase -i --root
  114  git status
  115  git add readme.md
  116  git status
  117  git  -i --root
  118  git rebase -i --root
  119  git commit -m 'change on readme '
  120  git rebase -i -root
  121  git rebase -i --root
  122  git rebase -i --root
  123  git rebase --continue
  124  git log
  125  git rebase --edit-todo
  126  git rebase --edit-todo
  127  git log
  128  git rebase --continue
  129  git log
  130  history
  ```
  
 ### Reordering Commits:
 ```
 81  git commit -m "another change on read me "
   82  git history
   83  git branch
   84  git branch main
   85  git branch
   86  git checkout main
   87  git status
   88  git log --oneline
   89  git rebase -i --root
   90  git log --oneline
   91  git rebase --continue
   92  git log
   93  git log --oneline
   94  git rebase -i HEAD~3
   95  git rebase --continue
   96  git rebase --skip
   97  git log
   98  git log --oneline
   99  git rebase -i HEAD~3
  100  git rebase -i HEAD~3
  101  git rebase -i HEAD~4
  102  git rebase -i HEAD~5
  103  git rebase -i HEAD~8
  104  git rebase -i HEAD~7
  105  git log --oneline
  106  git rebase -i HEAD~7
  107  git log --oneline
  108  git rebase -i HEAD~7
  109  git log --onelone
  110  git log --oneline
  111  history

 ```
  ### Cherry-Picking Commits:
  ```
  116  git branch ft/branch
  117  git checkout ft/branch
  118  git add test5.md
  119  git commit -m "change on fith file "
  120  git checkout main
  121  git log
  122  git chechout ft/branch
  123  git checkout ft/branch
  124  git log
  125  git checkout main
  126  git cherry-pick 3bae3e1ff01586476074f2485a81894d08af1c4c
  127  git log --oneline
  128  history

  ```
  ### Visualizing Commit History (Bonus):
  ```
  129  git add readme.md
  130  git commit -m "used cherry-pick "
  131  git log --graph
  132  git log
  133  history

  ```
  ### Understanding Reflogs (Bonus):
  ```
   134  git add readme.md
  135  git commit -m "visualizing commit history "
  136  git reflog
  137  history
  138  git add readme.md
  139  git commit -m "understanding reflogs "
  140  history 
  ```
  # part2:
  ### Feature Branch Creation:
  ```
  149  git branch ft/new-feature
  150  git checkout ft/new-feature
  ```
  ### Working on the Feature Branch:
  ```
   git add feature.txt
  152  git commit -m "Implemented core functionality for new feature "
  ```
  ### Switching Back and Making More Changes:
  ```
  156  git checkout main
  157  git add readme.txt
  158  git commit -m "Updated project readme "
  159  history

  ```
  ### Local vs. Remote Branches:
  ```
   160  git push origin ft/new-feature
  161  git push origin ft/new-feature
  162  history
  ```
  ### Local vs. Remote Branches:
  ```
  160  git push origin ft/new-feature
  161  git push origin ft/new-feature
  162  history
```
### Branch Deletion:
```
 163  git branch -d ft/new-feature
  164  git merge -sft/new-feature
  165  git branch -D ft/new-feature
  166  history

```
### Creating a Branch from a Commit:
```
 167  git log
  168  git log --oneline
  169  git checkout -b ft/new-branch-from-commit HEAD~2
  170  history

```
### Branch Merging:
```
 171  git checkout main
  172  git merge ft/new-branch-from-commit
  173  history
```
### Branch Rebasing:
```
 174  git checkout ft/new-branch-from-commit
  175  git rebase main
  176  history

```
### Renaming Branches:
```
 177  git branch -m ft/new-branch-from-commit ft/improved-branch-name
  178  history
```
### Checking Out Detached HEAD:  
```
 182  git checkout 85cc263f71bce1faff490ee19282c4033c82d404
  183  git add readme.md
  184  git commit -m "addition of part 2 "
  185  git checkout 85cc263f71bce1faff490ee19282c4033c82d404
  186  git checkout main
  187  git log
  188  git  log --oneline
  189  git reset b4109e9
  190  git reset b4109e98ce0f3bc792ce3d46dc86509b4a86a51e
  191  git checkout ft/improved-branch-name
  192  git add .
  193  git commit -m "changes on ft/improved-branch-name "
  194  git push
  195   git push --set-upstream origin ft/improved-branch-name
  196  git checkout main
  197  git pull
  198  history
```
# part3:
### Stashing Changes:
```
 199  git stash
  200  git stash apply
  201  git add readme.md
  202  git commit -m "the start of part 3 "
  203  history
```
### Retrieving Stashed Changes:
```
 209  git stash pop
  210  git add readme.md
  211  git commit -m "retrieving stashed changes "
```
### Branch Merging Conflicts (Continued):
```
 git merge ft/branch
  215  history
```
### Resolving Merge Conflicts with a Merge Tool:
```
 216  git mergetool
  217  git help config
  218  history

```
### Understanding Detached HEAD State:
```
 219  git add .
  220  git commit -m "changes on part3 "
  221  git push
  222  git git checkout ft/improved-branch-name
  223  git checkout   ft/improved-branch-name
  224  git checkout main
  225  history

```
### Ignoring Files/Directories:
```
```
### Working with Tags:
```
 226  git tag v1.0
```
### Listing and Deleting Tags:
```
 226  git tag v1.0
  227  history
  228  git tag
  229  git tag -d v1.0
  230  git tag
  231  history

```
### Pushing Local Work to Remote Repositories:
```
```