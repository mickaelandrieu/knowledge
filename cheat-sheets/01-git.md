# Git's cheat sheet

A highly opinionated [Git](http://git-scm.com/) cheat sheet:

* [General](#general)
* [Branches](#branches)
* [Tags](#tags)
* [Stashes](#stashes)

Take a look at the [Git tips](../git/tips.md).

## General

* cloning and switching to branch: `git clone <repository> -b <branch-name>`

## Branches

* listing existing branches: `git branch -avv`
* creating a new branch and switching to it: `git checkout -b <branch-name>`
* creating a branch from a remote one and track it: `git checkout -t <remote>/<branch-name>`
* pushing the branch and tracking it: `git push -u <remote> <branch-name>`
* removing the remote branch: `git push <remote> :<branch-name>` (note the `:` before the branch name)
* removing a local branch: `git branch -d <branch-name>` (won't remove unmerged branches)
* removing branches that doesn't exist anymore on the repository: `git fetch -p`
* renaming a branch: `git branch -m <current-branch-name> <new-branch-name>`
* finding unmerged branches: `git banch --no-merged`
* switching to a branch: `git checkout <branch-name>`

## Tags

* listing existing tags with the message: `git tag -n<number-of-lines>`
* creating a new tag: `git tag -a <tag-name> -m '<message>'`
* pushing the tag: `git push <remote> <tag-name>`
* removing a remote tag: `git push <remote> :<tag-name>` (note the `:` before the tag name)
* removing a local tag: `git tag -d <tag-name>`
* renaming a tag: `git tag <old-tag-name> <new-tag-name>; git -d <old-tag-name>`
* changing the tag's commit to the current one: `git tag -f <tag-name>`

## Stashes

* listing stashes: `git stash list`
* creating a new stash: `git stash [save '<description>']`
* applying the stash and remove it: `git stash pop <stash>`
* removing all stashes: `git stash clear`
* removing the stash: `git stash drop <stash>`

### The `<stash>` argument

* refering to a stash by its number: `stash@{<number>}`
* most recent stash: `stash@{0}`
* when ommiting the `<stash>` argument, `stash@{0}` is assumed

References: [git ready](http://gitready.com/beginner/2009/03/13/smartly-save-stashes.html)
