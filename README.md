# Git Custom Hooks

This script let you to set the custom pre and post hooks for git subcommands.

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
