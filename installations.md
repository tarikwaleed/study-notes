# MongoDb

```
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
```

```
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```

```
sudo apt update
```

```
sudo apt install mongodb-org
```

**Managing MongoDb**

`sudo systemctl status mongod`

`sudo systemctl stop mongod`

`sudo systemctl start mongod`

`sudo systemctl restart mongod`

`sudo systemctl disable mongod`

`sudo systemctl enable mongod`

---

# How to uninstall a .deb Package
- get the name of the package
```shell
dpkg --info /path/file.deb
```

- Purge it!
```shell
sudo dpkg -P package_name
```

# How to uninstall a snap package

```shell
sudo snap remove --purge pkg_name
```