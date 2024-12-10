# Run docker container for ros2 humble
- Build 
 ` docker build -t ros-humble `

 -Run
 ` xhost + && docker run -it --name ros2 --net=host --privileged --env="QT_X11_NO_MITSHM=1" -e DISPLAY=$DISPLAY -eQT_DEBUG_PLUGINS=1 -v /tmp/.X11-unix:/tmp/.X11-unix --device /dev/video0:/dev/video0 -v $(pwd):/workspace ros-humble:latest bash `
