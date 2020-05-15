============
Installation
============

USV Test Platform is tested and supported on the following 64-bit systems:

* Ubuntu 16.04

Build from source
=================

Build a USV Test Platform Ros package from source and install it on Ubuntu Linux or virtual machine.
While the instructions might work for other systems,
it is only tested and supported for Ubuntu and virtual machine.

Setup for Linux
---------------

Installing ROS as described in the `ROS installation instructions`_
and setting up the ROS environment on your computer.
If you are ever having problems finding or using your ROS packages make sure
that you have your environment properly setup.

Install Python and the dependencies of USV Test Platform.

.. code-block:: bash

    sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential python-rosdep python-wxtools python-lxml python-pathlib python-h5py python-scipy python-geolinks python-gdal
    sudo apt-get install libfftw3-dev libxml++2.6-dev libsdl-image1.2-dev libsdl-dev

Configure and Build
-------------------

Creating a catkin workspace:

.. code-block:: bash

    source /opt/ros/kinetic/setup.bash
    mkdir -p ~/catkin_ws/src
    cd ~/catkin_ws/
    catkin_make

.. tip:: The ``catkin_ws`` just a folder name, can replace it for clearly and concisely.

Clone the usv_sim repository in the src folder of your catkin workspace:

.. code-block:: bash

    cd ~/catkin_ws/src
    git clone https://github.com/yikangGu/usv_sim_cuhksz.git

Clone submodules of the repository/

.. code-block:: bash

    git submodule init
    git submodule update

Click this `link`_ and download some robot model files for usv_sim_cuhksz.
Please mail to yikang.gu@qq.com for getting password.

After that, compile the stack:

.. code-block:: bash

    cd ~/catkin_ws
    catkin_make_isolated --install

If you are never having problems, that means your environment properly setup.

Install from package
====================

`Docker`_ uses containers to create virtual environments
that isolate a USV Test Platform installation from the rest of the system.

The USV Test Platform `Docker images`_ are already configured to run.

    the docker images will publishing soon.

.. _`Docker`: https://docs.docker.com/install
.. _`Docker images`: https://docs.docker.com/install
.. _`ROS installation instructions`: http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment
.. _`link`: https://pan.baidu.com/s/1KbNvG0fFAhX9V5q269Co-A
