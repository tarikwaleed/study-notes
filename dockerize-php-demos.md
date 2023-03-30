### Docker Setup
First, Make sure that Docker is installed on your machine by running the following command
```shell
docker -v
```
If you havn't install docker already - but i'm sure you did from the docker course days- the docker documentation provides an easy to follow steps to set up docker on your local machine.


For ubuntu users , here you'll find instructions to install it on your machine.
[Follow this guide](https://docs.docker.com/engine/install/ubuntu/)

The installation  method i personally prefer is
[Here](https://docs.docker.com/engine/install/ubuntu/#install-from-a-package)

If you are using windows, as Dr. Noha always saying .. God bless your soul 😂 .
you can install Docker Desktop from here
[Docker Desktop Installation](https://docs.docker.com/desktop/)



### Steps
1. Clone the demo repo, or the repo of your intake track
```shell
git clone https://github.com/NohaAShehab/os43-assuit-php.git
```
2. cd into the directory
```shell
cd os43-assuit-php
```
3. Inside the project directory, create a new file named Dockerfile.
```shell
touch Dockerfile
```
4. open this file using your favourite text editor, i'm using vim but you can use VsCode or anything else.
```shell
vim Dockerfile
```
5. paste the following two lines in the file
```shell
FROM php:7.4-apache
COPY . /var/www/html/
```

6. Next, build the Docker image by running the following command from the project directory:
```shell
docker build -t php-day2-demos .
```
7. Once the image is built, you can start a container from it by running the following command:
```shell
docker run -p 8080:80 php-day2-demos
```
and that's it!
You can now access Day2 Demo application by visiting http://localhost:8080/validation/userstable.php in your web browser









