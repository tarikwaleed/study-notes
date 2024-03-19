- [ ] create a `creds` entry:
**on your machine**

- Run
```shell
touch ~/secrets/creds/new_machine_name
```
- echo the machine's ip address in the file
- create an alias for the  machine name in `config.fish`
- [ ] setup tmuxinator window for accessing this machine

- [ ] copy bash aliases
- On the new machine

```shell
wget -O - https://github.com/tarikwaleed/dotfiles/raw/master/bash_aliases >> ~/.bashrc
```
```shell
source ~/.bashrc
```

- [ ] setup docker
```shell
mkdir ~/docker-packges && cd ~/docker-packages
```
```shell
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/containerd.io_1.2.13-2_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-buildx-plugin_0.10.2-1~ubuntu.20.04~focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce-cli_19.03.10~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce-rootless-extras_20.10.0~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce_19.03.10~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-compose-plugin_2.10.2~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-scan-plugin_0.12.0~ubuntu-focal_amd64.deb
```
- [ ] Extract them using `sudo dpkg -i`, in the following order:
- docker-ce-cli
- container.io
- docker-ce_
- docker-compose-plugin
- docker-scan-plugin
- docker-ce-rootless
- docker-buildx-plugin

- [ ] configure ssh access
- create ssh key for the machine
```shell
ssh-keygen -t ed25519 -C machine-name@email.com
```

- Run
```shell
cat ~/.ssh/id_ed25519.pub | copy
```
- add your public key to `~/.ssh/authorized_keys` file on the new machine

**copy `.env` file using scp**
```shell
scp /path/to/local/.env username@remote-server:/path/to/remote/directory
```