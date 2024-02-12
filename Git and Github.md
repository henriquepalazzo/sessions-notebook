# Git Cheat sheet

## SETUP INIT

git init
initiate a repository on your local machine

git clone
create a clone of a remote repository on your local machine

## STAGE & SNAPSHOT

git status
shows modified and staged files

git log

git add
add files to the stage

git reset
unstage files

git diff
shows the difference between files

git restore --staged <file>

git commit -m 'Commit message'

## BRANCHING

git push <remote> <branch>
git branch a
git branch -D <branch>

**git checkout <branch>**

git checkout -b <branch>

**git switch**
Creates and automatically moves to the created branch

git switch -c <branch>

**git pull**
Update your local repo with the updated version from the remote repo

**git merge**
Merges a branch into another

**git rebase**
