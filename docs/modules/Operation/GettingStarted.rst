===============
Getting Started
===============

Install the simulator 
---------------------

Before starting these tutorials please complete installation as described in the `installation instructions`_.

Run a demo
--------------------

\'source\' the bash file to make sure your workspace is properly overlaid by the setup script,
make sure ROS_PACKAGE_PATH environment variable includes the directory you're in.

::

    source ~/catkin_ws/install_isolated/setup.bash

.. note:: if you haven't added this command in .bashrc file,
    you need to \'source\' the bash file every time open a new terminal.

Start the ROS core service process and parse the launch file to prepare to run the simulation.

.. code-block:: bash

    roscore &
    roslaunch usv_sim sailboat_scenario1.launch parse:=true

.. note:: The message of the command (roslaunch usv_sim \*.launch parse:=true) is not an error. It is just a warning that the parsing ended.

Run a scenario:

.. code-block:: bash

    roslaunch usv_sim sailboat_scenario1.launch parse:=false

.. tip:: The `issues instructions`_ may help you if launch failed.

Control your robot
------------------

We can run the python script to control our robot quickly in the usv_base_ctrl ros package.
Go to the usv_base_ctrl/scripts folder, then run this command:

.. code-block:: bash
    
    python headingControl_for_scene1.py

Of cause, we can modify this script to control robot better now.
The sailboat_controller.py is a controller contains some usv_sim API for uses quickly.

If you want to control robot manually, you can run the keyboard_teleop script.

.. code-block:: bash

    python keyboard_teleop.py

The next section will show you more about the usv_sim_cuhksz.

Configure your project
----------------------

The `configuration instructions`_ shows that how can configure this project.

.. _`installation instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Operation/Installation.html
.. _`configuration instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Customization/Configuration.html
.. _`issues instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Issues.html
