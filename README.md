steps
1. install virtualBox
Go to www.virtualbox.org and download the newest version of VirtualBox for OS you're using

2. setting up virtualBox

In order to install Ubuntu on VirtualBox, you should have a physical computer with at least 4 GB of RAM , a hard disk drive with at least 20 GB of free space of hard disk. Your CPU  must support Intel VT-x or AMD-v hardware virtualization features which must also be enabled in UEFI/BIOS. This point is especially important if you are looking for how to install Ubuntu 64-bit on VirtualBox.

3. installing ubunto 20.04 LST on virtualBox

4. install Ros melodic
Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." You can follow the Ubuntu guide for instructions on doing this.
 http://wiki.ros.org/melodic/Installation/Ubuntu

Setup your computer to accept software from packages.ros.org.
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

3. Set up your keys
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

4. Installation
First, make sure your Debian package index is up-to-date:
sudo apt update

Desktop-Full Install: ROS, rqt, rviz, robot-generic libraries, 2D/3D simulators and 2D/3D perception
sudo apt install ros-noetic-desktop-full
Desktop Install: ROS, rqt, rviz, and robot-generic libraries
sudo apt install ros-noetic-desktop
ROS-Base: (Bare Bones) ROS package, build, and communication libraries. No GUI tools.
sudo apt install ros-noetic-ros-base
There are even more packages available in ROS. You can always install a specific package directly.
sudo apt install ros-noetic-PACKAGE
For example:
sudo apt install ros-noetic-slam-gmapping

5. Environment setup
You must source this script in every bash terminal you use ROS in.
source /opt/ros/noetic/setup.bash

It can be convenient to automatically source this script every time a new shell is launched. These commands will do that for you:
bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc source ~/.bashrc
zsh
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc source ~/.zshrc
