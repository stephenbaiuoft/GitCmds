## git reset commits
* `git reset --soft HEAD^` will uncommit && unstage all staged files **with changes!**
* `git reset --HARD HEAD^` will remove the current commit HEAD points to

## git rebase (Squash & Iteractive)
* `git rebase -i HEAD^_num1` **num1** is number of commits including Head before the commit you'd like as it is num1's parent from the HEAD

## git branch + upstream
*`git branch --unset-upstream` (upset tracking stream)
*`git branch -u <upstream-branch>` is only used for fetch and pull information 

## git push + remote branch
* `git push origin --delete remote_branch` (removes the remote branch)
* on your local_branch run `git push origin <localbranch>:<remotebranchname>`


## git branch
* `git branch -m new-name` (if on branch to be modified)
* `git branch -m old-name new-name`
* `git branch --merged` (show branches that have been merged before)
* `git branch --no-merged` (show branches that have not merged)

## git mergetool
* `git mergetool` to help with mergin

## git diff remarks
* `<<<<<<< HEAD` : your current branch that called merge or rebase
* `>>>>>>`: the other branch to be merged in

## git checkout + branch
* `git checkout -b branch_1` (create branch_1 off the current branch and checkout to branch_1)

## git amend
* `git commit --amend` (change prev commit message or allow you add additional files)

## git log
* `git log -p -2` (last 2 patch changes)
* `git log --status` (file changes + abbrev)

## git diff

* `git diff --statged` (staged vs previous commits)
* `git diff` (changed but not staged)
* `git status -s` (short for files only)

## git checkout
* `git checkout HEAD .` (restore to HEAD commit, ignore all changed/staged modifications)

## git rm
* `git rm --cahced file_1` (untrack the file_1)
* `git rm file_1` (next commit, file_1 is gone!)

## git unstage files 
* git rm --cached <filePath> does not unstage a file, it actually stages the removal of the file(s) from the repo (assuming it was already committed before) but leaves the file in your working tree (leaving you with an untracked file).

* git reset -- <filePath> will unstage any staged changes for the given file(s).
    That said, if you used git rm --cached on a new file that is staged, it would basically look like you had just unstaged it since it had never been committed before.