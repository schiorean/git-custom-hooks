# Git Custom Hooks

Using this script you can customize the pre and post hooks for git.

# Installation

Clone this repository into your on PC, recomended somewhere on home (` ~/ `) folder. <br/>
Edit `~/.bash_profile` and add as source the `git-custom-hooks` file
> `source ~/path/to/the/file/git-custom-hooks`

# Usage

If you want to apply the hook for all repositories on your pc, put the hook file on `/hooks` folder from this repository.
If you want a hook to be applied just for an particular repository, put the hook file on `.git/hooks` folder from the repository

Name of hook must be `pre-<sub-command-name>` or `post-<sub-command-name>` <br/>
Like:

- pre-merge
- pre-branch
- pre-pull

# Custom commands

1. Custom commit command.
Usage:
> gc your custom commit message
  
What will execute
> git commit -am '#current_branch your custom commit message'

2. Publish method.
Usage:
> pb branch_to_publish your custom commit message

What will execute:
> `git commit --no-edit -am '#curent_branch your custom commit message'`

> `git checkout branch_to_publish`

> `git fetch`

> `git reset --hard origin/branch_to_publish`

> `git merge branch_where_you_was`

If you have conflicts, all process is stopped and you have to fix the conflicts and crun next commands manually

> `git push`

> `git checkout branch_where_you_was`

