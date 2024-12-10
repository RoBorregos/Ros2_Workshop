# Source

 For source the ros2 environment 

` source /opt/ros/humble/setup.bash `

Add source command into .bashrc

` echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc `

Check environment variables

` printenv | grep -i ROS `

For source project

` source install/setup.bash `

# ROS2 Variables

Ros domain for share nodes

` export ROS_DOMAIN_ID=<your_domain_id> `

Ros Localhost

` export ROS_LOCALHOST_ONLY=1 `

# ROS2 Commands

For search executables in package

` ros2 pkg executables turtlesim `

To run node

` ros2 run <pkg_name> <node_name> `

List different active structures

``` 
ros2 node list
ros2 topic list
ros2 service list
ros2 action list
```
