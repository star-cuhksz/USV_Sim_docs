====================================================
Welcome to USV Test Platform's documentation!
====================================================

USV Test Platform is a test environment base on `usv_sim_lsa`_.
It is developed to test control and trajectory strategies for USV, but it can be easily adapted to other applications.
It contains multiple robot models such as propelled boats(rudder boat, differential boat, airboat) and sailboat. 
Boats are affected by waves, wind and water currents, implemented by UWsim for water surface modeling, HEC-RAS for water speed of river and channel simulations, and Lattice Boltzmann in a 2D grid for wind current.
All those features allow to realistically modeling the movement of boats.

.. toctree::
   :hidden:
   :glob:

   modules/Operation/GettingStarted
   modules/Operation/Installation
   modules/Customization/Configuration
   modules/Issues
   modules/LeaderBoard

.. _`usv_sim_lsa`: https://github.com/disaster-robotics-proalertas/usv_sim_lsa
