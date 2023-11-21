- [ ] setup docker
```shell
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/containerd.io_1.2.13-2_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-buildx-plugin_0.10.2-1~ubuntu.20.04~focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce-cli_19.03.10~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce-rootless-extras_20.10.0~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-ce_19.03.10~3-0~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-compose-plugin_2.10.2~ubuntu-focal_amd64.deb
wget https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/docker-scan-plugin_0.12.0~ubuntu-focal_amd64.deb
```

- [ ] create a `creds` entry:
- Run
```shell
touch ~/secrets/creds/new_machine_name
```
- echo the machine's ip address in the file
- create an alias for the  machine name in `config.fish`
- [ ] configure ssh access
- create ssh key for the machine
```shell
ssh-keygen -t ed25519 -C tarikwaleed.tech@gmail.com
```

- Run
```shell
cat ~/.ssh/id_ed25519.pub | copy
```
- add your public key to `~/.ssh/authorized_keys` file on the new machine
- [ ] copy bash aliases
    >:bulb:use `wget` to download the file in `~/.bashrc`

- On the new machine

```shell
wget -O - https://github.com/tarikwaleed/dotfiles/raw/master/bash_aliases >> ~/.bashrc
```
