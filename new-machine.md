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
mkdir ~/docker-packages && cd ~/docker-packages
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

- [ ] configure git
```shell
git config --global user.name "new_machine_name"
git config --global user.email newmachine@gmail.com
```

**copy `.env` file using scp**
```shell
scp ./app/.env.app.production ubuntu@(cat ~/secrets/creds/zubi-instance-ip):/home/ubuntu/zubi-law-django/app
```
**To install `nodejs` on the server**
```shell
cd ~
curl -sL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh
```
```shell
sudo bash nodesource_setup.sh
```
```shell
sudo apt install nodejs
```
```shell
node -v
```

**To install `python3.10` on the server**
```shell
sudo add-apt-repository ppa:deadsnakes/ppa
```
```shell
sudo apt install python3.x #change x to the python version you like to install
```
```shell
apt install python3-pip
```
```shell
pip install pipenv
```




**To install `pm2`**
```shell
npm install pm2 -g
```


**To run `django` app with `pm2`**

```json
{
    "apps": [
        {
            "name": "zubi-django-pm2",
            "script": "/root/zubi-law-django/app/src/manage.py",
            "args": [
                "runserver",
                "0.0.0.0:8000"
            ],
            "exec_mode": "fork",
            "instances": "1",
            "wait_ready": true,
            "autorestart": false,
            "max_restarts": 5,
            "interpreter": "/root/.local/share/virtualenvs/app-KpfsMCDG/bin/python"
        }
    ]
}

```
