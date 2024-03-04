# Export GitLab bundle from GitLab

1) Go to Project Settings -> Export project -> Export project / Download export
2) Get exported TAR file
3) Unzip it and get three files : `project.bundle`, `project.json` and `VERSION`

# Convert GitLab bundle to local git repository

### Set up Git repository from GitLab bundle
```
$ mkdir project-name
$ git clone --mirror project.bundle project-name/.git
$ cd project-name
$ git init
$ git checkout
```

### Push Git repository to remote
```
$ git checkout master // reduce effort for changing remote project default branch later
$ git remote -v // double check existing remote origin before changes
$ git remote remove origin
$ git remote add origin {target git project path, recommended in ssh format}
$ git push --all origin
```
