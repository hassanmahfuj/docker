# docker
Docker Easy Guide


# #1 Download a image from dockerhub
```
docker pull ubuntu
```


# #2 Show downloaded images
```
docker images -a
```

# #3 Run a image
```
docker run -it -d ubuntu
```
	-it Terminal interactive
	-d Run container as deamon (run in background)


# #4 Show running containers
```
docker ps -a
```
	-a See all containers

# #5 Login into container terminal
```
docker exec -it <container id> bash
```

# #6 Stop a container
```
docker stop <container id>
```

# #7 Force stop or plugout a machine
```
docker kill <container id>
```

# #8 Delete a container
```
docker rm -f <container id>
	-f Delete a running container
  #Delete all container
    docker rm -f $(docker ps -a -q)
```

# #9 Delete an image
```
docker rmi <image id>
```

# #10 Create a custom image
```
docker commit <image id> <new image name>
```

# #11 Run a container with port forwording
```
docker run -it -p  82:80 -d httpd
```

# #12 Run a container with specific name
```
docker run -it --name wordpress1 -p 8080:80 -d wordpress
```

# #DOCKER AUTOSTART UPDATE
```
docker update --restart unless-stopped wordpress
```
