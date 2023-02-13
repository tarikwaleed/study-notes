# Basics
- [x] show password astrisks
- [x] mount Data partition
**Firefox**
- [x] sign-in to firefox
- [x] setup extensions
- [x] about:config -> layout.css.devPixelsPerPx=2.0
---
# Aptitude
- [x] `sudo apt-get update && sudo apt-get upgrade`

- [x] Packages
```bash
sudo apt-get install dconf-editor git stow mlocate xclip tmux fish ruby-full rbenv -y
```
---
# Desktop Environment
- [x] Restore dconf 
```shell
dconf reset -f /
```
```shell
dconf load / < ~/dotfiles/dconf/dcon
```
- [x] Sanity Checks
---
# Ubuntu Software Center
- [x] slack
- [x] Vscode
- [x] Teams for linux
- [x] Gnome Tweaks

---
# Git
- [x] configure git
- [x] clone dotfiles
- [x] create new github access token
---
# Terminal Emulator
- [x] Install a nerd font from dotfiles (Cousine)
- [x] font: cousine18, theme:Tango Light
# Tmux
- [x] install tpm
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
[More Details](https://github.com/tmux-plugins/tpm)
- [x] install tmux-powerline 
```bash
git clone https://github.com/erikw/tmux-powerline.git ~/.local/share/tmux-powerline
```
[More Details](https://github.com/erikw/tmux-powerline)
- [x] stow tmux
- [x] Remove some files before stow
```bash
rm ~/.local/share/tmux-powerline/themes/default.sh
rm ~/.local/share/tmux-powerline/segments/time.sh
rm ~/.local/share/tmux-powerline/segments/date.sh
```
- [x] stow tmux-powerline
# Fish
- [x] make fish the default shell
```shell
chsh -s /usr/bin/fish
```
- [x] reboot, then make sure it's been changed
```shell
echo $SHELL
```     
- [x] make sure that fish stow directory contains only user-generated files
- [x] stow fish
- [x] install some gem packages
```shell
sudo gem install colorls tmuxinator
```
- [x] stow tmuxinator
- [x] stow colorls
- [x] install fisher, nvm, npm, node
```shell
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
fisher install jorgebucaran/nvm.fish
nvm install lts
set --universal nvm_default_version v16.15.0
```
[More Details](https://rmdhnreza.my.id/install-nvm-on-fish-shell/)
- [x] reboot
- [x] install tldr
```shell
npm install  -g tldr
```
- [x] Install some Fisher Packages
```shell

fisher install mattmc3/cd-ls.fish edc/bass sentriz/fish-pipenv jethrokuan/z 
```
- [x] install omf
```shell
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
```
- [x] change omf theme
```shell
omf install agnoster
omf theme agnoster
```
---
# Neovim
- [x] install nvim
```shell
sudo dpkg -i /media/tarikwaleed/Data/linux-tools/tarballs/nvim-liux64.deb
```

- [x] stow neovim
- [x] nvim -c PackerSync
---
# MongoDb
- [ ] Insall
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
- [ ] Download the 6 .deb packages(amd64)
[Download from here](https://download.docker.com/linux/ubuntu/dists/focal/pool/stable/amd64/)
- [ ] Extract them using `sudo dpkg -i`
---
# MySQL
- [ ] install
[Guide](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)
- [ ] mysql-shell
[Guide](https://dev.mysql.com/doc/mysql-shell/8.0/en/mysql-shell-install-linux-quick.html)
---
# VmWare Player
- [ ] ownload
[Guide](https://customerconnect.vmware.com/en/downloads/details?downloadGroup=WKST-PLAYER-1700&productId=1377&rPId=97014)   
- [ ] if ran into problems
[Guide](https://kb.vmware.com/s/article/2146460)
[Guide](https://communities.vmware.com/t5/VMware-Workstation-Player/ubuntu-22-04-install-vm-workstation-error/td-p/2905277)