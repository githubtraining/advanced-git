# git rerere

### Reference docs

In a workflow employing relatively long lived topic branches, the developer sometimes needs to resolve the same conflicts over and over again until the topic branches are done (either merged to the "release" branch, or sent out and accepted upstream).

This command assists the developer in this process by recording conflicted automerge results and corresponding hand resolve results on the initial manual merge, and applying previously recorded hand resolutions to their corresponding automerge results.

### Configuring rerere

```
git config rerere.enabled true
```

### Set up

Let's create some merge conflicts!

1. `git checkout -b rerere-me`
2. Create, add, and commit 3 files separately
3. `git checkout master`
4. Create, add, and commit the same 3 files, with different content

### Trial merge

First we will do the trial merge:

```
git checkout rerere-me
git merge master
```

Resolve each of the conflicts as you desire, then undo the merge:

```
git reset --hard HEAD^1
```

### Merge again

```
git checkout master
git merge rerere-me
```

Or, for more fun, try doing a rebase:

```
git checkout rerere-me
git rebase master
```




###
