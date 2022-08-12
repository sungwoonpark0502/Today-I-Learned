# GitHub

### Create a new repository on the command line
```command
git init
git commit -m "commit message"
git branch -M main
git remote add origin (url.git) # use "git remote -v" to check
git push -u origin master # origan = location of the git repository, master = name of the branch)
```

### Push an existing repository from the command line
```command
git remote add (url.git)
git branch -M main # (not sure if needed)
git push -u origin master # master could be diff depending on which branch you're in
```

### Update Chnage to GitHub
```command
git status # to see the changes
git add . # add every changes
OR
git add (name of the file) # only add the written file
git commit -m "update message" # commit
git push origin (name of the branch)
OR
git push -u origin (name of branch) # next time when pushing, use "git push" 
```

### Branch
```command
# Change to Other Branch
git checkout (name of branch I want to change to)

# Make New Branch
git checkout -b (name of new branch)

# Deleting Branch
git branch -d (name of the branch I want to delete)

# Display which Branch I'm in
git branch

# Merging
git diff (name of the branch you want to compare with)
git merge (name of the branch that you want to merge to)

```
### Undo
```command
# Undo Add Command
git reset
OR
git reset (name of the file)

# Undo Commit
git reset HEAD~1
```

### History of Commits
```command
git log
```

### Things to Know
* Can use git commit -am "message" when there are only modified files, no untracked files
