# Git

### Initialize Repository
```command
git init
```
### Check Status
```command
git status
```
### Add File(s) to the Staging Area
```command
# Used when there has been a change or a new file
git add . # adds all the changed/new files
OR
git add (name of the file) # only adds the specific file
```
### Making Commits
```command
git commit -m "commit message"
OR
git commit -am "commit message" # only when modified, no untracked file
```
### History of Commits
```command
git log
```
### Branch
```command
# Go Back to a certain branch
git checkout (commit hash)
OR
git checkout (name of a branch)

# Creating New Branch
git checkout -b (name of the new branch)

# Show which branch I'm In
git branch

# Merging Branches
git merge (name of the branch)
```

### Show which branch I'm In
```command
git branch
```
### Merging Branches
```command
git merge(name of the branch)
```
