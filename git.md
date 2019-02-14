# git - tips & tricks
```bash
git diff --staged  # show changes that have been staged
```

```bash
git reset --soft HEAD~1  # undo last commit, keep changes staged
git reset --mixed HEAD~1  # undo last commit, unstage changes
git reset --hard HEAD~1  # undo last commit, **delete** local changes
```
