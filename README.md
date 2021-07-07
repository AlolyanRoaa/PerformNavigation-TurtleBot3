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

![01-Launch simulation](https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/01-Launch%20simulation.PNG)


when gazebo start open a new terminal and run the navigation node with the map we created earlier, and RViz window will open.


```bash
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

![02-Run navigation](https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/02-Run%20navigation.PNG)


![03-Run navigation](https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/03-Run%20navigation.PNG)


## How to control the robot in the simulation environment


We must estimate the initial pose before running the Navigation, Click the <img src="https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/07-2d%20pose%20estimate.PNG" width="125"> button in the RViz menu.


Click on the map where the robot is located, and then drag the arrow toward the direction where the robot is facing.


![04-after estimate the initial pose](https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/04-after%20estimate%20the%20initial%20pose.PNG)


now click the <img src="https://github.com/AlolyanRoaa/PerformNavigation-TurtleBot3/blob/main/06-2d%20nav%20gaol.PNG" width="125"> button in the RViz menu, then specify destination and direction.



## Demo



https://user-images.githubusercontent.com/85321139/124842158-99e66100-df97-11eb-931d-c73900bf9628.mp4



