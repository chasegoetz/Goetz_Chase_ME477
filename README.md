# Goetz_Chase_ME477

This is my github repository for the ME477 Robotics mini-course final project. The project consists of three main packages Goetz Topics, Goetz Services, and Goetz Actions. The packages are useful because they highlight different types of counters and node interactions. They can be launched easily displaying their functions. 

## Requirements

These packages were created in Linux based environment on ubuntu18. The ros distro is melodic, version 1.14.4. 

## Installation

To make these packages available to your ROS distribution, complete the following steps...

1.Create a ROS workspace with a src directory.
    
2.Fork and clone the repository to this src directory.

git clone https://github.com/chasegoetz/Goetz_Chase_ME477.git

3.In the workspace, execute a catkin_make command.

4.The workspace should then be sourced with the following command.

source devel/setup.bash

These packages can then be navigated or run using the included launch files.

## Goetz Topics

The ROS naming convention for Goetz Topics is goetz_topics. To launch this package, the following command should be entered when in the workspace root. (Note: If launching in a new terminal, the workspace should be built with catkin_make and sourced with source devel/setup.bash)

roslaunch goetz_topics topics.launch

When launched, random numbers will incrementally be published for both real and imaginary. The subscriber prints the message data to the terminal. This repeats until the it is prompted to stop with CTRL+C.

## Goetz Services

The ROS naming convention for Goetz Services is goetz_services. To launch this package the following command should be entered when in the workspace root. (Note: If launching in a new terminal, the workspace should be built with catkin_make and sourced with source devel/setup.bash)

roslaunch goetz_services services.launch input:='*insert text*'

When launched, the inserted text will be processed. The server node breaks up the text to be counted by the word count service file. Then the client processes and prints the request, displaying the text and the corresponding word count. To exit after the process has successfully run, CTRL+C must be input. 

## Goetz Actions

The ROS naming convention for Goetz Actions is goetz_actions. To launch this package the following command should be entered when in the workspace root. (Note: If launching in a new terminal, the workspace should be built with catkin_make and sourced with source devel/setup.bash)

roslaunch goetz_actions fancy_action.launch

When launched, the feedback will be display the elapsed time between communication of the server and client nodes. It also displays how much time is remaining in the set 5 seconds. This will run until the 5 seconds has elapsed. To prevent excessive time intervals a seperate function will abort the task. To exit after the process has successfully run, CTRL+C must be input. 

## Origins 

These packages were origanally from Programming Robots with ROS, by Morgan Quigley, Brian Gerkey and William D. Smart (O'Reilly Media, Inc., 2015). It was forked for educational use in this project.