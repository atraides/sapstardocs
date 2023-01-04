# Personal Development Linux (Ubuntu)

## Install

## Configuration

### Update the system

``` shell
sudo apt update -y && sudo apt upgrade -y
```

### Install the required packages for pyenv

#### Ubuntu 22.04

``` shell
sudo apt-get update; sudo apt-get install make build-essential libssl-dev \
zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
```

### Install the required packages for chezmoi

``` shell
sudo apt install git
```

### Change the default shell to ZSH

``` shell
sudo apt install zsh
sudo chsh atraides -s /usr/bin/zsh
```

### Initialize the chezmoi environment

``` shell
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply atraides
```

### Install the local CA certificates

``` shell
sudo curl -Lo /usr/local/share/ca-certificates/sharpnet-root.crt http://smilpdch4000.sharpnet.sdac:32080/static/certs/sharpnet-root.crt
sudo curl -Lo /usr/local/share/ca-certificates/sharpnet-intermediate.crt http://smilpdch4000.sharpnet.sdac:32080/static/certs/sharpnet-intermediate.crt
sudo update-ca-certificates
```

### Install Bitwarden CLI

``` shell
curl -Lo bw-linux.zip https://vault.bitwarden.com/download/\?app\=cli\&platform\=linux
unzip bw-linux.zip
```

### Install Cargo

``` shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

### Instll MUC

``` shell
cargo install --git=https://github.com/nate-sys/muc
```