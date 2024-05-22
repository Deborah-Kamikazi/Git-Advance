#git Advance exercise

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

  ### Dropping a Commit:
  