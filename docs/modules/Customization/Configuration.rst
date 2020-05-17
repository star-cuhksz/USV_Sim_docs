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

How to import a robot
=====================

1. Prepare 2 formats of file, obj and dae.
2. Put them in usv_sim/meshes folder.
3. Create a xacro file to descript robot.
4. Create a xml file to descript a scenario for uwsim.

.. tip:: The uwsim just parse a urdf file name that "your-xacro-filename_uwsim".urdf.
    This file will created when run the "... parse:= true" command in terminal.
    So the xml file should import the urdf file replace the xacro file.

5. Create a launch file to import the robot when the uwsim and gazebo start.

Modify the xml file
===================

This a template for the xml file.

.. code-block:: xml

    <?xml version="1.0"?>
    <!DOCTYPE UWSimScene SYSTEM "UWSimScene.dtd">
    <UWSimScene>
        <oceanState>
            [Necessary]: to configure the uwsim scene setting,
            like the wind current and the water current.
        </oceanState>

        <simParams>
            [Necessary]: unknown
        </simParams>

        <camera>
            [Optional]: to configure the camera.
        </camera>

        <vehicle>
            [Necessary]: to configure a robot at least one.
        </vehicle>

        <object>
            [Necessary]: to configure the terrain.
        </object>

        <rosInterfaces>
            <ROSOdomToPAT>
                [Optional]: if a robot needs move.
            </ROSOdomToPAT>

            <OceanSurfaceToROSOceanVehicle>
                [Optional]: if a robot needs motion on the ocean face.
            </OceanSurfaceToROSOceanVehicle>

            <ROSJointStateToArm>
                [Optional]: if a robot needs are control.
            </ROSJointStateToArm>
        </rosInterfaces>
    </UWSimScene>


Other
=====

If have any problem that cannot be solved, welcome to contact yikang.gu@qq.com.
