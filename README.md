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

# Custom prompt
  If you want a custom prompt which show you the current git branch, like this:
  
  > user@hostname ~/work/directory (current_branch_name)
  
  You have to edit `git-custom-hooks` and uncomment lines 59 and 60
  
  #### From:
  
  > #GIT_PS1_SHOWCOLORHINTS=true
  
  > #PROMPT_COMMAND='__git_ps1 "\e[0;32m\u@\h \e[0;33m\w" "\e[0m\n\\\$ "'
  
  
  #### To:
  
  > GIT_PS1_SHOWCOLORHINTS=true
  
  > PROMPT_COMMAND='__git_ps1 "\e[0;32m\u@\h \e[0;33m\w" "\e[0m\n\\\$ "'
  

# Custom commands

### Custom commit command.

Usage:
> gc your custom commit message
  
What will execute
> git commit -am '#current_branch your custom commit message'



### Publish method.
Usage 1:
> pb branch_to_publish your custom commit message

What will execute:
> `git commit --no-edit -am '#curent_branch your custom commit message'`

> `git checkout branch_to_publish`

> `git fetch`

> `git reset --hard origin/branch_to_publish`

> `git merge branch_where_you_was`

If you have conflicts, all process is stopped and you have to fix the conflicts and run next commands manually

> `git push`

> `git checkout branch_where_you_was`

<br/>
<br/>

Usage 2:
> pb current_branch your custom commit message

What will execute:
> `git commit --no-edit -am '#curent_branch your custom commit message'`

> `git pull`

> `git push`
