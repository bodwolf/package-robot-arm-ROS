# package-robot-arm-ROS

# need before
1-install  virtualbox
2-install  ubuntu
3-install  ROS




# first step
1-open virtualbox and use ubuntu

![image](https://user-images.githubusercontent.com/107868423/183302425-5d3cd258-704c-4301-99ea-bb020f197c1e.png)

2- open terminal


![image](https://user-images.githubusercontent.com/107868423/183302452-a9d6b132-e4a7-4ad8-a362-dd166ddb35b6.png)


3-writing code one by one



sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt-get update

sudo apt-get install ros-kinetic-desktop-full

apt-cache search ros-kinetic

echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

sudo apt install python-rosdep

sudo rosdep init

rosdep update

sudo apt-get install ros-noetic-catkin

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git 

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-kinetic-moveit

sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line
(source /home/abdullah/catkin_ws/devel/setup.bash)
then 


click (ctrl+o)


![image](https://user-images.githubusercontent.com/107868423/183302635-ecb3a513-7872-4269-81b6-3ad2dfd78d8e.png)


click Enter


click (ctrl+x)


![image](https://user-images.githubusercontent.com/107868423/183302667-48217ffb-7740-4dc1-949d-a560df2fd132.png)


source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch


![image](https://user-images.githubusercontent.com/107868423/183302762-413f7a26-41fd-4282-9e13-cd9d87651b28.png)



