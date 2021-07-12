# Summary

In this project, through the simulation of gazebo, the Baxter robot is operated to identify coke can loaded based on point cloud, grab and drop off the coke can four times to make a square.

## Quick start

```
catkin_make -j4
source devel/setup.bash
roslaunch baxter_variations baxter_kinect.launch
```
Baxter, coke_can and table are loaded in gazebo.
```
roslaunch coordinator coord_vision_manip_coke.launch
```
Rviz is loaded and the arms are moving to pre pose.
Object finder action server, object grabber action server, arm planner and  object manipulation properties are loaded. 
```
rosrun coordinator grab_and_drop
```
Baxter finds the table top and the coke can. Having known the pose of coke can, baxter moves its right arm to grab and drop off the coke can four times so that it seems like a square.

## Overview
The operation effect is shown in the figure below
<img src="illustration.png" alt="illustration">
You can get the running video through the video link: https://www.youtube.com/watch?v=oZbIIizFcgA

## FAQ
1 - What is the recommended operating environment for the project?
- It is recommended to run in Ubuntu 20.04, and ROS noetic.

2 - In addition to the code of the home page of this project, what other repositories are needed?
- Yes, this project is based on the existing code package for secondary development. You need to download the following code at the same time and replace the original code package with the code of this project.
https://github.com/wsnewman/learning_ros_external_packages_noetic.git
https://github.com/wsnewman/learning_ros_noetic.git
