# Cheat Sheet

- Get the IP of the container
```shell
docker inspect app1 | grep Address
```
**OR**
```shell
docker container inspect [container_id] -f '{{.Address}}'
```
- To filter the `docker inspect` JSON output
```shell
docker container inspect [container_id] -f '{{.property.property}}'
```
**Useful example**: to know the status of the container
```shell
docker container inspect [container_id] -f '{{.State.Status}}'
```
# Guides
## Docker Volumes
### Three types of docker volumes
:one: Host volumes
```shell
docker run -v /path/on/host:/path/on/container
```
:two: Anonymous volumes
```shell
docker run -v /path/on/container
```
:three: Named volumes (Recommended)
```shell
docker run -v name:/path/on/container
```
### To mount a volume to a container

:one: Create a volume, and try to specify an expressive name. For example, i'll create a volume to persist `mysql` database data.
```shell
docker volume create mysql-volume
```
:two: Attach that volume to the mysql server container
```shell
docker run 
--name mysql-with-volume
-p 3306:3306
-e MYSQL_ROOT_PASSWORD=my-secret-pass,
OTHER_EVN_VARIABLE=other_value
-d
--mount
source=mysql-volume,
target=/var/lib/mysql
mysql
```
### Using a bind mount
We're usually using this method to sync files between the host and the container.
```shell
docker run 
--name mysql-with-volume
-p 3306:3306
-e MYSQL_ROOT_PASSWORD=my-secret-pa
-d
--mount
type=bind,
source="$(pwd)/directory-you-want-to-sync
target=/var/lib/mysql
mysql
```










