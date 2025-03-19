# gitLearn
This Repo includes all the necessary steps to use git. It is more of a cheatsheet created and regularly updated by developers & designers at Shiftux.


## Download and Install Git Bash:
https://www.git-scm.com/

__________________________________________________
## Set username:
Open git and type-
```
git config --global user.name "yourUserName"
```
## Set email:
```
git config --global user.email "youremail@domain.com"
```

## Check if username is set:
```
git config user.name
```

## Check if email is set:
```
git config user.email
```
__________________________________________________
## Commit files to repo (if no files are there):
```
git init
git add README.md
```
Stage all files:
```
git add .
```
Stage single file:
```
git add [file name]
```
```
git commit -m "message"
git branch -M main
git remote add origin [URL]
git push -u origin main
```

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

## Pull and Merge (for changed files):
```
git init
```
Fork the repo
```
git pull [URL]
```
Make changes in files
```
git add .
git commit -m "message"
git remote add origin [URL]
git push -u origin master
```

## For copying repo in local and pushing files in repo:
```
git init
git clone [URL]
```
Enter the local repo:
```
cd [path]
```
Change in a file or add a new file:
```
git add .
git commit -m "message"
git push
```
__________________________________________________
## To Show the origin and Destination:
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

## Sync your fork:
```
git fetch upstream
git checkout master
git merge upstream/master
git push -u origin
```
__________________________________________________
## Change the authorized github account with git:

Control Pannel > User Accounts > Credential Manager > Windows Credentials > git: https://github.com 
Remove it<br>
So when try to push stuff to a repo. It will ask for authorization again

__________________________________________________
## For making changes in a different branch of an existing repo:
```
git clone [URL]
cd [path]
#git pull [URL]
git branch #to see all branches
git branch -c [branch name] #new branch created
git checkout [branch name] #to make the new branch as new working directory
# change in file
git add .
git commit -m [message]
git push origin head #to push in the new branch
```

## For Push Content Into Private Contributor repository:
```
create folder
open terminal
git init
git pull <repo URL>
//Change in file
git add .
git commit -m "message"
git remote add origin<repo URL>
git push -u origin main
```
__________________________________________________
# For pushing larger files (size>100MB)

### Make sure git is installed

## Download and Install Git Large File Storage:
https://git-lfs.com/

## Configure Git-LFS:
Open CMD and run:
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
