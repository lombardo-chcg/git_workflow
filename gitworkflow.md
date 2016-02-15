# Git Guide

## SOME USEFUL COMMANDS

### inspect the contents of the working directory and staging area
  * git status
  
### show the difference between the working directory, staging area and last commit
  * git diff
  
### view past git commit data
  * git log
  
### create a new branch
  * git checkout -b "branch-name"
    * creates and switches into new branch
  * git branch branch_name            
    * just creates the branch 
  
### switch from one branch to another
  * git checkout branch_name

### add changed files to commit queue
  * git add "file"
  git add .     adds everything in the current directly.  .. is up one directory 
  
### permanently store file changes from the staging area in the repository
  * git commit -m "commit message"   -----commit message should be present tense and 50 characters or less
  
### the commit you are currently on is known as the HEAD commit. In many cases, the most recently made commit is the HEAD commit.  
  * git show HEAD
  
### restore a file to its version at the last commit
  * git checkout HEAD filename
  
### unstage file from the staging area 
  * git reset HEAD filename
  
### return to a specific previous version - (aka - rewind the project history)
  * git reset xxxxxxx      <--- first 7 characters of commit SHA identifier 
  
### merge - git merge temp     
  * branch called temp will be pulled into whatever branch you are currently in  

### delete a branch
  * git branch -d branch_name
  
### Lists all a Git projects branches (current branch marked by *)
  * git branch
  
### list a git projects remotes  
  * git remote -v

### go back to previous file state at time of last commit 
  * git checkout -- filename.ext
 
 
## PUSH COMMIT TO REMOTE REPO

### change from branch to master git
  * git checkout master
  
### pull down any changes from the remote repo  
  * git pull origin master  
  
### switch back to the feature branch
  * git checkout branch-name
  
### merge changes from the master into the feature branch   
  * git merge master
  
### push a copy of your feature branch to remote repo
  * git push origin branch-name
  
### proceed to GitHub and create pull request  

### switch to master branch 
  * git checkout master
  
### pull changes down from GitHub and merge
  * git fetch origin master
  *git merge origin/master
  *OR*  
  * git pull origin master

### delete feature branch 
  * git branch -d branch-name
  
## GIT WORKFLOW
  1. Start New Repo on GitHub
  2. Clone Locally
  3. Create a new local branch and switch to it
  4. Do work
  5. Add new files to staging area
  6. Commit (and comment!)
  
  7. change to master branch and pull down any changes from remote repo
  8. switch to feature branch and pull in (merge) updated master 
  9. push a copy of your feature branch to remote repo
  10. proceed to GitHub and create pull request  
  11. switch to master branch 
  12. pull changes down from GitHub 
  13. delete feature branch 

### start the day with a git pull while in master version locally 
  
  
  
##  TYPICAL COLLABORATION WORKFLOW

- Fetch and merge changes from the remote
- Create a branch to work on a new project feature
- Develop the feature on your branch and commit your work
- Fetch and merge from the remote again (in case new commits were made while you were working)
- Push your branch up to the remote for review