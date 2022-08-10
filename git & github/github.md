# GitHub

Create a new repository on the command line
1. git init
2. git commit -m "commit message"
3. git branch -M main (not sure if needed)
4. git remote add origin (url.git)
5. git push -u origin master

Push an existing repository from the command line
1. git remote add (url.git)
2. git branch -M main (not sure if needed)
3. git push -u origin master(master could be diff depending on which branch ur in)


Update Change
1. git status = to see the changes
2. git add . = add every changes
3. git commit -m "update message" = commit
4. git push = push to github

Pull
* git pull origin master 
* origin is the url


* git remote -v = will list the remote I have

If I want to get a code on other's github, I can clone it
1. git status (if in made branch, then back out using "cd .."
2. mkdir (name of the new directory)
3. cd (name of the new directory) = changes to the new directory
4. git clone (url of the github code that we want to copy)


When I want to make chagnes to the open source code on github
1. Click Fork
2. git clone (url of the forked repo)
3. ls
4. cd (return value from ls)/
5. ls
6. Now make changes to the file
7. git add .
8. git commit -m "message"
9. git remote -v = check
10. git push -u origin master

Pull Request
 * If I want to let the original developer the change I made
