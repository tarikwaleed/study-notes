# Mount a Partition
- `sudo blkid`
- copy the id of the partition you want to mount
- `vim /etc/fsatb`
- put this line 
`UUID=68342E8E342E5F76 /media/tarikwaleed/Data ntfs defaults 0 0`
- check for errors:
    `sudo findmnt --verify`
- mount
    `sudo mount -a`
---
# Backup and restore dconf settings
**dump**
`dconf dump / > dconf-settings`
**reset**
`dconf reset -f /`
**restore**
`dconf load / < ~/dotfiles/dconf/dcon`

---
# Dash to Dock
- enable dash to dock extension
- from inside dconf:
- search for dash-to-dock
- enable autohide
- disable dock-fixed
---

