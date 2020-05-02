# docker-commands

```shell
docker ps # list all running containers
docker ps -a	# list all containers including both running and non-running one
docker stop container_id # stop a container
docker rm container_id # remove a container
docker images # list images
docker rmi image_id/image_name # remove images
docker pull image_name # download images 
docker run -d image_name # run a container in background
docker exec container_id command # run command in the container
docker run --name new_name image # run and rename a container
docker run -it image # enter input and terminal mode for container
docker run -d image # run container in background
docker rm -f container # remove a running container
```
* To delete the image, we have to delete all dependent containers first

该项目在pipenv的虚拟环境下，使用Dockerfile里的参数来创建docker image。
docker build -t simple-django-on-docker -f Dockerfile .

使用生成的image来创建container
docker run --name babala -d -p 8888:8888 docker_django
生成了在后台运行的docker 并且将主机端口8888映射到了container的端口8888

