# Commands
```shell
find . -type f -exec cat {} \;
```
### To access VM from your local machine
**in Virtual Machine**
```shell
vim /etc/ssh/sshd_config
```
- edit the line
```shell
PermitRootLogin yes
```
- check VM ip address

```shell
ip addr show
```
**on your machine**

```shell
ssh root@{vm-ip-address}
```
---
### To know the distribution of the machine
```shell
cat /etc/os-release
```

