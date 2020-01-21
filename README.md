# Home Service Robot Project

## Introduction
-----

The goal of this project is creating a full home service robot capable of navigating to pick up and deliver virtual objects.
 
![Gazebo](https://github.com/lucastakara/Home_Service_Robot/blob/master/images/home_service.png?raw=true)
## Concepts
---
The following concepts will be explored in this project:
- Gazebo models and world-building 
- Gazebo plugins
- URDF6
- XML
- ROS essentials: Publishers, Subscribers and Services
- C++
- Monte Carlo Localization
- ROS AMCL package
- ROS Navigation package

## Getting Started
----
The following items are required in order to visualize and create the project:
 
#### Installation Instructions:

#### Prerequisites / Dependencies 

- Gazebo >= 7.0

- ROS Kinetic

- gcc/g++ >= 5.4

- Linux: gcc / g++ is installed by default on most Linux distros

- ROS Navigation package

- [Linux Ubuntu 16.04.6 LTS (Xenial Xerus)](http://releases.ubuntu.com/16.04/)
- [Gazebo](http://gazebosim.org/tutorials?tut=install_ubuntu&cat=install) 
- [Robot Operating System](http://wiki.ros.org/kinetic/Installation/Ubuntu) (ROS)

Once these components are installed, you need to create a Catkin Workspace:


- `$ mkdir -p catkin_ws/src`

- `$ cd catkin_ws/src`

- `$ catkin_init_workspace`

Download/clone the repository:

- `$https://github.com/lucastakara/Home_Service_Robot.git`

Then, navigate up to the top-level catkin workspace directory and build the executables:

- `cd ..`
- `catkin_make` 
- `rosdep -i install gmapping -y`
- `rosdep -i install turtlebot_teleop -y`
- `rosdep -i install turtlebot_rviz_launchers -y`
- `rosdep -i install turtlebot_gazebo -y`

Next, you can open Gazebo with the robot in it:

- `$ source devel/setup.bash`
- `$ cd scripts`
- `$ chmod +x home_service.sh`
- `$ ./home_service.sh`


### Packages Explanation
----

- **gmapping**: With the gmapping_demo.launch file, you can easily perform SLAM and build a map of the environment with a robot equipped with laser range finder sensors or RGB-D cameras.

- **turtlebot_teleop**: With the keyboard_teleop.launch file, you can manually control a robot using keyboard commands.

- **turtlebot_rviz_launchers**: With the view_navigation.launch file, you can load a preconfigured rviz workspace. You’ll save a lot of time by launching this file, because it will automatically load the robot model, trajectories, and map for you.

- **turtlebot_gazebo**: With the turtlebot_world.launch you can deploy a turtlebot in a gazebo environment by linking the world file to it.

### Tasks
---
1. Design a simple environment with the Building Editor in Gazebo.
2. Teleoperate your robot and manually test SLAM.
3. Use the ROS navigation stack and manually commands your robot using the 2D Nav Goal arrow in rviz to move to 2 different desired positions and orientations.
4. Write a pick_objects node that commands your robot to move to the desired pickup and drop off zones.
5. Write an add_markers node that subscribes to your robot odometry, keeps track of your robot pose, and publishes markers to rviz.






