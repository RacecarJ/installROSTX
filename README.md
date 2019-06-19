# installROSTX
Install Robot Operating System (ROS) on NVIDIA Jetson TX Dev Kits

These scripts will install Robot Operating System (ROS) on the NVIDIA Jetson TX1 and Jetson TX2  Development Kit.

Tested on L4T 28.1 (Ubuntu 16.04). L4T 28.1 was installed with JetPack 3.1.

The script is based on the Ubuntu ARM install of ROS Kinetic: http://wiki.ros.org/kinetic/Installation/UbuntuARM

Maintainer of ARM builds for ROS is http://answers.ros.org/users/1034/ahendrix/

<strong>updateRepositories.sh</strong>
This is an optional step. Adds the repositories universe, multiverse, and restricted and then apt-get update. These repositories are in the standard 28.1 install, so probably not needed.

<strong>installROS.sh</strong>
Adds the ROS sources list, sets the keys and then loads ros-kinetic-ros-base. Edit this file to add other ROS packages for your installation. After loading, rosdep is initialized.

<strong>setupCatkinWorkspace.sh</strong>
Usage:

$ ./setupCatkinWorkspace.sh [optionalWorkspaceName]

where optionalWorkspaceName is the name of the workspace to be used. The default workspace name is catkin_ws. This script also sets up some ROS environment variables. Refer to the script for details.

<em><b>Note:</b> On June 7, 2019 the GPG key for ROS was changed due to security issues. If you have ROS installed on your system before this, you should delete the GPG key:</em>
 
<pre>
$ sudo apt-key del 421C365BD9FF1F717815A3895523BAEEB01FA116
</pre> 


## Release Notes
June 2019
* L4T 28.1
* Update ROS GPG Key

November 2017
* L4T 28.1


## License
MIT License

Copyright (c) 2017 Jetsonhacks
Copyright (c) 2017 Kangalow LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
 
