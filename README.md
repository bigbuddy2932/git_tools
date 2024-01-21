# Git Tools
Some git aliases to make life a git easier.
These tools are made for bash and bash only, no other interpreter is currently supported.

## Commands

### grbrod
Running `gtbrof` will create a new local branch off of a specified remote branch. It will run git fetch before doing this.

```
gtbrof <new branch name> <remote branch name> [remote; default=origin]
```

### groot
Using `groot` will change your current working directory to the root directory of the git repository your working directory is in. If your working directory is not in a git repository nothing will happen.

This command has no arguments.

### gtstatus

An alternative to `git status` is `gtstatus`. It is implmented in a way that shows the full file name from the git root of each file.

This command has no arguments.

