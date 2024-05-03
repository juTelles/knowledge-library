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

## Make NEW LOCAL repository

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

## Clone EXISTENT repository

1- Get the URL of the remote repository
2- Clone the remote repository to your PC

``` git clone <remoteRepositoryURL> ```

A folder containg the contents of the remote repository will be created in your local machine, named the same as the remote repository

If you want the folder to have another name

``` git clone <remoteRepositoryURL> <localRepositoryName(optional)> ```

You can also clone a just a single branch from the remote repository
``` git clone <remoteRepositoryURL> --branch <branchName(optional)> --singleBranch ```

If the branch name to be cloned is not especified in the command it will clone the ```main``` or ```master``` branch (whichever is the main branch of the repository)

## Showing information

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

## ADD (STAGE) changes
Add changes you made to the staged area

#### Add (stage) all the changes you made
``` git add . ```
#### Add (stage) the changes made in a specifique file
``` git add <fileName> ```

## COMMIT changes
Commit all the added (staged) changes with a descritive message
``` git commit -m "message" ```

## Undo commands

#### Undo last commit message
Edit the commit message in the command itself
``` git commit --amend -m "new message" ```
Opens a commit editor where you use vim to edit the message
```git commit --amend```

#### Undo NOT ADDED (NOT STAGED) changes in LOCAL repository
Discards all not added (staged) changes, after use the discarted changes cannot be recuperated
```git restore <fileName>```

#### Undo ADDED changes in LOCAL repository (UNSTAGE)
Undo all added (staged) changes
```git reset .```
or
```git restore --staged .```

Undo all added (staged) changes in specified file
```git reset <fileName>```
or
```git restore --staged  <fileName>```


#### Undo COMMIT in LOCAL repository
Resturns to earlier specified (by its Hash code) commit

Returns to the especified commit and unstages all changes made after
``` git reset <commitHash> ```

Returns to the especified commit and stages (adds) all changes made after
``` git reset --soft <commitHash> ```

Returns to the especified commit and untages all changes made after (default option - the same as git reset)
``` git reset --mixed <commitHash> ```

Returns to the especified commit and discards all changes made after
``` git reset --hard <commitHash> ```

## PUSH changes to REMOTE

1- First PULL (get) all the changes that occurred in the remote repository since your last pull and resolve any conflits that appear
```git pull```

#### PUSH changes
2- Then PUSH (send) your commited changes to the remote repository
``` git push <remoteName> <branchName>```

## PULL changes from REMOTE
PULL (get) all the changes that occurred in the remote repository since your last pull
```git pull```

## FETCH
Downloads all the content of the remote repository without merging this content with you local content, makes a remote/local branch that contains this content
```git fetch origin <branchName>```

If later you wante to actually merge the content fetched with you local repository you can merge them
```git merge origin/<branchName>```

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