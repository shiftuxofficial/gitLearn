# gitLearn
This Repo includes all the necessary steps to use git. It is more of a cheatsheet created and regularly updated by developers & designers at Shiftux.


## Download and Install Git Bash:
https://www.git-scm.com/

__________________________________________________
## Open git to configure-
### Set username:
```
git config --global user.name "yourUserName"
```
### Set email:
```
git config --global user.email "youremail@domain.com"
```

### Check if username is set:
```
git config user.name
```

### Check if email is set:
```
git config user.email
```
__________________________________________________
## Commit files to repo (if no files are there):
### Initializing working directory as local repo:
```
git init
```
### To know files are staged or not:
```
git status
```
### Stage all new & modified files:
```
git add .
```
### Stage new or modified single file:
```
git add [file name]
```
### Stage single deleted file
```
git rm [file name]
```
### Stage all modified or deleted files
```
git add -u
```
### Commit with message:
```
git commit -m "message"
```
### Push to remote repo:
```
git branch -M main
git remote add origin [URL]
git push -u origin main
```
________________________________________________________
## Commit files to repo (if files are there):
```
git init
git status
git add .
git status
git add [file name]
git status
git commit -m "message"
git status
git branch -M main
git remote add origin [URL]
git pull origin main --allow-unrelated-histories
git push -u origin main
```
_______________________________________________
## Pull and Merge (for changed files):
```
git init
```
### Fork the repo and pull the contents:
```
git pull [URL]
```
### Make changes in files and push:
```
git add .
git commit -m "message"
git remote add origin [URL]
git push -u origin master
```
___________________________________________________________
## For copying repo in local and pushing files in repo:
```
git init
git clone [URL]
```
### Go to the local repo:
```
cd [path]
```
### Change in a file or add a new file:
```
git add .
git commit -m "message"
git push
```
__________________________________________________
## To show the origin and destination:
```
git remote -v
```
## To remove destination:
```
git remote rm destination
```
## To remove an origin:
```
git remote rm origin
```
__________________________________________________
## Add a new remote upstream repository:
```
git remote add upstream [Parent Repo URL]
```
___________________________________________________
## Sync your fork:
```
git fetch upstream
git checkout master
git merge upstream/master
git push -u origin
```
__________________________________________________
## Change the authorized github account with git:

`Control Pannel > User Accounts > Credential Manager > Windows Credentials > git: https://github.com`
### Remove it
So when try to push stuff to a repo. It will ask for authorization again

__________________________________________________
## For making changes in a different branch of an existing repo:
```
git clone [URL]
cd [path]
git pull [URL]
```
### To see all branches:
```
git branch
```
### Create new branch:
```
git branch -c [branch name]
```
### To make the new branch as new working directory:
```
git checkout [branch name] 
```
### Make changes in file, then stage and commit:
```
git add .
git commit -m [message]
```
### To push in the new branch:
```
git push origin head
```
____________________________________________________
## For Push Content Into Private Contributor repository:
```
mkdir [folder name]
cd [folder name]
git init
git pull [URL]
```
### Make changes in file and commit:
```
git add .
git commit -m "message"
git remote add origin [URL]
git push -u origin main
```
__________________________________________________
## Undo commits:
### For last n commits and keep files staged:
```
git reset --soft HEAD~[n]
```
### For last n commits and unstage changes:
```
git reset --mixed HEAD~[n]
```
### For last n commits and delete changes in code:
```
git reset --hard HEAD~[n]
```
### Delete the push from GitHub (careful if working with team):
```
git push origin main --force
```
__________________________________________________
## Commit with a desired date:
### Replace old commit:
```
GIT_AUTHOR_DATE="[YYYY:MM:DD]T[hh:mm:ss]" GIT_COMMITTER_DATE="[YYYY:MM:DD]T[hh:mm:ss]" git commit --amend --no-edit --date="[YYYY:MM:DD]T[hh:mm:ss]"
```
### Force push amended commit (careful if working with team):
```
git push --force
```
### For New commit:
```
GIT_AUTHOR_DATE="[YYYY:MM:DD]T[hh:mm:ss]" GIT_COMMITTER_DATE="[YYYY:MM:DD]T[hh:mm:ss]" git commit -m "message"
```
### Push:
```
git push
```
__________________________________________________
# For pushing larger files (size>100MB)

### Make sure git is installed

## Download and Install Git Large File Storage:
https://git-lfs.com/

## Configure Git-LFS:
### Open CMD and run:
```
git lfs install
```

## For pushing large files:
```
git lfs track "*.<extension of large file>"
git add .gitattributes
git add <filename>.<extension>
git commit -m "Add large file"
git push origin main
```
