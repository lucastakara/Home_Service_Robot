# Home Service Robot Project

## Introduction
-----

The goal of this project is creating a full home service robot capable of navigating to pick up and deliver virtual objects.
 
![Gazebo](https://github.com/lucastakara/Where_Am_I/blob/master/images/Goal.png?raw=true)
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

## Getting Started
----
The following items are required in order to visualize and create the project:
 
#### Installation Instructions:

#### Prerequisites / Dependencies 

- Gazebo >= 7.0

- ROS Kinetic

- gcc/g++ >= 5.4

- Linux: gcc / g++ is installed by default on most Linux distros

- [Linux Ubuntu 16.04.6 LTS (Xenial Xerus)](http://releases.ubuntu.com/16.04/)
- [Gazebo](http://gazebosim.org/tutorials?tut=install_ubuntu&cat=install) 
- [Robot Operating System](http://wiki.ros.org/kinetic/Installation/Ubuntu) (ROS)

Once these components are installed, you need to create a Catkin Workspace:


- `$ mkdir -p catkin_ws/src`

- `$ cd catkin_ws/src`

- `$ catkin_init_workspace`

Download/clone the repository and copy the "my_robot","ball_chaser" directory in the src directory:

- `$ git clone https://github.com/lucastakara/Where_Am_I`


`Then, navigate up to the top-level catkin workspace directory and build the executables:

- `cd ..`
- `catkin_make` 

Next, you can open Gazebo with the robot in it:

- `$ source devel/setup.bash`

- `$ roslaunch my_robot world.launch`



This will initialize all the nodes. In Rviz, you should see a red robot on a black and white map, surrounded by red arrows representing the particles associated with the AMCL filter.

To operate the robot via the keyboard, open a second terminal, navigate to the root level directory and execute:


- `$ source devel/setup.bash`
- `$ rosrun teleop_twist_keyboard teleop_twist_keyboard.py`


