=============
Configuration
=============

The usv_sim_cuhksz package has 8 subpackages.

|   usv_sim_cuhksz
|   ├── `usv_sim`_
|   ├── `usv_base_ctrl`_
|   ├── `usv_env_disturb`_
|   ├── `usv_dynamics`_
|   ├── `uwsim`_
|   ├── `freefloating_gazebo`_
|   ├── `usv_sim_rviz`_ (will be removed in future)
|   └── `usv_navigation`_ (will be removed in future)

usv_sim
=======

mainly contains configuration files and 3D model files.

::

    usv_sim
    ├── config
    │   └── sailboat.yaml                 this is the sailboat underlying PID controller configuration file
    ├── launch
    │   ├── models                        contains robot launch files
    │   ├── scenarios_launchs             contains scenario launch files
    │   └── world                         contains terrain launch files
    ├── meshes                            contains robot 3D model files
    ├── scenes
    │   ├── sailboat_scenario_cuhksz.xml  the scenario configuration file
    │   ├── sailboat_scenario1.xml
    │   └── UWSimScene.dtd
    ├── terrain                           contains terrain 3D model files
    ├── urdf
    ├── world
    ├── xacro                             the robot description files
    │   ├── boat_subdivided4.xacro
    │   ├── buoy.xacro
    │   ├── sailboat_cuhksz.xacro
    │   └── sailboat.xacro
    └── ...

usv_base_ctrl
=============

contains some controller scripts

usv_env_disturb
===============

contains configuration files for wind plugin and water plugin.

usv_dynamics
============

contains the

uwsim
=====

freefloating_gazebo
===================

usv_sim_rviz
============

the rviz configuration file

usv_navigation
==============
