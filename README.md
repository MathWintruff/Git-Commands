Git Commands
============

_A list of my commonly used Git commands_

*If you are interested in my Git aliases, have a look at my `.bash_profile`, found here: https://github.com/joshnh/bash_profile/blob/master/.bash_profile*

--
### Starting with a Repository

`!!! create a new repository on the command line !!!`
| Command | Description |
| ------- | ----------- |
| `git init`| Initialize the local repository |
| `git add README.md`|  add a Readme file in the local repository|
| `git add -A` | Add all new and changed files to the staging area |
| `git branch -M main`| select or create a Main repository |
| `git commit -m "first commit"`|  commit changes to git|
| `git remote add origin https://github.com/MathWintruff/test.git`| Add and Set the remote repository of git for the local repository |
| `git push -u origin main`| Push to github (if the repository doens's exist it will be created) |

`!!! push an existing repository from the command line !!!`
| Command | Description |
| ------- | ----------- |         
| `git remote add origin https://github.com/MathWintruff/test.git`| Add and Set the remote repository of git for the local repository |
| `git branch -M main`| select or create a Main repository |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "first commit"`|  commit changes to git|
| `git push -u origin main`| Push to github (if the repository doens's exist it will be created) |

### Usefull Commands

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git reset <commit> -- <path>` | Unstage files on Git - By default, the commit parameter is optional : if you don’t specify it, it will be referring to HEAD. |
| `git reset` | Unstage all files on Git |
| `git git checkout -- <path>` | Remove unstaged changes |
| `git checkout -- .` | Discard your entire working directory |
| `git reset --soft <commit>` | Unstage commits softly (just unstage the commit) |
| `git reset --hard <commit>` | Unstage commits hardly (unstage and discart all changes of the commit) |
| `git rm --cached FILENAME` | Ignore an allready staged and commited file |
| `git rm --cached FOLDERNAME -r` | Ignore an allready staged and commited folder |
| `touch .gitignore ` | Creates the .gitignore on the folder executed |
| `git config --global core.excludesfile ~/.gitignore_global` | Opens the Global .gitignore |
| `git check-ignore [<options>] <pathname>` | Check whether the file is excluded by .gitignore and output the path if it is excluded |
| `git git check-ignore [<options>] --stdin` | For each pathname given via a file via --stdin, check whether the file is excluded by .gitignore and output the path if it is excluded |
### [<options>]:
-q, --quiet
Don’t output anything, just set exit status. This is only valid with a single pathname.

-v, --verbose
Instead of printing the paths that are excluded, for each path that matches an exclude pattern, print the exclude pattern together with the path. (Matching an exclude pattern usually means the path is excluded, but if the pattern begins with ! then it is a negated pattern and matching it means the path is NOT excluded.)

For precedence rules within and between exclude sources, see gitignore[5].

--stdin
Read pathnames from the standard input, one per line, instead of from the command-line.

-z
The output format is modified to be machine-parsable (see below). If --stdin is also given, input paths are separated with a NUL character instead of a linefeed character.

-n, --non-matching
Show given paths which don’t match any pattern. This only makes sense when --verbose is enabled, otherwise it would not be possible to distinguish between paths which match a pattern and those which don’t.

--no-index
Don’t look in the index when undertaking the checks. This can be used to debug why a path became tracked by e.g. git add . and was not ignored by the rules as expected by the user or when developing patterns including negation to match a path previously added with git add -f.


### Getting Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
| `OR`|
| `git clone https://github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |


### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |
