# Git

* __git init__ = initialize repository
* __git status__ = check the status of the repo(repository)
* __git add__ = add the file to the staging area
  * Used when there has been a change or a new file
  * type: git add (name of the file)
  * type2: git add .
    * adds all the files
* __git commit -m__ = making commits
  * type: git commit -m "Commit message"
* __git log__ = shows the history of commits
* __ git checkout__ = go back to the certain commit/branch
  * type1: git checkout (commit-hash)
  * commit-hash can be seen from git log
  * type2: git checkout master
    * will take back to master branch
  * type3: git checkout (name of the branch)
    * will go the specified branch
* __git branch__ = shows which branch I am in
* __git branch (name of the branch)__ = create new branch
* __git merge__ = merge one branch to the other
  * usually used when someone elses code looks better and want to change my original code
  * type: git merge (name of the branch)


1. git init => to make a new repo
2. git status => see the changes or new files added
3. git add . => add all the files
4. git commit -m "changed" => commit
