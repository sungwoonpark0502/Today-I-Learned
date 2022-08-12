# GitHub

Create a new repository on the command line
1. git init
2. git commit -m "commit message"
3. git branch -M main (not sure if needed)
4. git remote add origin (url.git) => use "git remote -v" to check
5. git push -u origin master (origan = location of the git repository, master = name of the branch)

Push an existing repository from the command line
1. git remote add (url.git)
2. git branch -M main (not sure if needed)
3. git push -u origin master(master could be diff depending on which branch ur in)


Update Change
1. git status = to see the changes
2. git add . = add every changes
3. git commit -m "update message" = commit
4. git push origin (name of the branch) OR git push -u origin (name of branch) = next time when pushing, use "git push"

Change to other branch
* git checkout (name of the branch I want to change to)
Make new branch
* git checkout -b (name of new branch)
Showing which branch I'm in
* git branch
Deleting branch
* git branch -d (name of the branch I want to delete)

Merging two branches
git diff (name of the branch you want to compare with) = shows what's been changed
git merge (name of the new branch)

solving merge conflict
* deleting the conflict markers

undo add
git reset
git reset (name of the file)
undo commit
git reset HEAD~1 

git log
=
