- To filter the `docker inspect` JSON output
```shell
docker container inspect [container_id] -f '{{.property.property}}'
```
**Useful example**: to know the status of the container
```shell
docker container inspect [container_id] -f '{{.State.Status}}'
```

**try out those commands**
```shell
FROM ubuntu:latest
RUN mkdir /omar-dir/
# WORKDIR /omar-dir
RUN touch omar2.txt
RUN apt-get update
RUN apt-get install -y --no-install-recommends mysql-clientRUN rm -rf /var/lib/apt/lists/*USER OMAR
RUN touch /omar2.txt
RUN echo "this is word from docker file." >> omar2.txt
RUN cat /omar2.txt
COPY ./omar.txt .
RUN cat omar-dir/omar.txtADD https://drive/mydrive/omar.txt /# ENTRYPOINT ["mysql"]
```
```shell
docker container  run --detach --name mariadb-container --env MARIADB_ROOT_PASSWORD=1234  mariadb:latest
```
```shell
docker container run -d --name mariadb-container -v /salamaNew:/var/lib/mysql -e MARIADB_ROOT_PASSWORD=1234 mariadb:latest
```
```shell
docker container run -d --name mywebsite2 -p 80:80 -v /path:/usr/share/nginx/html nginx 
```




