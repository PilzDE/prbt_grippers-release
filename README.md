# prbt_gripper

## Package: prbt_grippers
The meta package contains support for using the PILZ manipulator PRBT robot with a gripper.

## Package: prbt_pg70_support
The package enables the usage of the PILZ manipulator PRBT with a Schunk pg+70 gripper.

### Usage
If the package is installed, simply append `gripper:=pg70` to your roslaunch command like this:
`roslaunch prbt_moveit_config moveit_planning_execution.launch sim:=true pipeline:=ompl gripper:=pg70`

Basically this packages plugs the necessary parameters into the existing launchfiles from
[prbt_moveit_config](https://wiki.ros.org/prbt_moveit_config) to start the manipulator with an attached gripper.
If you want to add another gripper it is recommended to follow the naming convention by naming your package
prbt_[gripper_name]_support.

## Technical limitation
The gripper package is separated from the robot description to allow an installation
without all the dependencies of the gripper packages
(e.g. schunk_description currently depends on gazebo).
