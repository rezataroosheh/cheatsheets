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
