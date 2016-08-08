# Node

## setup

### nvm
https://github.com/creationix/nvm
```bash
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.31.4/install.sh | bash
```
Do not forget to close and reopen your terminal to start using nvm.


### jq
 - OSX
```bash
brew install jq
```

- Ubuntu
```bash
sudo apt-get install jq
```

https://stedolan.github.io/jq/download/

### install node and npm
cd to one of the project directories and install the respective node and npm versions (should be the same across projects):
```bash
git@github.com:upfrontIO/livingdocs-server.git
cd livingdocs-server
nvm install "$(jq -r '.engines.node' package.json)"
npm install -g npm@"$(jq -r '.engines.npm' package.json)"
nvm alias default $(node -v)
```
