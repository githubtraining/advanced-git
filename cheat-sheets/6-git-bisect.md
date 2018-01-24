# git bisect

### Reference docs

This command uses a binary search algorithm to find which commit in your project’s history introduced a bug (or a performance improvement).

### The Set-Up

Let's make a file called password.txt and hide it in our branch.

### The long version

```
git bisect start
git bisect bad <bad-revision>
git bisect good <good-revision>
```

At each pause, test to determine whether the "bug" exists. If the bug exists at the revision, type `git bisect bad`. If everything is ok, type `git bisect good`.

To end the bisect, type:

```
git bisect reset
```

### The quick(er) version

```
git bisect start <bad-revision> <good-revision>
git bisect run ls password.txt
```
