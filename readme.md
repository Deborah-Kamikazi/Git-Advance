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