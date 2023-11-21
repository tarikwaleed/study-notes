# Basics
- [ ] show password astrisks
- Run
```
sudo visudo
```
- add `,pwfeedback` after `env_reset`at the first line
- [ ] mount Data partition
- [ ] change root password
```
sudo passwd root
```
**Firefox**
- [ ] sign-in to firefox
- [ ] setup extensions
- [ ] about:config -> layout.css.devPixelsPerPx=2.0

**Mount "Data" Partition**
- [ ] change font of the terminal
- [ ] Mount "Data" Partition
- Get the id of the partition
```shell
sudo blkid
```
- put this line at the end of `/etc/fstab` file
```shell
UUID=68342E8E342E5F76 /media/tarik/Data ntfs defaults 0 0
```
```shell
sudo mount -a
```

- [ ] Fix Read-only filesystem
```
To turn-off fast-boot on windows 10 do the following:
    Go to Control Panel.
    Click Power Options.
    Choose "what the power buttons do."
    Click "Change settings that are currently unavailable."
    Find and uncheck "Turn on fast startup."
    Save changes.
    Shutdown and boot linux.
```

---
# Apt
- [ ] `sudo apt-get update && sudo apt-get upgrade`

- [ ] Packages
```bash
sudo apt-get install dconf-editor git stow mlocate xclip tmux fish ruby-full rbenv sct unrar apache2 gnome-shell-extension-manager -y
```

---
# Git
- [ ] configure git
```shell
git config --global user.name "tarikwaleed"
git config --global user.email "tarikwaleed.tech@gmail.com"
```
- [ ] setup `ssh` with bitbucket and github
- Run
```shell
ssh-keygen -t ed25519 -C tarikwaleed.tech@gmail.com
```
- add the public key to github or bitbucket keys

- [ ] clone repos
```
git clone git@github.com:tarikwaleed/study-notes.git /home/tarik/study-notes
```
```
git clone git@github.com:tarikwaleed/dotfiles.git /home/tarik/dotfiles
```

```
git clone git@github.com:tarikwaleed/secrets.git /home/tarik/secrets
```
```
git clone git@github.com:tarikwaleed/pk-amana-design-documents.git /home/tarik/work/pk/docs
```
```
git clone git@bitbucket.org:pk-amana/backend.git /home/tarik/work/pk/backend
```
```
git clone git@bitbucket.org:pk-amana/package.git /home/tarik/work/pk/package
```
---



---
# Desktop Environment
- [ ] Restore dconf 
```shell
dconf reset -f /
```
```shell
dconf load / < ~/dotfiles/dconf/dconf
```
---




# Ubuntu Software Center
- [ ] slack
- [ ] Vscode
- [ ] Teams for linux
- [ ] Gnome Tweaks







# Terminal Emulator
- [ ] Install all fonts in `~/dotfiles/fonts`
- [ ] stow fonts
- [ ] Install all fonts
- [ ] font: cousine18, theme:Tango Light
---





