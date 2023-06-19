# Git Guilde
## What is the Git?
- Git is an open source distributed version control system. The git source code is hosted on Github, Gitlap, ops,...
- Git is used primarily by developers to manage their source code. Git records changes to files over time, integrity of those changes at each stage of processing. Users can revert to earlier versions and compare different versions at the file level.
- **Git is not limited to source code**
## Workflow
- Working directory (WD): Make change to file:
	- Additions
	- Deletions
	- Modifications
- Staging Area (SA)
	- file ready to commit
- Repository (Repo)
	- Change are saved to repository as commit
## Basic statement
1. Git init: Use to create new local repository. It set up tool for git too.
> `git init`
2. Git clone: Use to clone repository from server source (Github, Gitlap, ops,...)
> `git clone [git url]`

>`git clone https://github.com/Arthur-Cap/gitGuilde.git`
3. git status: Use to check changed of WD and SA
> `git status`
4. git add: Add file change from WD to SA
> `git add [file name 1], ..., [file name n]`


or
> `git add .`

to add all file change.
4. git diff: Use to check modify between WD and SA
> `git diff [file name]`
5. git commit: Use to move file change from SA to repo
> `git commit [options]`

`[options]`:
- `--m`: add message to commit
> `git commit --m [message]`
- `--amend`: update to the latest commit
> `git commit --amend [message]`

or
> `git commit --amend --no-edit`

to update without change message

`[message]`:
- must write in quotes
- use present sentense
- should be shorter than 50 character
- should define what this commit do
6. git log: Use to get list of commit before
>`git log` 

or 
>`git log [options]`

`[option]`
- --graph: use to display like graph
- --oneline: use to display only commit title
## Back track
1. HEAD:

Head is the latest commit has been added to repository

2. Get information of commit
> `git show HEAD`
3. Restore:
- Restore file to the latest commit
> `git checkout HEAD [filename]`
- Reset move file from SA to WD
> `git reset HEAD [filename]`
- Reset all file to commit
> `git reset [options] [SHA]`

`[SHA]` is the first 7 charaters of commit id

`[options]`:
- --soft: don't touch the index file or the working tree at all. This leave all change to SA
- --mixed: (default) don't touch the index or the working tree at all. This leave all change to WD
- --hard: Reset the index and working tree. any change simply will have been deleted
- --mirge: Reset the index and working tree of any diffrent between `[SHA]` and `HEAD`
4. Stash change
- stash all change
> `git stash`
- get the last change has been stashed
> `git pop`