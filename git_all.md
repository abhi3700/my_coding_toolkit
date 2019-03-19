# Git & Github Essentials
## Commands
* ##### `git init` - intialize git within a non-Github folder (i.e. a local folder)
* ##### `git add .` - add all the files, folders inside a repo. for commit.
* ##### `git add ./find.cpp` - adding a `.cpp` file for commit.
* ##### `git commit -m "Add a comment"` - commit to the master branch.
* ##### `git push origin <branch-name>` - pushing the added commit (locally) to the remote url (respective branch).
  E.g. `git push origin master` - pushing the commits in the local master branch to the remote master branch.
* ##### `git pull origin master` - pulling the Master branch of the repo.
* ##### Add a remote url to a git repo.
  ```console
  # Set a new remote
  $ git remote add origin https://github.com/user/repo.git

  # Verify new remote
  $ git remote -v
  > origin  https://github.com/user/repo.git (fetch)
  > origin  https://github.com/user/repo.git (push)
  ```
* ##### `git remote -v` - verify the url of the repo.
* ##### `git clone <repo-url>` - clone a github repository from link like - https://github.com/EOSIO/eosio.cdt
* ##### `git clone <repo-url> <your-repo-name>` - clone a github repository with a custom name.
* ##### `git clone -b <branch> <remote_repo>` - clone a specific branch (only) of github repo.
  E.g. - `git clone -b v1.x --single-branch https://github.com/gabime/spdlog.git` [git v1.7.10 and later]
* ##### `svn checkout <repo-url>` - clone a github repo.
* ##### `svn checkout <repo-url> <custom-name>` - clone a github repo with a custom local name.
* ##### `svn checkout <modified-repo-url> <custom-name-optional>` 
  clone a folder from github repo. Original repo-url - `https://github.com/EOSIO/eosio.cdt`
  - Master branch: modified-repo-url --> `https://github.com/EOSIO/eosio.cdt/trunk/libraries`
  - other branch: modified-repo-url --> `https://github.com/EOSIO/eosio.cdt/branches/develop/libraries`
