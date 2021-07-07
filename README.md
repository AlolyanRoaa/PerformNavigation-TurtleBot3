# Perform Navigation on TurtleBot3


This is documentation of how to perform navigation on TurtleBot3 burger robot.This document is completely dependent on the previous document (Creating-a-map-using-Turtlebot3-and-SLAM), it is recommended to reviewing it before starting.


so, please [click here](https://github.com/AlolyanRoaa/Creating-a-map-using-Turtlebot3-and-SLAM) to go to its repository.


## Outline


- Launch simulation world and Run navigation node.
- How to control the robot in the simulation environment.
- Demo


## Launch simulation world and Run navigation node


*Note: These instructions have been done on `Ubuntu 18.04.5 LTS bionic` and `ROS melodic` .* 

After making sure of saving the map that we created in the previous repository (Creating-a-map-using-Turtlebot3-and-SLAM).


open a new terminal and set TurtleBot3 model parameter as burger and run gazebo by using these commands.


```bash
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

![1]()


when gazebo start open a new terminal and run the navigation node with the map we created earlier, and RViz window will open.


```bash
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

![2]()


![]()


## How to control the robot in the simulation environment


We must estimate the initial pose before running the Navigation, Click the **2D Pose Estimate** button in the RViz menu.


Click on the map where the robot is located, and then drag the arrow toward the direction where the robot is facing.


now click the **2D Nav Goal** button in the RViz menu, then specify destination and direction.

![]()


## Demo


![]()













