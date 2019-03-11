# Git & Github Essentials
## Commands
* ##### `git init` - intialize git within a non-Github folder (i.e. a local folder)
* ##### `git add .` - add all the files, folders inside a repo. for commit.
* ##### `git add ./find.cpp` - adding a `.cpp` file for commit.
* ##### `git commit -m "Add a comment"` - commit to the master branch.
* ##### `git push origin master` - pushing the added commit to the remote url
* ##### `git remote -v` - verify the url of the repo.
* ##### `git clone <repo-url>` - clone a github repository from link like - https://github.com/EOSIO/eosio.cdt
* ##### `git clone <repo-url> <your-repo-name>` - clone a github repository with a custom name.
* ##### `git clone -b <branch> <remote_repo>` - clone a specific branch (only) of github repo.
  E.g. - `git clone -b v1.x --single-branch https://github.com/gabime/spdlog.git` [git v1.7.10 and later]
* ##### `svn checkout <repo-url>` - clone a github repo.
* ##### `svn checkout <modified-repo-url>` 
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

## References
* Udacity courses on Git & Github:
  - [Github & Collaboration](https://classroom.udacity.com/courses/ud456)
  - [Version Control with Git](https://classroom.udacity.com/courses/ud123)
  - [Optimize your Github profile](https://classroom.udacity.com/courses/ud247)
  - [How to use Git and Github](https://classroom.udacity.com/courses/ud775)
