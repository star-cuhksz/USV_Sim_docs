===============
Getting Started
===============

What is this?
=============

This a simulator and uses a combination of multiple physics packages to build a test environment for Unmanned Surface Vehicles (USV). 

Quickly Start
=============

1. Install the simulator 
------------------------

Before starting these tutorials please complete installation as described in the `installation instructions`_.

2. Run a demo
------------------------

\'source\' the bash file to make sure your workspace is properly overlaid by the setup script,
make sure ROS_PACKAGE_PATH environment variable includes the directory you're in.

::

    source ~/catkin_ws/install_isolated/setup.bash

.. note:: if you haven't added this command in .bashrc file,
    you need to \'source\' the bash file every time open a new terminal.

Run a scenario:

.. code-block:: bash

    roscore &
    roslaunch usv_sim_cuhksz sailboat_scenario1.launch parse:=true
    roslaunch usv_sim_cuhksz sailboat_scenario1.launch parse:=false

.. tip:: The `error instructions`_ may help you if the startup failed many times.


3. Configure your project
-------------------------

The `configuration instructions`_ shows that how can configure this project.

.. _`installation instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Operation/Installation.html
.. _`configuration instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Customization/Configuration.html
.. _`error instructions`: https://usv-sim-docs.readthedocs.io/en/latest/modules/Error.html
