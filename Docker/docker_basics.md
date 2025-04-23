# Docker Basics

## Docker Worklow Commands

### Download a Docker image
	docker pull ros:dashing

### List downloaded Docker images
	docker images

### List Docker containers
	docker ps -a

### On the host, allow Docker to access your X11 display (so that applications like Rviz can use the display)
	xhost +local:root

### To create and start a Docker container (Shingo's way)
	docker container run --env DISPLAY=$DISPLAY -v /tmp/.X11-unix/:/tmp/.X11-unix/ --name container_name -it your_image_name

### To create and start Docker container with network interfaces support as well as GUI access:
	docker container run -it --network=host --env="DISPLAY" --env="QT_X11_NO_MITSHM=1" --volume "/tmp/.X11-unix:/tmp/.X11-unix:rw" --name container_name your_image_name 

### To start an already created Docker container 
	docker container start -ai container_test

### To connect to an already running Docker container (from a new terminal)
	docker exec -it container_test /bin/bash

### Create Docker image from container
	docker container commit container_test image_test

### "Export" the Docker image to a zipped folder
	docker save -o export_test.tar image_test

## Troubleshooting

### Container can not access X11 display
- Exit from the container and stop it.
- Give again Docker access to the X11 display:

		xhost +local:root

- Start the container.
