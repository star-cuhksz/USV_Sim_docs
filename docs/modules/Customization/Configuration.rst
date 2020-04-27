=============
Configuration
=============

This usv_sim_cuhksz package has 6 subpackages.

- usv_sim:
    Contains setup configuration files, launch files and model files.

    - config : robot joint PID control parameters.
    - launch/models : robots launch file.
    - launch/scenarios_launchs : scenarios launch file.
    - launch/world : terrain launch file.
    - meshes : robot 3D model file.
    - scenes : uwsim scenario description file.
    - terrain : terrain 3D model file.
    - urdf : urdf format robot description file.
    - world : gazebo world description file.
    - xacro : xacro format robot description file.

- usv_base_ctrl
    Robot control

- usv_env_disturb
    It can display the data from the third-party plug-in on the rviz and act on the robot when the environment type is local.

    - wind_current
    - water_current

- freefloating_gazebo [Changes are not recommended]
    A Gazebo plugin to simulate and control underwater vehicles.
    The package builds two Gazebo plugins:

    - freefloating_gazebo_fluid (world plugin)
        simulates buoyancy and viscous force from water.
    - freefloating_gazebo_control (model plugin)
        opens topics for thrusters and joints, in order to control the considered robots.

- usv_dynamics [Changes are not recommended]
    - foil_dynamics_plugin : a gazebo plugin for CFD model.

- uwsim [Changes are not recommended]
    UWSim is a tool for testing and integrating perception and control algorithms before running them on the real robots.

    - underwater_simulation
    - uwsim_bullet
    - uwsim_osgbullet
    - uwsim_osgocean
    - uwsim_osgworks
    - visualization_osg
