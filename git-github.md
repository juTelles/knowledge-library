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

## Showing different types of information on Git

#### Status
You can see the branch status (preparation area status) if you want with
``` git status ```

#### Commit logs
``` git log ```

Output Example:
```
commit 41cd38e227acfb1a5c7847329fd3172d062b9dc0 (HEAD -> master)
Author: userName <userEmail>
Date:   Thu May 2 23:00:33 2024 -0300`
```
This give us the commit hash (unique to the especifique commit), its autor and date

#### More detailed history of commits
```git reflog```

## Adding and commiting changes

1- Add (stage) all the changes you made to the project
``` git add . ```
or add (stage) the changes made in a specifique file
``` git add <fileName> ```

2 - Then commit those changes with a descritive message
``` git commit -m "message" ```

## Undo commands

## Undo last commit message
Edit the commit message in the command itself
``` git commit --amend -m "new message" ```
Opens a commit editor where you use vim to edit the message
```git commit --amend```

## Undo CHANGES in LOCAL repository
Discards all not commited changes, after use the discarted changes cannot be recuperated
```git restore <fileName.fileExtension>```

## Undo COMMIT in LOCAL repository
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

## Additional information

#### gitKeep
Git won't recoganize empty folders as commitable changes, so files named .gitKeep, are empty files named that way as a convenction to sinalize e make it commitable a empty folder

#### Delete Git repository from folder
1- Go into the folder you want not to be a Git repository anymore
``` cd <folderAddress>```
2- Remove the .git file from the folder
```rm -rf .git```

#### using vim editor
Press ```i``` to edit
Press ESC and write ```:wq``` to write (save) and exit
w => write
q => exit

*Depending on model, version and configuration of your git and IDE, if your Git is vinculated to a IDE it opens the commit in a git commit file in your IDE, this file can be normally edited and changes you take effect when closed.