# TF2 introduction

To install example 
` sudo apt-get install ros-humble-rviz2 ros-humble-turtle-tf2-py ros-humble-tf2-ros ros-humble-tf2-tools ros-humble-turtlesim `

To run example


` ros2 launch turtle_tf2_py turtle_tf2_demo.launch.py `

To view frames

` ros2 run tf2_tools view_frames `


## Static publisher

Send static publisher 

` ros2 run tf2_ros static_transform_publisher --x x --y y --z z --yaw yaw --pitch pitch --roll roll --frame-id frame_id --child-frame-id child_frame_id `
