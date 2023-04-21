**Run odoo on docker containers**
```shell
docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo
-e POSTGRES_DB=postgres --name db postgres:13
```
```shell
docker run -t -p 8069:8069 --name odoo --link db:db odoo:15.0
-d odoo15
```

