# install-arm-package..

To install the arm package, go to src and install git, then install the arm package

```
 $ cd ~/catkin_ws/src
 $ sudo apt install git
 $ git clone https://github.com/smart-methods/arduino_robot_arm
```
### Install the dependencies
```
 $ cd ~/catkin_ws
 $ rosdep install --from-paths src --ignore-src -r -y
 $ sudo apt-get install ros-melodic-moveit
 $ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
 $ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
 $ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
```
### To compile packages
 ```$ catkin_make```
 
 After the install is complete,open it
 
 ``` $ roslaunch robot_arm_pkg check_motors.launch ```
 
![Screenshot from 2021-07-04 04-01-13](https://user-images.githubusercontent.com/85907057/124371265-bed19000-dc88-11eb-9a0d-91a4bb43ee5e.png)
 
 --------------------------------
 ## Is Installed arduino  
 
### install rossrial by using code
```
 $ sudo apt-get install ros-melodic-rosserial-arduino
 $ sudo apt-get install ros-melodic-rosserial 
```
### install ros_lib by using code
```
 $ cd Arduino/libraries
 $ rm -rf ros_lib
 $ rosrun rosserial_arduino make_libraries.py
 ```
 ------------------------------
## instructions to use gazebo

- in terminal
```
 $ cd catkin_ws
 $ source devel/setup.bash
 $ roslaunch robot_arm_pkg check_motors.launch
```
- in other terminal
```
 $ cd catkin_ws
 $ source devel/setup.bash
 $ roslaunch robot_arm_pkg check_motors_gazebo.launch
```
- in other terminal.change the permission
```
 $ cd catkin_ws/src/arduino_robot_arm/robot_arm_pkg/scripts
 $ sudo chmod +x joint_states_to_gazeo_py
```
- after that
```
 $ cd catkin_ws
 $ source devel/setup.bash
 $ rosrun robot_arm_pkg joint_states_to_gazebo.py
```
![Screenshot from 2021-07-04 05-19-42](https://user-images.githubusercontent.com/85907057/124371316-3f908c00-dc89-11eb-8089-8b0185fd3339.png)


--------------------------------
### running gazebo and RViz in moveit

 ```$roslaunch moveit_pkg demo.launch```


![Screenshot from 2021-07-04 05-42-37](https://user-images.githubusercontent.com/85907057/124371656-a6fc0b00-dc8c-11eb-9519-5c76c9e7724e.png)

![Screenshot from 2021-07-04 06-05-11](https://user-images.githubusercontent.com/85907057/124371816-250ce180-dc8e-11eb-9712-bbdbda4b0aaf.png)


  



