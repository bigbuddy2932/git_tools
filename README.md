# Git Tools
Some git aliases to make life a git easier.
These tools are made for bash and bash only, no other interpreter is currently supported.

## Commands

### grbrof
Running `gtbrof` will create a new local branch off of a specified remote branch, then push the newly created branch to the remote. It will run `git fetch` before doing this.

```
gtbrof <new branch name> <remote branch name> [remote; default=origin]
```

### gtchp
Running `gtchp` will attempt to checkout a branch from the specified remote, and pull in the latest changes. If the branch already exists locally, it will checkout that branch and pull. It will run `git fetch` before doing any of this this.

```
gtbrof <remote branch name> [remote; default=origin]
```

### groot
Using `groot` will change your current working directory to the root directory of the git repository your working directory is in. If your working directory is not in a git repository nothing will happen.

This command has no arguments.

### gtstatus

An alternative to `git status` is `gtstatus`. It is implmented in a way that shows the full file name from the git root of each file.

This command has no arguments.
