# git filter-branch

### Reference docs

Lets you rewrite Git revision history by rewriting the branches specified, applying custom filters on each revision. Those filters can modify each tree (e.g. removing a file or running a perl rewrite on all files) or information about each commit. Otherwise, all information (including original commit times or merge information) will be preserved.

### Using git's filter branch

Let's run filter branch to scrub that password file from our history:

```
git filter-branch --tree-filter 'rm -f password.txt' HEAD
```

After everything is verified:

```
git update-ref -d refs/original/refs/heads/master
git reflog expire --expire=now --all && git gc --prune=now
```

### Another option

Check out [BFG repo cleaner](https://rtyley.github.io/bfg-repo-cleaner/)
