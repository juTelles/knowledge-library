# Git and GitHub basics

## Config Git
use ```--global``` for global configurations (whole pc) and nothing for user configurations

#### Config git user name
``` git config --global user.name "<name>" ```
``` git config user.name "<name>" ```

#### Config git user email
``` git config --global user.email "<email>"```
``` git config user.email "<email>" ```

#### Config default branch
Branch type: ```main``` or ```master```

``` git config --global init.defaultBranch <branchType> ```
``` git config init.defaultBranch <branchType> ```

#### Store credentials
StorageType: ```store``` (pemanente) or ```cache``` (only stored in cache)

``` git config --global credential.helper <storageType> ```
``` git config credential.helper <storageType> ```

## Make new local repository

#### Make new folder to init repository on
```mkdir <projectFolderAddress>```
#### Or go inside folder of the repository to be
```cd <projectFolderAddress>```
#### Initiate repository
```git init```

## Connect a LOCAL repository to a REMOTE repository

1- First create remote repository in GitHub (for example)
2- Then add get the URL of the remote repository created
3- Add the remote repository created to your local repository

``` git remote add origin <remoteRepositoryURL> ```

## Clone existent repository from GitHub (for example)

1- Get the URL of the remote repository
2- Clone the remote repository to your PC

``` git clone <remoteRepositoryURL> ```

A folder containg the contents of the remote repository will be created in your local machine, named the same as the remote repository

If you want the folder to have another name

``` git clone <remoteRepositoryURL> <localRepositoryName(optional)> ```

You can also clone a just a single branch from the remote repository
``` git clone <remoteRepositoryURL> --branch <branchName(optional)> --singleBranch ```

If the branch name to be cloned is not especified in the command it will clone the ```main``` or ```master``` branch (whichever is the main branch of the repository)

## Adding and commiting changes

*You can see the branch status (preparation area status) if you want with
``` git status ```

1- Add all the changes you want to commit
``` git add ```
2 - Then commit those changes with a descritive message
``` git commit -m "message" ```

#### Undo last commit message
``` git commit --amend -m "new message" ```

## Undo changes in LOCAL repository
``` git reset ```
``` git reset --soft ```
``` git reset --mixed ```
``` git reset --hard ```

## Sending your changes to REMOTE repository

1-  Push (get) all the changes that occurred in the remote repository since your last push and resolve any conflits that appear
``` git push ```

2- Then pull (send) your commited changes to the remote repository
``` git pull ```

## Branch manipulations

#### Change to another branch
``` git checkout <branchName> ```

#### Create new branch and change to it
``` git checkout -b <newBranch> ```

#### Delete a branch
``` git branch -d <branchName> ```

#### See last commit in a branch
``` git branch -v ```
