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
- [ ] make fish the default shell
```shell
chsh -s /usr/bin/fish
```
- [ ] reboot
- [ ] make sure that fish stow directory contains only user-generated files
- [ ] stow fish
- [ ] install colorls
```shell
sudo gem install colorls
```
- [ ] install tmuxinator
```shell
sudo gem install tmuxinator
```
- [ ] stow tmuxinator
- [ ] stow colorls
- [ ] install fisher, nvm, npm, node
```shell
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
fisher install jorgebucaran/nvm.fish
nvm install lts
set --universal nvm_default_version v16.15.0
```
[More Details](https://rmdhnreza.my.id/install-nvm-on-fish-shell/)
- [ ] reboot
- [ ] install tldr
```shell
npm install  -g tldr
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
omf theme agnoster
```
---
# Neovim
- [ ] download latest nvim.deb in ~/Downloads/tarballs
- [ ] stow neovim
- [ ] vim -c PackerSync
- [ ] install stylua
---
# Vagrant
- [ ] install vagrant
- [ ] download vagrant-vmware-utility .. it's already downloaded at /media/tarikwaleed/Data/linux-tools/tarballs
- [ ] install the previously installed plugin
---
# Docker
- [ ] Download the 6 .deb packages(amd64)
- [ ] xtract them
---
# MySQL
- [ ] install
- [ ] mysql-shell
---
# VmWare Player
- [ ] ownload
- [ ] f ran into problems
- [ ] f ran into problems
---
# MongoDb
- [ ] ttps://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04
---
# Postman
- [ ] nstallation