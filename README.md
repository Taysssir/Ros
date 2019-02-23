# Ros
## Robot Operating System (ROS) 
ROS is a meta-operating system for your robot.It provides language-independent and network-transparent communication for a distributed robot control system.

## Installation Notes

For full installation instructions, including system prerequisites and platform-specific help, see:

[Ros.org] ( http://wiki.ros.org/indigo/Installation/Ubuntu )


### Installing ROS Indigo on a Ubuntu 14.04 Fresh Install

ROS Indigo ONLY supports Saucy (13.10) and Trusty (14.04) for debian packages.
1.- Setup your sources.list:

Setup your computer to accept software from packages.ros.org.

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
2.- Setup your keys:

sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
3.- Verify Latest Debians

First, make sure your Debian package index is up-to-date:

sudo apt-get update
4.- Install ROS Indigo Desktop Full (Recommended)

sudo apt-get install ros-indigo-desktop-full
5.- Initialize rosdep

Before you can use ROS, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS.

sudo rosdep init

rosdep update
6.- Environment setup

It's convenient if the ROS environment variables are automatically added to your bash session every time a new shell is launched:

echo "source /opt/ros/indigo/setup.bash" >> ~/.bashrc

source ~/.bashrc

If you have more than one ROS distribution installed, ~/.bashrc must only source the setup.bash for the version you are currently using.

If you just want to change the environment of your current shell, you can type:

source /opt/ros/indigo/setup.bash
7.-Getting rosinstall

rosinstall is a frequently used command-line tool in ROS that is distributed separately. It enables you to easily download many source trees for ROS packages with one command.

To install this tool on Ubuntu, run:

sudo apt-get install python-rosinstall
END TUTORIAL: http://wiki.ros.org/indigo/Installation/Ubuntu
