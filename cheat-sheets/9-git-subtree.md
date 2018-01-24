# git subtree

### What is it?

The subtree command adds a subdirectory containing the files from a second repository. The history for the sub-project is grafted onto the existing tree of the parent project.

### Adding a subtree

```
git subtree add --prefix=example-submodule https://github.com/githubtraining/example-submodule master --squash
```

### Updating the subtree

To pull in changes made in the subtree repository:

```
git remote add subtree-remote https://github.com/githubtraining/example-submodule
git subtree pull --prefix=example-submodule subtree-remote master --squash
```