* ##### `svn update` - Update the repo. by going inside the folder.
* ##### `git pull` - Update the repo. by going inside the folder.
* ##### `git submodule add <repo-url.git> <custom-repo-name>` - add submodule
* ##### `git-delete-submodule <custom-repo-name>`: delete submodule
  - First, install [`git-extras`](https://github.com/tj/git-extras) - [Installation](https://github.com/tj/git-extras/blob/master/Installation.md)
* ##### update submodule
  - `$ cd <custom-submodule-repo-name>`
  - `$ git pull`
* ##### `git submodule status` - check submodule status inside the parent repo.
* ##### `git status` - check the status of files, folders changed.
* ##### `git submodule update` - update the submodule after cloning any git repo.
* ##### `git branch` - list the branches. `*` shows the current branch.
* ##### `git log` - logs all the commits. Press <kbd>down arrow</kbd> to scroll down. Type <kbd>q</kbd> to exit out of **END** display in the terminal.
* ##### `git branch cool-new-feature` - create a branch **cool-new-feature**
* ##### `git checkout cool-new-feature` - work in the branch **cool-new-feature**
* ##### `git merge cool-new-feature master` - merge **cool-new-feature** with the master branch
* ### origin vs master:
  - **origin**:When you clone a repository for the first time origin is a default name given to the original remote repository that you clone, from where you want to push and pull changes. So basically ‘origin’ is alias of your so big remote repository name. By saying git push origin <branch_name> , you are saying to push to the original repository.
  - **master**: Master is the name of the default branch that git creates for you when first creating a repository . In most cases, "master" means "the main branch”. It's the branch that represents production code, and that all other branches come from and generally eventually rejoin. This is the local `master` branch where you make changes and they are to be merged with the remote master branch i.e. `origin/master`.
  
  E.g. `git branch -a` - shows all the branches inside a git repository.
  ```console
  * master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  ```
  
  E.g. `git diff origin/master..master` or `git diff remotes/origin/master..master` - Both are the same thing, which says difference b/w remote `master` branch and my `master` branch
  
  #### Short difference:
  - `origin/master` is "where master was over there last time I checked"
  - `master` is "where master is over here based on what I have been doing"  
* ##### `git log --oneline --graph --color --all --decorate` - shows the entire graph of the repo.

## Activities
* ### Push a local folder to Github
  1. create a github repo.
  2. clone using **git** on bash-cmd in Ubuntu.
  3. get inside the repo using `$ cd <repo>`.
  4. add any files inside this local folder in computer.
  5. `$ git init` - initialize/reinitialize the git environment
  6. `$ git add .` - add all into local repo.
  7. `$ git commit -m "First commit"` - give name to the commit as "First commit".
  8. `$ git remote add origin <repo-url>` - sets the new remote. Add the github link to the commit
  9. `$ git remote -v` - verifies the new remote URL.
  10. `$ git push origin master`
  11. DONE!

  [Source](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)

* ### Clone a Submodule (from github) inside a Module (cloned from github repo)
  1. Open terminal (cmd or bash) in the directory (cloned repo)
  2. `$ git submodule add <repo-url.git> <custom-repo-name>`
  3. A file will be created with this content:
  `[submodule "eos-api"] path = eos-api url = https://github.com/oraclize/eos-api.git`
  4. DONE!

* ### Clone a folder from github repo.
  NOTE: Valid for Github repo. only.
  1. copy the url - https://github.com/EOSIO/eosio.cdt
  2. Modify the url - https://github.com/EOSIO/eosio.cdt/libraries
  3. Clone a folder from 
    - master branch: `svn checkout https://github.com/EOSIO/eosio.cdt/trunk/libraries`
    - other branch: `svn checkout https://github.com/EOSIO/eosio.cdt/branches/develop/libraries`
    
  [Source](https://stackoverflow.com/a/18194523/6774636)

## Troubleshoot
* `git` may not work properly on `bash-cmd` in directory of **removable disk**. So, use `git-bash` to use the bash commands.

## Git for Server
Setup a local directory as server (in place of Github) for Git repositories.
### Installation
* OpenSSH
  - Search "manage optional features" in the start menu.
  - "Optional features" >> "Add a feature" >> OpenSSH Server. Install it. And then it will be listed in the Optional features.
  - Now, **OpenSSH Server** & **OpenSSH Client** are installed.
  
### Setup

## Git for Excel - `xltrail`
### System
Currently, only available on Windows.

### Installation
* [Github]()
* Download & install setup file from [here](https://www.xltrail.com/client).
* open cmd and `git xltrail install` - Git xltrail requires a global installation once per-machine.
* Now, available terminal commands are: `git-xltrail`, `git-xltrail-diff`, `git-xltrail-merge`. <br/>
  All these are available in this installed folder: "F:\Softwares\Git xltrail". Also, these has been added in **PATH** of Environment variables.
  

### Setup
* Spreadsheet Compare - "C:\Program Files (x86)\Microsoft Office\Office15\DCF\SPREADSHEETCOMPARE.EXE" [Microsoft Office Professional Plus 2013]

### References [`xltrail`]
* https://www.xltrail.com/blog/git-diff-spreadsheetcompare


## References
* Udacity courses on Git & Github:
  - [Github & Collaboration](https://classroom.udacity.com/courses/ud456)
  - [Version Control with Git](https://classroom.udacity.com/courses/ud123)
  - [Optimize your Github profile](https://classroom.udacity.com/courses/ud247)
  - [How to use Git and Github](https://classroom.udacity.com/courses/ud775)
* Microsoft docs
  - [History in Git](https://docs.microsoft.com/en-us/azure/devops/repos/git/history?view=azure-devops)
* Git for Server
  - http://guides.beanstalkapp.com/version-control/git-on-windows.html
  - Book pages:
    + https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Getting-Git-on-a-Server
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Git-Daemon
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Smart-HTTP
    + https://git-scm.com/book/en/v2/Git-on-the-Server-GitWeb
    + https://git-scm.com/book/en/v2/Git-on-the-Server-GitLab
    + https://git-scm.com/book/en/v2/Git-on-the-Server-Third-Party-Hosted-Options
* [Set up Git server on your local network windows](https://medium.com/@piteryo7/how-to-set-up-git-server-on-local-network-windows-tutorial-7ec5cd2df3b1)
