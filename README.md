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

Custom commit command will run "git commit -am '#current_branch $message'"
> gc message

Publish method will execute an set of git commands:
1. gc $message
2. git checkout $pub_branch
3. git fetch
4. git reset --hard origin/$pub_branch
