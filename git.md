* Remove vscode from git:
```shell
	git rm --cached .vscode
```

* Squash main branch:
```shell
	git reset --soft Head~3
	git commit -m 'Project Created'
	git push --force origin main
```

  * Add submodule:
```shell
	git submodule add [url] [path](src/...)
```

* Submodule recursive:
```shell
	git submodule update --init --recursive --remote
```

* After change password run below command:
```shell
	git config --global credential.helper wincred
```