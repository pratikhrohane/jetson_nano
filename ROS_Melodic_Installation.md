# ROS MELODIC

Get ROS Pacakge from packages.ros.org
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
Setup the Secure Key
```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
Update the Package
```
sudo apt update
```
Download the Desktop Version
```
sudo apt install ros-melodic-desktop
```
Setup Environment Variable
```
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

ROS installtion is completed, can check by
```
export | grep ROS
```

Install other ROS Tools
```
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
```

Initilize ROSDEP
```
sudo apt install python-rosdep
sudo rosdep init
rosdep update
```

Check ROS Version 
```
rosversion -d
```
___

Create Catkin Workspace
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
```

Configure Catkin Workspace
```
catkin_make
```
Update .bashrc File
```
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc 
source ~/.bashrc
```
***
