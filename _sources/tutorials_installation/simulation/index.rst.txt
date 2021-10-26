.. _mapping:

******************************
TIAGo ROS2 simulation tutorial
******************************


Purpose
#######

This tutorial shows how to make simulate TIAGo with ROS2 in gazebo.

Pre-Requisites
##############

First make sure that the tutorials are properly installed along with the TIAGo simulation, as shown in the tutorials `installation`_ section.

Execution
#########

First of all open one consoles and source ros setup

.. code:: bash

   source /opt/ros/foxy/setup.bash

Now you can launch the TIAGo simulation

.. code:: bash

   ros2 launch tiago_gazebo tiago_gazebo.launch.py

.. image:: media/pal-hey5.png
    :alt: gazebo simulation

If you want to choose the type of end effector of the robot you can use the launch argument:

.. code:: bash

   ros2 launch tiago_gazebo tiago_gazebo.launch.py end_effector:=pal-gripper

.. image:: media/pal-gripper.png
    :alt: gazebo TIAGo with gripper

.. code:: bash

   ros2 launch tiago_gazebo tiago_gazebo.launch.py end_effector:=pal-hey5

.. image:: media/pal-hey5.png
    :alt: gazebo TIAGo with hey5

.. _installation: http://cesc.folch.github.io/tiago-tutorial/tutorials_installation/installation