# Tmux
- [ ] install tpm
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
[More Details](https://github.com/tmux-plugins/tpm)
- [ ] install tmux-powerline 
```bash
git clone https://github.com/erikw/tmux-powerline.git ~/.local/share/tmux-powerline
```
[More Details](https://github.com/erikw/tmux-powerline)
- [ ] stow tmux
- [ ] Remove some files before stow
```bash
rm ~/.local/share/tmux-powerline/themes/default.sh
rm ~/.local/share/tmux-powerline/segments/time.sh
rm ~/.local/share/tmux-powerline/segments/date.sh
```
- [ ] stow tmux-powerline
---




# Fish
- [ ] make fish the default shell
```shell
chsh -s /usr/bin/fish
```
- [ ] reboot, then make sure it's been changed
```shell
echo $SHELL
```     
- [ ] Run
```shell
rm ~/.config/fish/config.fish
rm -rf ~/.config/fish/functions
```

- [ ] stow fish
- [ ] install some gem packages
```shell
sudo gem install colorls tmuxinator
```
- [ ] stow tmuxinator
- [ ] stow colorls
- [ ] install fisher, nvm, npm, node
```shell
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```
```shell
fisher install jorgebucaran/nvm.fish
```

```shell
nvm install lts
```


```shell
set --universal nvm_default_version v16.15.0
```
[More Details](https://rmdhnreza.my.id/install-nvm-on-fish-shell/)
- [ ] reboot
- [ ] install tldr
```shell
sudo npm install  -g tldr
```
- [ ] Install some Fisher Packages
```shell

fisher install mattmc3/cd-ls.fish edc/bass sentriz/fish-pipenv jethrokuan/z 
```
- [ ] install omf
```shell
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
```
- [ ] change omf theme
```shell
omf install agnoster
```

```shell
omf theme agnoster
```
---




# Neovim
- [ ] install nvim
- Download from [Here](https://github.com/neovim/neovim/releases)
- then extract it at `Downloads`

- [ ] run
```shell
stow neovim
```

- [ ] Run
```shell
nvim -c PackerSync

```

---


# MySQL
- [ ] install
[Guide](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)
**steps**
```shell
sudo apt update
```
```shell
sudo apt install mysql-server
```
```shell
sudo systemctl start mysql.service
```
```shell
sudo mysql
```
```shell
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
change 'password' with your password, then `exit`

```shell
sudo mysql_secure_installation
```
```shell
CREATE USER 'tarikwaleed'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
```shell
GRANT CREATE, ALTER, DROP, INSERT, UPDATE, INDEX, DELETE, SELECT, REFERENCES, RELOAD on *.* TO 'tarikwaleed'@'localhost' WITH GRANT OPTION;
```
```shell
mysql -u tarikwaleed -p
```
- [ ] mysql-shell
[Guide](https://dev.mysql.com/doc/mysql-shell/8.0/en/mysql-shell-install-linux-quick.html)
**steps**
```shell
sudo apt-get update
```
```shell
sudo dpkg -i /media/tarikwaleed/Data/linux-tools/tarballs/mysql-apt-config_w.x.y-z_all.deb
```

```shell
sudo apt-get update
```
```shell
sudo apt-get install mysql-shell
```


---
# Apache
```shell
sudo apt install apache2
sudo ufw app list
sudo ufw allow 'Apache'
```
**Setting up a VirtualHost**



---


# PHP
```shell
sudo add-apt-repository ppa:ondrej/php
```
```shell
sudo apt install --no-install-recommends php8.1
```
```shell
sudo apt-get install -y php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath
```




**Setting up Composer**
```shell
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e21205b207c3ff031906575712edab6f13eb0b361f2085f1f1237b7126d785e826a450292b6cfd1d64d92e6563bbde02') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar /usr/local/bin/composer
```


---

# Python

- Python3 is already installed

**pip3**
```shell
sudo apt-get install python3-pip
```

**Virtualenv**
```shell
pip3 install virtualenv
```
```shell
virtualenv --version
```
```shell
virtualenv project-name-env
```
```shell
source project-name-env/bin/activate.fish
```













# MongoDb
```shell
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
```
```shell
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```
```shell
sudo apt update
```
```shell
sudo apt install mongodb-org
```
```shell
systemctl status mongod
```

```shell
rm /tmp/mongodb-27017.sock
```
---




# npm packages
```shell
npm install -g express-generator nodemon
```
[guide](https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04)

---


# Postman
- [ ] Installation
```shell
curl https://gist.githubusercontent.com/SanderTheDragon/1331397932abaa1d6fbbf63baed5f043/raw/postman-deb.sh | sh
```
---



# Vagrant
- [ ] install vagrant
>:bulb: check that it's located in the right path as defined in fishconfiguration /media/tarikwaleed/Data/linux-tools/tarballs/opt/vagrant/bin
- [ ] Download vagrant-vmware-utility .. it's already downloaded at /media/tarikwaleed/Data/linux-tools/tarballs
[Guide](https://developer.hashicorp.com/vagrant/docs/providers/vmware/vagrant-vmware-utility)
- [ ] install the previously installed plugin
```shell
vagrant plugin install vagrant-vmware-desktop
```
---



# Docker
- [ ] Download the 7 .deb packages(amd64)
[Download from here](https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/)
- [ ] Extract them using `sudo dpkg -i`, in the following order:
- docker-ce-cli
- container.io
- docker-ce_
- docker-compose-plugin
- docker-scan-plugin
- docker-ce-rootless
- docker-buildx-plugin
- [ ] to use docker without `sudo`
```shell
sudo gpasswd -a username docker
```
```shell
sudo service docker restart 
```

---
# Httpie
```shell
curl -SsL https://packages.httpie.io/deb/KEY.gpg | apt-key add -
```
```shell
curl -SsL -o /etc/apt/sources.list.d/httpie.list https://packages.httpie.io/deb/httpie.list
```
```shell
apt update
```
```shell
apt install httpie
```


# VmWare Player
- [ ] Download
[Guide](https://customerconnect.vmware.com/en/downloads/details?downloadGroup=WKST-PLAYER-1700&productId=1377&rPId=97014)   

- [ ] Add execution permision to the dowonloaded `.bundle` file

```shell
sudo chmod a+x VMware-Player-6.0.3-1895310.x86_64.bundle
```
- [ ] execute the .bundle file
```shell
sudo ./VMware-Player-6.0.3-1895310.x86_64.bundle
```
## If you ran into problems
### Problem1
>"Cannot open /dev/vmmon: No such file or directory" error when powering on a VM (2146460)

**solution**
[Guide](https://kb.vmware.com/s/article/2146460)

```shell
openssl req -new -x509 -newkey rsa:2048 -keyout MOK.priv -outform DER -out MOK.der -nodes -days 36500 -subj "/CN=VMware/"
```
```shell
sudo /usr/src/linux-headers-(uname -r)/scripts/sign-file sha256 ./MOK.priv ./MOK.der $(modinfo -n vmmon)
```
```shell
sudo /usr/src/linux-headers-(uname -r)/scripts/sign-file sha256 ./MOK.priv ./MOK.der $(modinfo -n vmnet)
```

```shell
sudo mokutil --import MOK.der
```


### Problem2
[Guide](https://communities.vmware.com/t5/VMware-Workstation-Player/ubuntu-22-04-install-vm-workstation-error/td-p/2905277)
