## Grant to usr/local
```shell
sudo chown -R username
```

## Setup wsl for development with azure config
1. Update linux
```shell
sudo apt-get update
sudo apt update
```
2. Install git
```shell
sudo apt-get update
sudo apt-get install git
```

3. Resolve git slow issue in wsl mnt path. add this function to ~/.bashrc
```shell
nano ~/.bashrc
function git() {   if [[ $(pwd -P) = /mnt/* ]]; then     git.exe "$@";   else     command git "$@";   fi; }
```
4. Configure git
```shell
git config --global credential.helper "/mnt/c/Users/<your username>/AppData/Local/Programs/Git/mingw64/bin/git-credential-manager.exe"
git config --global credential.https://dev.azure.com.useHttpPath true
git config --global user.name "<Your Name>"
git config --global user.email "<Your Email>"
```

5. Install telnet
```shell
sudo apt-get update && \
    apt-get install -y telnet
```
	
6. Install curl
```shell
sudo apt-get update && \
    apt-get install -y curl
```

7. Install Kubectl
```shell
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl


#chmod +x kubectl
#mkdir -p ~/.local/bin
#mv ./kubectl ~/.local/bin/kubectl
kubectl version --client
```

8. set KUBECONFIG environment variable to windows kube config path
```shell
nano ~/.bashrc
export KUBECONFIG="/mnt/c/Users/<your username>/.kube/config"
```

9. Install azure cli
```shell
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
sudo apt-get install azure-cli
az upgrade
sudo az aks install-cli
```

10. Install oh-my-fish
```shell
sudo apt-add-repository ppa:fish-shell/release-3
sudo apt update
sudo apt install fish

sudo vim /etc/pam.d/chsh
change "auth required pam_shells.so" -> "auth sufficient pam_shells.so"

sudo chsh -s $(which fish) $(whoami)

sudo vim /etc/pam.d/chsh
change "auth sufficient pam_shells.so" -> "auth required pam_shells.so"

curl -L https://github.com/oh-my-fish/oh-my-fish/raw/master/bin/install | fish
omf update
omf install bobthefish
```
