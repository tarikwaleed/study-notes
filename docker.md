>:bulb: Docker containers are not like VMs; they are designed to run an application. When the application terminates, so does the container.

- To filter the `docker inspect` JSON output
```shell
docker container inspect [container_id] -f '{{.property.property}}'
```
**Useful example**: to know the status of the container
```shell
docker container inspect [container_id] -f '{{.State.Status}}'
```