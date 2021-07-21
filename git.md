# Git Commands


## Remove vscode from git:
```shell
git rm --cached .vscode
```

## Squash main branch:
```shell
git reset --soft Head~3
git commit -m 'Project Created'
git push --force origin main
```

## Add submodule:
```shell
git submodule add [url] [path](src/...)
```

## Submodule recursive:
```shell
git submodule update --init --recursive --remote
```

## After change password run below command:
```shell
git config --global credential.helper wincred
```

## Log on a single line
```shell
git log --pretty=oneline
```

## Log show indented branch-points and merges
```shell
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

## Delete Local Branch
```shell
git branch -D <branchname>
```

## Delete Remote Branch
```shell
git push origin --delete <branchname>
```

## Create branch from unpush commit on main
```shell
git checkout -b <branchname>
```

## Create upstream for a branch
```shell
git push -u origin <branchname>
```

## Stash (Temporary Commit)

- staged changes
```shell
git stash
```
- list stack-order of stashed file changes
```shell
git stash list
```
- write working from top of stash stack
```shell
git stash pop
```
- discard the changes from top of stash stack
```shell
git stash drop
```
