# Controlling the robot arm by joint_state_publisher, Moveit and kinematics

## Create a workspace by using catkin_make
- source /opt/ros/noetic/setup.bash
- mkdir -p ~/catkin_ws/src
- cd ~/catkin_ws/
- catkin_make
- source devel/setup.bash

## Install the arduino_robot_arm package
- cd ~/catkin_ws/src
- sudo apt install git
- git clone https://github.com/smart-methods/arduino_robot_arm
### install all the dependenceies
- cd ~/catkin_ws
- rosdep install --from-paths src --ignore-src -r -y
- sudo apt-get install ros-noetic-moveit
- sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
- sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
- sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control Compile the package
- catkin_make

![image](https://github.com/user-attachments/assets/f03453fb-c80f-47c9-99d7-12fe7b43e212)



## Controlling the robot arm by joint_state_publisher

### Run the following instructions to use gazebo

- roslaunch robot_arm_pkg check_motors.launch
- roslaunch robot_arm_pkg check_motors_gazebo.launch
- rosrun robot_arm_pkg joint_states_to_gazebo.py

### In its initial position
<img width="926" alt="image" src="https://github.com/user-attachments/assets/ff6c2660-db35-4ffe-8dce-b74783747953">

### After moving
![image](https://github.com/user-attachments/assets/7d146eea-da1a-4b71-a1f0-8193bebda343)

### Gazebo launch
![image](https://github.com/user-attachments/assets/4acee130-a850-4166-a063-aaf4d734208b)

## Controlling the robot arm by Moveit and kinematics 

### Run the following instruction to use gazebo

- roslaunch moveit_pkg demo_gazebo.launch

![image](https://github.com/user-attachments/assets/8e7151fb-1b8e-49dc-8d07-709bf279634c)


## when using Approx IK solution if i moved the ball and pressed plan and execute the robot will move In a spontaneous way without giving him any angle only position

https://github.com/user-attachments/assets/052d81e7-15cd-4d94-acc3-06f77e36fc97

