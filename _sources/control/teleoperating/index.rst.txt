.. _teleoperating:

***********************************************
Teleoperating the mobile base with the keyboard
***********************************************


Purpose
#######

This tutorial shows a way to teleoperate the mobile base of TIAGo using the keyboard. This relies on the ROS2 package `teleop_twist_keyboard`_ which is compatible with most of ROS2 enabled robots.

Pre-Requisites
##############

First make sure that the tutorials are properly installed along with the tiago simulation, as shown in the tutorials `installation`_ section. 

Execution
#########

First of all open two consoles and source ros setup

.. code:: bash

   source /opt/ros/foxy/setup.bash

In the first console launch the TIAGo gazebo simulation simulation

.. code:: bash

   ros2 launch tiago_gazebo tiago_gazebo.launch.py

This will launch a gazebo empty world with a TIAGo.

.. image:: media/gazebo_nav.png
    :alt: gazebo

In the second console launch the keyboard teleoperation node

.. code:: bash

   ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args --remap cmd_vel:=key_vel

.. image:: media/key_teleop.png
    :alt: teleop ros2

Now you can navigate the robot to correct the position error.

.. _installation: https://cesc-folch.github.io/tiago-tutorial/installation
.. _tiago_mapping: https://cesc-folch.github.io/tiago-tutorial/mapping
.. _teleop_twist_keyboard: https://index.ros.org/p/teleop_twist_keyboard/github-ros2-teleop_twist_keyboard
