# git checkout

### Reference docs

Updates files in the working tree to match the version in the index or the specified tree. If no paths are given, git checkout will also update HEAD to set the specified branch as the current branch.

### Discarding changes

```
git checkout -- <file-name>
```

### Moving branches

```
git branch <branch-name>
git checkout <branch-name>
git checkout -b <branch-name>
```

### Checkout conflicts

```
git stash
git checkout --force <branch-name>
```

### Detached HEAD state

```
git checkout v1.0
git checkout <commit-sha>
```

### Where has HEAD been?

```
git reflog
```
