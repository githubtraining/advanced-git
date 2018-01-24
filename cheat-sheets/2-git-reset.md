# git reset

### Reference docs

In the first and second form, copy entries from <tree-ish> to the index. In the third form, set the current branch head (HEAD) to <commit>, optionally modifying index and working tree to match. The <tree-ish>/<commit> defaults to HEAD in all forms.

### Modes of reset

```
git reset --soft HEAD~2
git reset HEAD~
git reset --hard <commit-SHA>
```

### Removing items from the staging area

```
git reset -- <filename>
```

### Reset across merge commits

```
git reset --hard HEAD~^
git reset --hard HEAD~^2
```
