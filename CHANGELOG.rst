^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package baxter_moveit_config
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.0.7 (2016-07-26)
------------------
* added gripper_action_controllers to controller list
* updated srdf file to launch files to consider grippers
* added all links of gripper to eef-group to allow a real grasping including touching the object
* re-enabled some collisions to avoid major collisions between arms and screen resp. torso
* Contributors: Arne Hitzmann

1.0.6 (2016-04-19)
------------------
* [fix] both_arm move group stopped functioning (`ref <https://groups.google.com/a/rethinkrobotics.com/forum/#!topic/brr-users/59kLdsAfR-g>`_)
* Contributors: Ian McMahon

1.0.5 (2016-02-10)
------------------
* [fix] Update ompl_planning.yaml to set default planning config, which is supported on moveit 0.7 (`moveit_ros/pull/625 <https://github.com/ros-planning/moveit_ros/pull/625>`_)
* Contributors: Kei Okada

1.0.4 (2016-01-15)
------------------
* Added Gripper construction Xacros for Baxter
  baxter.srdf.xacro is now the new "baxter.srdf" (the old one is
  left unchanged for backwards compatibility). The xacro creates the
  standard "no-gripper" Baxter srdf by default, but can enable new
  gripper collision checks if left or right_electric_gripper args are
  set to true. Also, the link used as the kinematic tip for each arm
  (<side>_tip_name) can be set at launch
  - Set the default tip name to be <side>_gripper
  - Now a default end effector sdf takes care of the default <side>_gripper
  collisions
  - Electric Gripper specific collisions use the correct finger link names
  - Fixed a move_group arg value in demo_baxter
  - Removed nefarious planning_context.launch call from move_group.launch
  which would overwrite all args from a previous move_group.launch call
* Contributors: Ian McMahon

1.0.3 (2015-11-02)
------------------

1.0.1 (2015-09-19)
------------------
* Initial binary DEB release
* Contributors: Kyle Maroney, Chris Smith, Ian McMahon, Isaac IY Saito, Kei Okada
