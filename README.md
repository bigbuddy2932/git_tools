# Git Tools
Some git aliases to make life a git easier.
These tools are made for bash and bash only, no other interpreter is currently supported.

## Aliases
This section is for any aliases made via the alias command.

### gtfp
GiT Fetch Prune

Alias for `git fetch -p`

## Functions
These are the bash functions brought in by Git Tools.
This documentation, for the most part, uses the [IEEE Utility Argument Syntax](https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap12.html).
Default values for optional parameters are represented with `; default=defaultValue`. Not all optional paramters necessarily have default values.
Parameter order matters.

### gtbrof
GiT BRanch OF

Running `gtbrof` will create a new local branch off of a specified remote branch, then push the newly created branch to the remote.
It will run `git fetch` before doing this.

```
gtbrof <new branch name> <remote branch name> [remote; default=origin]
```

### gtchp
GiT CHeckout Pull

Running `gtchp` will attempt to checkout a branch from the specified remote, and pull in the latest changes.
If the branch already exists locally, it will checkout that branch and pull.
It will run `git fetch` before doing any of this this.

```
gtchp <remote branch name> [remote; default=origin]
```

### gtchc
GiT CHeckout Commit

A specific commit hash can be selected and branched off of with `gtchc`.
If a branch name is specified, then the newly created branch will also be pushed to the remote.

```
gtchc <commit hash> [new branch name; default=branch_<commit hash>] [remote; default=origin]
```

### gtdb
GiT Delete Branch

Delete a selected branch both locally and remotely with `gtdb`.

The escape branch paramter is used to switch branches before the deletion takes place.
It uses `gtchp` to do this.
Escape branch is generally not required, but is requried if `gtdb` is used to delete the currently checked out branch.


```
gtdb <branch to delete> [escape branch] [remote; default=origin]
```

### groot
Git ROOT

Using `groot` will change the working directory to the root directory of the git repository the current working directory is in.
If the current working directory is not in a git repository, then nothing will happen.

This command has no arguments.
