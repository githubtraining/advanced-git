# git submodule

### Reference docs

A submodule is a repository embedded inside another repository. The submodule has its own history; the repository it is embedded in is called a superproject.

### Adding a submodule

```
git submodule add https://github.com/githubtraining/example-submodule
git commit -m "adding new submodule"
```

### Seeing what has changed

```
git diff --cached example-submodule
git diff --cached --submodule example-submodule
```

### Cloning a repository with a submodule

Anyone who clones will need to:

```
git clone --recursive URL
```

Anyone who already has a local copy of the repo will need to:

```
git submodule update --init
```

### Updating the submodule

To pull in changes made in the submodule repository:

```
git submodule update --remote
```
