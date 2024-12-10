# Run docker container for ros2 humble

- Build

`docker build -t ros-humble .`

-Run

`xhost + && docker run -it --name ros2 --net=host --privileged --env="QT_X11_NO_MITSHM=1" -e DISPLAY=$DISPLAY -eQT_DEBUG_PLUGINS=1 -v /tmp/.X11-unix:/tmp/.X11-unix --device /dev/video0:/dev/video0 -v $(pwd):/workspace ros-humble:latest bash`

-Start

`docker start ros2 && xhost + && docker exec -it --user $(id -u):$(id -g) ros2 bash`

- Docker compose

Note: the compose file relies on `LOCAL_USER_ID` and `LOCAL_GROUP_ID`. To add these values to the environment, run the following commands:

```bash
export LOCAL_USER_ID=$(id -u)
export LOCAL_GROUP_ID=$(id -g)
```

You may also add these to `~/.bashrc` to set them automatically when opening a terminal.

```bash
# cd to the directory where the docker-compose.yml file is located
ls # -> check if the docker-compose.yml file is in the current directory

docker compose up -d # Turn on the container

docker exec -it r2 bash # Enter the container

docker compose down # Turn off the container
```
