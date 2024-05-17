## Download Git Bash  
[Download](https://www.git-scm.com/)  

---  
## Set username:  

```
git config --global user.name "yourName"

#example
git config --global user.name "PALLADIUM26"
```  
---  
## Set email:  

```
git config --global user.email "yourEmail"

#example
git config --global user.email "pranithdutta26@gmail.com"
```  
---  
 
### Check if Username is set:  

```
git config user.name
```  
---  
### Check if Email is set:  

```
git config user.email
```  
---  

## Commit files to Repository:

<details>

<summary>If No Files are there</summary>  
 
 
``` 
#initialization
git init

#to add README file
git add README.md


#for adding all files
git add . 


#for adding particular file
git add [file name]


#commit message
git commit -m "message"


#renaming Branch
git branch -M main


#add remote repository
git remote add origin [link]


#to upload the remote repository
git push -u origin main
```  

</details>

<details>

<summary>If Files are there:</summary>


```
#initialization
git init

#Show working tree status
git status

#for adding all files
git add . 

#Show working tree status  
git status

#for adding particular file
git add [file name]

#Show working tree status
git status

#commit message
git commit -m "message"

#Show working tree status
git status

#renaming Branch
git branch -M main


#add remote repository
git remote add origin [link]

#to fetch and download content from a remote repository
git pull origin main --allow-unrelate-history


#to upload the remote repository
git push -u origin main
```  
</details>  

---  

## Pull and Merge (for changed files):  

```
#initialization
git init

#fork the repo
git pull [link]

#change in file
git add .

#add commit message
git commit -m "message"

#add remote repository
git remote add origin [link]

#to upload the remote repository
git push -u origin master
```
---  

### For copying repository in local machine and pushing files in the repository:


```
#initialization
git init

#clone the repository to local machine
git clone [url]

#change the working directory
cd [path] 

#change in a file or add a new file
git add .

#add commit message
git commit -m "message"

#to upload the remote repository
git push
```  
---  

### To Show the origin and Destination:  

```
git remote -v

#To remove an origin or destination
git remote rm destination
git remote rm origin
```  
---  

# Add a new remote upstream repository  

```
git remote add upstream [Parent Repo Link]
```  

# Sync your fork  

```
#to download contents from a remote repository
git fetch upstream

#to navigate between the branches created by git branch
git checkout master

#to combine two branches
git merge upstream/master

#to upload the remote repository
git push -u origin
```  

---  

### Change the authorized github account with git  

Control Pannel > User Accounts > Credential Manager  
> Windows Credentials > git: https://github.com  

### Remove it  
So when try to push stuff to a repo. It will ask for authorization again  

---  

# For making changes in a different branch of an existing repo:

```
#to clone the repository in local machine
git clone [link]

#change the working directory
cd [path]

#git pull [link]

#to see all branches
git branch 

#new branch created
git branch -c [branch name] 

#to make the new branch as new working directory
git checkout [branch name] 


#change in file
git add .

#commit message
git commit -m [message]

#to push in the new branch
git push origin head 
```  

---  

### For Push Content Into Privet Contributor repository

Creat Folder  
Open Terminal,then  
  
```
#initialization
git init

#to fetch and download content from a remote repository
git pull <repo link>

#Change in file
git add .

#commit message
git commit -m "message"


git remote add origin <repo link>

#to upload the remote repository
git push -u origin main
```  

---  