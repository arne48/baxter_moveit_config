Baxter MoveIt!
==========
Author: Rethink Robotics Inc.

Website: https://github.com/RethinkRobotics/sdk-examples

MoveIt! configuration package for the Baxter Research Robot from Rethink Robotics.

PACKAGE DEPENDENCIES
---------
To use the baxter_moveit_config package you will need the baxter_description package containing Baxter's URDF. This package is available for download at the following repository:

   git clone https://github.com/RethinkRobotics/baxter_common.git

GRASPING ADDITIONS
---------
This config was modified to allow the usage of the pick & place capabilities of moveIt!

An additional launch file (baxter.launch) starts the necessary action servers.

The baxter.launch file considers the setup at our laboratory i.e. left eef is a Rethink Robotics parallel gripper and the right one is a vacuum gripper.

So you might either change it's default values in respect to your setup or start the launch files parameterized.

