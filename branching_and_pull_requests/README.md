# Creating a branch
```
git clone git@github.com:nancy134/realty-app.git
git checkout master
git pull
git checkout -b test-branch 
```
# Committing code changes to the branch
```
git status (to see what files change)
git add README.md (to commit the file README.md)
git add . (to commit all files)
git commit -m "A commit comment"
git push --set-upstream origin test-branch (after this 'git push' should work for future pushes)
```
# Creating a pull request
```
Go to https://github.com/nancy134/user-service
Select "Pull requests"
Select "Compare & pull request"
Select "Create pull request"
```

