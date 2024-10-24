﻿###liste of branchs:
 $git branch

###Before creating a new branch, pull the changes from upstream. Your master needs to be up to date.
$ git pull

###create/pull a new branch:
$git checkout -b <branchname>

###change to branch
$git checkout <branchname>

###push the new branch to gitlab:
$git push origin <branchname>

###clone a repository:
$git clone git@blabla.git

###clone a repository (specific branch)
git clone -b develop ssh://git@gitlab-prod.eu.techem.corp:2222/eai/temoreadstatusrouter.git

###Delete a branch on your local filesystem :
$ git branch -d [name_of_your_new_branch]

###Delete a branch on remote repository
$ git push -d origin <branchname>


#Switch over to the branch you want to add new commits to it.
$ git checkout <branch> 

#Stage the file for commit to your local repository
$ git add

#Commit the file that you've staged in your local repository.
$ git commit -m "Add existing file"


####Push the changes in your local repository to Git
$ git push origin your-branch

###Merge a specific file from another branch
$ git checkout <another-branch> <path-to-file> [<one-more-file> ...]  
$ git status  
$ git commit -m "'Merge' specific file from '<another-branch>'"

###State before the merge began
$ git merge --abort

###Stashing Your Work
$ git stash

###Apply one of the older stashes
$ git stash apply

###Hinzufügen/entfernen file zu index bevor commit
$ git add/reset file

###Creating a Branch from a Stash
$ git stash branch testchanges
----------------------------------------------------------------------
###Renaming local and remote
##### Rename the local branch to the new name
git branch -m <old_name> <new_name>

##### Delete the old branch on remote - where <remote> is, for example, origin
git push <remote> --delete <old_name>

##### Or shorter way to delete remote branch [:]
git push <remote> :<old_name>

##### Prevent git from using the old name when pushing in the next step.
##### Otherwise, git will use the old upstream name instead of <new_name>.
git branch --unset-upstream <new_name>

##### Push the new branch to remote
git push <remote> <new_name>

##### Reset the upstream branch for the new_name local branch
git push <remote> -u <new_name>
--------------------------------------------------------------------

### Reset the master Branch to the Desired Commit abc1234
git reset --hard abc1234  
git push --force origin master

