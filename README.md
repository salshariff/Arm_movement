**Arm_movement**
#  workspace by using catkin_make
## installed catkin
* $ source /opt/ros/melodic/setup.bash

## create catkin workspace:
* $ mkdir -p ~/catkin_ws/src
* $ cd ~/catkin_ws/ 
* $ catkin_make
## To make it easier to use the code
* $ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc $ source ~/.bashrc
## Add the “arduino_robot_arm” package to “src” folder
* $ cd ~/catkin_ws/src
* $ sudo apt install git
* git clone https://github.com/smart-methods/arduino_robot_arm
## Install all the dependencies
* $ cd ~/catkin_ws
* $ rosdep install --from-paths src --ignore-src -r -y
* sudo apt-get install ros-melodic-moveit
* $ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
* $ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
* $ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
## To collect packages
* $ catkin_make
## install rossrial by using code
* $ sudo apt-get install ros-melodic-rosserial-arduino
* $ sudo apt-get install ros-melodic-rosserial 
## install ros_lib by using code
* $ cd Arduino/libraries
* $ rm -rf ros_lib
* $ rosrun rosserial_arduino make_libraries.py
# instructions to use gazebo
## in terminal
* $ cd catkin_ws
* $ source devel/setup.bash
* $ roslaunch robot_arm_pkg check_motors.launch
## in other terminal
* $ cd catkin_ws
* $ source devel/setup.bash
* $ roslaunch robot_arm_pkg check_motors_gazebo.launch
## in other terminal.change the permission
* $ cd catkin_ws/src/arduino_robot_arm/robot_arm_pkg/scripts
* $ sudo chmod +x joint_states_to_gazeo_py
## after that
* $ cd catkin_ws
* $ source devel/setup.bash
* $ rosrun robot_arm_pkg joint_states_to_gazebo.py
# running package moveit
* $roslaunch moveit_pkg demo.launch
# running with Arduino
## in terminal
* $ roslaunch moveit_pkg demo.launch
## in other terminal
* $ rosrun rosserial_python serial_node.py _port:=/dev/ttyUSB0 _baud:=115200
* ![](images/Screenshot from 2021-06-30 04-31-08.png)


  



