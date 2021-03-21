# Flask Docker



## Objectives

To practice docker with flask application



## Execute

You can choose one of the following three methods



### Copy

This method copies the scripts to a docker container.

```shell
git clone https://github.com/respect5716/Flask_Docker.git
cd Flask_Docker

docker build -t flask -f Dockerfile1 .

docker run --name flask -p 5000:5000 flask
```



### Volume

This method mounts the files and directory to a docker container. So the code changes can be applied when using flask debug mode.

```shell
git clone https://github.com/respect5716/Flask_Docker.git
cd Flask_Docker

docker build -t flask -f Dockerfile2 .

docker run --name flask -p 5000:5000 -v ${PWD}:/app flask
```



### docker-compose

This method uses docker-compose. The function is same with Volume mode.

```shell
git clone https://github.com/respect5716/Flask_Docker.git
cd Flask_Docker
docker-compose up
```

