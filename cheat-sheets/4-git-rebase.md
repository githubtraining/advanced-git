# git rebase

### Reference docs

If a branch is specified, git rebase will perform an automatic git checkout to the target branch before doing anything else. Otherwise it remains on the current branch.

All changes made by commits in the current branch (but that are not in the target branch are saved to a temporary area and then reapplied to the current branch, one by one, in order.

### Simple rebase

```
git checkout rebase-me
git rebase -i master
```

### Rebase in place

```
git rebase -i <commit-SHA>
```

### Rebase with conflicts

```
git checkout rebase-conflict
git rebase -i master
```
